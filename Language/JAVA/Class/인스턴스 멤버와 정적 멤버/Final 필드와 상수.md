## Final 필드와 상수

final필드란 ‘최종적인 필드’라는 뜻으로 final필드는 **초기값이 저장되면** 이것이 **최종적인 값**이 되어서 프로그램 실행 도중에 수정할 수 없다.

 

### final 필드를 초기화 하는 방법

- 필드 선언 시에 초기화
- 생성자를 통해서 초기값을 지정

```java
public class Person {
    final String nation ="Korea";   //final 필드를 선언, 초기화
    final String ssn;               
    String name;

    public Person(String ssn,String name){
        this.ssn=ssn;               //생성자를 통해 final 필드를 초기화
        this.name=name;
    }
}

public class PersonExample{
    public static void main(String[] args) {
        Person p1 = new Person("123456-1234567", "홍길동");

        System.out.println(p1.nation);
        System.out.println(p1.ssn);
        System.out.println(p1.name);
    }
}
```

## 상수

일반적으로 불변하는 값을 상수라고 부르는데, 이러한 불변의 값은 수학에서 사용하는 원주율이나 지구의 무게, 둘레 등이 해당된다.

### 상수의 선언

상수는 객체마다 저장할 필요가 없는 **공용성**을 띠고 있으며, **여러 가지 값**으로 **초기화될 수 없기** 때문에 final과 static 키워드를 사용해서 상수를 선언한다.

```java
static final double PI = 3.14159;
static final double EARTH_RADIUS = 6400;
static final double EARTH_AREA = 4 * Math.PI * EARTH_RADIUS * EARTH_RADIUS;
```
