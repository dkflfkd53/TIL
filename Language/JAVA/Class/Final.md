## Final 필드

final필드란 ‘최종적인 필드’라는 뜻으로 final필드는 초기값이 저장되면 이것이 최종적인 값이 되어서 프로그램 실행 도중에 수정할 수 없다.

 

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
