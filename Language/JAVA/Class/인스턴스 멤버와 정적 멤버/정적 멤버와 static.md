## 정적 멤버와 static

정적 멤버란 클래스에 고정된 맴버로서 **객체를 생성하지 않고 사용할 수 있는 필드와 메소드**를 말하며, 이들을 각각 정적 필드, 정적 메소드라고 부른다.

- 정적 필드와 정적 메소드는 원칙적으로는 **클래스 이름으로 접근**해야 하지만 객체 참조 변수로도 접근이 가능하다. (하지만 정적 요소는 클래스 이름으로 접근하는 것이 좋다.)

### 정적 멤버 선언

```jsx
public class 클래스 {
    //정적 필드
    static 타입 필드 [= 초기값];
    
    //정적 메소드
    static 리턴 타입 메소드( 매개변수선언, ...) {...}
}
```

### 정적 필드

객체마다 가지고 있을 필요없이 공용 데이터라면 정적 필드를 사용한다.

```jsx
public class Calculator {
    String color;                //계산기별로 색깔이 다를 수 있다.
    static double pi = 3.141592; //계산기에서 사용하는 파이 값은 동일하다.
}
```

### 정적 메소드

인스턴스 필드를 가지고 있다면 인스턴스 메소드를 사용하고, 인스턴스 필드를 포함하지 않는다면 정적 메소드를 사용한다.

정적 메소드에서 인스턴스 멤버를 사용하고 싶다면 객체를 먼저 생성하고 참조 변수로 접근해야 한다.

```jsx
public class Calculator {
    String color;                                       //인스턴스 필드        
    void setColor(String color) {this.color = color; }  //인스턴스 메소드
    static int plus(int x, int y) {return x+y; }        //정적 메소드
    static int minus(int x, int y) {return x-y; }       //정적 메소드
}
```
