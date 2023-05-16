# 상속

상속이란 부모 클래스의 멤버를 자식 클래스에게 물려주어서 상위 클래스의 필드 메서드와 같은 멤버들을 하위 클래스에서도 사용 가능하게 해주는 개념이다.

## 클래스 상속

현실에서 상속은 부모가 자식을 선택해서 물려주지만, 프로그램에서는 자식이 부모를 선택해 어떤 부모 클래스를 상속받을 것인지 결정한다.

```java
class 자식클래스 extends 부모글래스 {
  //필드
  //생성자
  //메소드
}
```

> 자바에서 상속은 단 하나의 부모 클래스만 상속받을 수 있고, private 접근 제한을 갖는 필드와 메소드는 상속 대상에서 제외된다.
> 

## 부모 생성자 호출

자바에서도 자식 객체를 생성하면, 부모 객체가 먼저 생성되고 그다음에 자식 객체가 생성된다. 이러한 부모 클래스의 객체 생성을 위한 생성자는 자식 클래스에서 **super문**으로 호출된다.

### super문

(다음은 Sudent가 People 클래스를 상속받는 코드를 작성한 것이다)

```java
//부모 클래스
public class People {
  public int age;
  public String name;

  public People(int age, String name) {
    this. age = aeg;
    this. name = name;
  }
}

//자식 클래스
public class Student extends People {
  public int classNumber;

  public Student(int age, String name, int classNumber) {
    super(age, name);                       //부모 생성자 호출
    this.classNumber = classNumber;            
  }
} 
```                                                                                                    
