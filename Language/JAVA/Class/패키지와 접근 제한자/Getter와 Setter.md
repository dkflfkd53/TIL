## Getter와 Setter 메소드

일반적으로 객체 지향 프로그래밍에서는 객체의 **무결성**(결점이 없는 성질)을 지키기 위하여 객체의 필드를 객체 외부에서 직접적으로 접근하는 것을 막습니다.

클래스를 선언할 때는 가능하다면 **필드를 private로 선언**해서 외부로부터 보호하고, 필드에 대한 **Setter와 Getter 메소드를 작성**해서 필드값을 안전하게 변경/사용하는 것이 좋다.

### Setter

OOP에서는 필드에 외부 접근을 막고 매개값을 검증해서 유효한 값만 객체의 필드로 저장할 수 있게 해주는 **메소드로 필드를 변경**하는 방법을 선호하는데, 이러한 역할을 하는 메소드가 Setter이다.

**(자동차의 속도를 메소드를 통해서 변경할 경우 다음처럼 코드를 작성할 수 있다)**

```java
void setSpeed(double speed) {
  if(speed < 0) {
    this.speed = 0;          //매개값이 음수일 경우 speed 필드의 값을 
    return;                  //0으로 저장하고, 메소드 실행 종료
  } else {
    this.speed = speed;
  }
}
```

### Getter

외부에서 객체의 데이터를 읽을 때도 부적절한 필드값의 사용을 막기 위해서 사용하는 메소드가 Getter이다.

**(자동차의 속도를 마일에서 km단위로 바꿔서 외부로 리턴하는 코드는 다음처럼 작성할 수 있다)**

```java
double getSpeed() {
  double km = speed*1.6;            //필드값인 마일을 km 단위로
  return km;                        //환산 후 외부로 리턴
}
```
