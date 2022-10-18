**mvc패턴**

- mvc패턴이란?
    
    model, view, controller의 약자로 model은 실제 데이터베이스에 데이터 처리하는 장소 view는 사용자한테 보여주는 장소이다 그리고 controller는 model과 view 사이에 있으며 둘을 연결한다 일종의 허브 그리고 양방향 디자인 패턴이다
    
- mvc 패턴을 사용하는 이유는?
    
    패턴을 사용하는 이유는? 비즈니스 로직과 UI 로직을 분리하여 유지 보수를 독립적으로 수행할 수 있다
    Model과 View가 다른 컴포넌트들에 종속되지 않아 애플리케이션의 확장성, 유연성에 유리하고 중복 코딩의 문제점 제거한다.
    
- mvc패턴 문제는 뭘까?
    
    MVC 패턴에서 View는 Controller에 연결되어 화면을 구성하는
    단위 요소이므로 다수의 View를 가질 수 있습니다. 그리고 Model은
    Controller를 통해서 View와 연결되지만, Controller에 의해서 하나의 View에
    연결될 수 있는 Model도 여러 개가 될 수 있어 View와 Model이 서로 의존성을 띠게 됩니다. 즉, Controller에 다수의
    Model과 View가 복잡하게 연결된 상황이 발생할 수도 있습니다.
    그래서 이 문제를 해결하기 위해서 페이스북 팀에서 flux라는 패턴을 만들었습니다.
