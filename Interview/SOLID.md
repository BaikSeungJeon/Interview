- ### SOLID란?
    - SOLID란 로버트마틴이 2000년대 초반에 명명한 객체지향 프로그래밍 및 설계의 다섯 가지 기본 원칙을 소개한 것입니다. 프로그래머가 시간이 지나도 [](https://ko.wikipedia.org/wiki/%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4_%EC%9C%A0%EC%A7%80_%EB%B3%B4%EC%88%98)유지보수와 확장이 쉬운 시스템을 만들고자 할 때 이 원칙들을 함께 적용할 수 있습니다.
    SOLID 원칙들은 소프트웨어 작업에서 프로그래머가 소스코드가 읽기 쉽고 확장하기 쉽게 될 때까지 소프트웨어 소스 코드를 리팩토링하여 코드 냄새를 제거하기 위해 적용할 수 있는 지침입니다.

- **SRP (Single Responsibility) 단일 책임 원칙**
    - 한 클래스는 하나의 책임만 가져야한다.
    - 한 클래스가 수행할 수 있는 기능(책임)이 여러 개라면, 클래스 내부 함수끼리 강한 결합이 발생하면 유지 보수시에 매우 어렵기 때문에 책임을 잘게 쪼개어 분리시키라는 말입니다.

- **OCP (Open-Closed) 개방-폐쇄 원칙**
    - 소프트웨어 요소는 확장에는 열려 있으나 변경에는 닫혀 있어야 한다.
    - 기존의 코드를 변경하지 않고 기능을 수정하거나 추가할 수 있도록 설계해야합니다
    - 자주 변화하는 부분을 추상화함으로써 기존 코드를 수정하지 않고 기능을 확장할 수 있도록해서 유연함을 높이는 방법을 사용합니다.

- **LSP (Liskov Substitution) 리스코프 치환 원칙**
    - 상위 타입의 객체를 하위 타입의 객체로 치환해도 상위 타입을 사용하는 프로그램은 정상적으로 동작해야 한다
    - 하위 타입 객체가 상속받은 상위 타입의 객체의 메소드나 프로퍼티를 마음대로 변경하지 말라는 의미인것같습니다.

- **ISP (Interface Segregation) 인터페이스 분리 원칙**
    - 특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나보다 낫다
    - 각 클라이언트가 필요로 하는 인터페이스(추상화)를 분리함으로써 A인터페이스가 변경이 되더라도 B인터페이스는 영향을 받지 않도록 만들어야 합니다.

- **DIP (Dependency Inversion) 의존 역전 원칙**
    - 프로그래머는 “추상화에 의존해야지, 구체화에 의존하면 안된다
    - 고수준 클래스와 저수준 클래스는 서로 의존하지 않아야하고 추상화에 의존 해야합니다.
    - 구현이 변경되더라도 추상화가 변경되면 안됩니다. 즉 새로운 기능이 추가되어도 추상화는 변경되지 않아야합니다.
    - ![의존성 역전 원칙](https://user-images.githubusercontent.com/75124028/198244792-f7f29ecc-7ecf-4736-8944-ea57890e9c5f.png)