![[Pasted image 20240218225938.png]]
![[Pasted image 20240218225944.png]]
![[Pasted image 20240218230111.png]]
★main 메소드에서 선언된 str 과 change 메소드의 매개변수(지역변수) str
![[Pasted image 20240218230224.png]]
★새로운 문자열의 주소가 변수 str에 저장된다.
![[Pasted image 20240218230635.png]]
![[Pasted image 20240218230810.png]]
★change 메소드가 종료되면 작업에 사용하던 메모리를 반환하므로 change 메소드의 지역변수인 str역시 메모리에서 제거된다.
★문자열 ABC123456 은 참조하는 변수가 하나도 없으므로 적절한 시기에 가비지컬렉터에 의해 제거된다
```java
public class Exercise6_16 {
	public static void change(String str) {
		str += "456";
		System.out.println(str);
	}
	
	public static void main(String[] args) {
		
		String str = "ABC123";
		System.out.println(str);
		change(str);
		System.out.println("After change:" + str);
	}
}
```
![[Pasted image 20240218231340.png]]
★메인 메소드의 str 변수 / change 메소드의 str 변수 둘 다 지역변수지만 서로 다른 변수임. call stack 영역을 잘 생각해보자.

