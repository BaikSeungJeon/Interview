![Singleton](https://user-images.githubusercontent.com/75124028/197334205-42e7f46a-4dfe-414c-b0c0-fe284026f286.png)


- **특징**
    
    singleton 패턴은 클래스의 인스턴스를 만들어서 해당하는 인스턴스를 전역에서 참조할 수 있게 만들어서 해당 인스턴스를 공유하게 만들어서 앱의 전역 상태를 관리하도록 만들어진 패턴입니다. 대신 저장소는 하나로 만듭니다. (인스턴스를 한 개만 만들도록 강제한다.)
    
- **장점**
    
    인스턴스를 하나만 만들도록 강제하기 때문에 많은 메모리 공간을 절약할 수가 있습니다.
    
- **단점**
    
    인스턴스가 많은 일을 하거나 많은 데이터를 변경 시킬 경우 다른 클래스의 인스턴스 간에 결합도가 높아져 수정 및 단위테스트에 어려움이 생깁니다.
    
- **React의 전역 상태 관리는?**
    
    React에서는 상태관리를 위해서 singleton 인스턴스를 만드는 것 대신 Redux, contextApi를 사용합니다. singleton과 유사하지만 singleton은 인스턴스 값을 직접 수정할 수 있지만 해당 도구들은 읽기 전용 상태로 제공합니다. 따라서 개발자가 의도한 대로만 수정되도록 하는 것입니다.