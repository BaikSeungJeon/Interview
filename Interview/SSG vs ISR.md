- SSG
    - SSG는 Static Site Generation의 약자로 페이지를 생성할 때 기본으로 적용되는 설정입니다.
    - SSR과 다른 점은 클라이언트가 요청하는 시점이 아니라 빌드 시에 페이지를 미리 생성해놓는 것입니다.
    
    ```jsx
    export default function Ssg({res}) {
      return (
        <main>
          <Components res={res} />
        </main>
      );
    }
    export const getStaticProps: GetStaticProps = async () => {
      const res = await axios.get('api주소');
      return {
        props: res
      };
    };
    ```
    
    - 처음 빌드시에 페이지를 생성해 놓기 때문에 데이터가 중간에 변경이 되어도 빌드하지 않는이상은 페이지에 반영되지 않습니다.
- ISR
    - ISR은 Incremental Static Regeneration의 약자로 빌드 시점에 페이지를 렌더링 한 후, 설정한 시간 마다 페이지를 새로 렌더링 합니다. 즉, ISR로 구분했지만 사실 SSG에 포함되는 개념이라고 할 수 있습니다. SSG는 빌드 시에 페이지를 생성하기 때문에 fetching 하는 데이터가 변경되면 다시 빌드해야 하지만 ISR은 일정 시간마다 알아서 페이지를 업데이트 해줍니다.
    
    ```jsx
    export default function Isr({res}) {
      return (
        <main>
           <Components res={res} />
        </main>);
    }
    
    export const getStaticProps: GetStaticProps = async () => {
      const res = await axios.get('api주소');
      return {
        props: res,
        revalidate: 50,
      };
    };
    ```
    
    - revalidate라는 값을 설정해주면 해당 초마다 페이지가 새로 업데이트 됩니다.
