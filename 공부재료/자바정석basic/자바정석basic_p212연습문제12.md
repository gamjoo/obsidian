![[Pasted image 20240218212245.png]]
★클래스변수는 클래스가 처음 메모리에 로딩될 때 자동 초기화되므로 인스턴스 변수보다 먼저 초기화 된다.
★생성자는 초기화 블록이 수행된 다음에 수행된다.

# 초기화 블록(initialization block)
★클래스 초기화 블록 : 클래스 변수의 복잡한 초기화에 사용된다
★인스턴스 초기화 블록 : 인스턴스 변수의 복잡한 초기화에 사용된다

```java
public class Ex6_14 {
	static {
		System.out.println("static {}");
	}
	
	{
		System.out.println("{}");
	}
	
	public Ex6_14() {
		System.out.println("생성자");
	}
	
	public static void main(String[] args) {
		System.out.println("Ex6_14 bt = new Ex6_14(); ");
		Ex6_14 bt = new Ex6_14();
		
		System.out.println("Ex6_14 bt2 = new Ex6_14(); ");
		Ex6_14 bt2 = new Ex6_14();
	}
}
```
![[Pasted image 20240218215812.png]]
★위 프로그램이 실행되면서 Ex6_14 클래스가 메모리에 로딩될 때 (1)클래스 초기화 블록이 가장 먼저 수행되어 static{ } 화면에 출력된다. -> (2) 그 다음에 main 메소드가 수행되어 -> Ex6_14의 인스턴스가 생성되면서 (3)인스턴스 초기화 블록이 먼저 수행되고, -> (4) 끝으로 생성자가 수행된다.
★클래스 초기화 블록은 처음 메모리에 로딩될 때 한번만 수행되었지만, 인스턴스 초기화 블록은 인스턴스가 생성될 때마다 수행된다.

