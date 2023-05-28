## final 클래스

클래스를 선언할 때 final 키워드를 class 앞에 붙이면 이 클래스는 최종적인 클래스가 되므로 상속할 수 없는 클래스가 된다. **즉 final 클래스는 상속 될 수 없다.**

```java
public final class 클래스 { ... }
```

다음 예제는 final로 선언된 Member를 상속해서 VeryImportantPerson을 선언할 수 없음을 보여준다.

```java
public final class Member {
}
```

```java
//Member를 상속할 수 없음.
public class VeryImportantPerson ~~extends Member~~ {
}
```

## final 메소드

메소드를 선언할 때 final 키워드를 붙이면 이 메소드를 최종적인 메소드이므로 재정의할 수 없는 메소드가 된다. **즉 부모 클래스에 선언된 final 메소드는 자식 클래스에서 재정의할 수 없다.**

```java
public final 리턴타입 메소드 ( 매개변수 ) { ... }
```

다음 예제는 Car 클래스에서 final로 선언된 stop() 메소드를 SportsCar 클래스에서 제정의할 수 없음을 보여준다. 

```java
public class Car {
	//필드
	public int speed;
	
	//메소드
	public void speed() { speed += 1; }

	//final 메소드
	public final void stop() {
		System.out.println("차를 멈춤");
		speed = 0;
	}
}
```

```java
public class SportsCar extends Car {
	@Override
	public void speedUp() { speed +=10; }

	//제정의 할 수 없음
	~~@Override~~                                        
	public void stop() {                           
		System.out.println("스포츠카를 멈춤");       
		speed = 0;                                  
	}
}
```
