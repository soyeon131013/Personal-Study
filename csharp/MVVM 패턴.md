# MVVM 패턴
**MVVM** **패턴**이란 Model, View, View Model의 약자로 프로젝트를 진행할 때 작업의 분업화, 이후 유지보수를 용이하게 하기 위해 나온 개념이다. 이 패턴을 쓰는 이유는 View와 Model 사이의 의존성 최소화를 위해서이다.    
구조는 Model, View, View Model의 세 가지로 이루어져 있다.   
![MVVM 구조](https://docs.microsoft.com/en-us/previous-versions/msp-n-p/images/hh830877.1afe20bab0052f5ab0fc400bf3b6f3f7%28en-us%2cpandp.10%29.png)   
###### 출처: https://docs.microsoft.com/en-us/previous-versions/msp-n-p/hh848246(v=pandp.10)?redirectedfrom=MSDN
- Model: 화면과 관련된 데이터 요소. 비즈니스 로직을 작성하는 곳이다. 예를 들어, 주소록을 만든다고하면, 이름, 나이, 이메일 등 가장 기본적인 변수를 넣는 것이다.   
- View: 화면에 보여지는 구성 요소. 쉽제 말하면 사용자들이 눈으로 보는 페이지이다.   
- View Model: 화면의 동장 방식 및 흐름을 표현하는 곳. View와 Model을 연결시켜주는 곳이다. 이곳에는 UI 로직, 커맨드, 이벤트, 모델에 대한 참조가 포함되어 있다.   
   
View에 표시되는 데이터는 데이터바인딩을 통해 갱신을 하게된다. 데이터 바인딩은 바인딩 대상과 바인딩 소스 간의 상호 작용으로 일어난다.     
   
또한 MVVM에서는 두 가지의 인터페이스를 사용한다.   
- INotifyPropertyChanged : xaml의 디자인 한 폼에서 데이터의 즉각적 변화나 데이터를 가져올 때 사용하는 인터페이스이다.    
- ICommand: xaml에서 액션과 이벤트를 처리하기 위한 인터페이스이다.    
   
그림을 보며 결론적으로 MVVM의 과정을 설명하자면, View는 View Model에게 데이터 바인딩과 Command를 요청하고 View Model은 그 요청을 Model에게 전달한다. 그리고 View와 View Model은 Notification을 받게 된다.   
   
이 MVVM 패턴은 복잡한 설계를 단순하게 만드는데 도움을 준다. 그렇기 때문에 소규모 프로젝트 보다는 대규모 프로젝트에 도움이 될 것이다.





















###### 내용 출처: https://itpro.tistory.com/8 
###### 내용 출처: https://centbin-dev.tistory.com/2