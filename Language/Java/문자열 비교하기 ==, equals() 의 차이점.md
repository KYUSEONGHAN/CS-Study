![]()

## JAVA에서의 데이터(값) 비교
- 자바에서 Int와 boolean과 같은 일반적인 데이터 타입의 비교는 == 이라는 연산자를 사용하여 비교한다.
- 하지만 String처럼 Class의 값을 비교할때는 ==이 아닌 equals()라는 메소드를 사용하여 비교한다.
- 두 비교방식에는 어떤 차이점이 있을까?

## String 변수 생성시 주소할당
- String 변수를 생성할때는 두 가지 방법이 있다.
    - 리터럴을 이용한 방식
    - new 연산자를 이용한 방식
- 리터럴을 사용하게 되면 string constant pool이라는 영역에 존재하게 되고
- new를 통해 string을 생성하면 Heap 영역에 존재하게 된다.
```javascript
String str1 = "apple"; //리터럴을 이용한 방식
String str2 = "apple"; //리터럴을 이용한 방식
String str3 = new String("example"); //new 연산자를 이용한 방식
String str4 = new String("example"); //new 연산자를 이용한 방식
```
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcAbQYM%2Fbtrm3PpaEN2%2FAuIXpphooR5Q2KuPDYf5JK%2Fimg.png)

## 주소값 비교(==)와 값 비교(equals)
- == 연산자는 비교하고자 하는 두개의 대상의 주소값을 비교하는데 반해
- String클래스의 equals 메소드는 비교하고자 하는 두 개의 대상의 값 자체를 비교한다는 것이다.
- String은 일반적인 타입이 아니라 클래스이다.
- 클래스는 기본적으로 call by Reference 형태로 생성 시 주소값이 부여된다.
- 그렇기에 string 타입을 선언했을때는 같은 값을 부여하더라도 서로간의 주소값이 다르다.
```js
public class compare {
    public static void main(String[] args) {
        String s1 = "abcd";
        String s2 = new String("abcd");
		
        if(s1 == s2) {
            System.out.println("두개의 값이 같습니다.");
        }else {
            System.out.println("두개의 값이 같지 않습니다.");
        }
    }
}
```
- 위 는 두개의 값이 같지 않다는게 출력됨.

```js
public class compare {
    public static void main(String[] args) {
        String s1 = "abcd";
        String s2 = new String("abcd");
		
        if(s1.equals(s2)) {
            System.out.println("두개의 값이 같습니다.");
        }else {
            System.out.println("두개의 값이 같지 않습니다.");
        }
    }
}
```
- 위 에서는 값이 같다고 출력됨.
- equals는 두 비교대상의 주소 값이 아닌 데이터값을 비교하기 때문에 정확한 비교가 가능.

## 참고자료 출처
[https://coding-factory.tistory.com/536](https://coding-factory.tistory.com/536)