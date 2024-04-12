# MyBatis
![](../image/Pasted%20image%2020240412090917.png)
★select 에서만 resultType 속성이 존재한다.
![](../image/Pasted%20image%2020240412090941.png)
![](../image/Pasted%20image%2020240412091021.png)
![](../image/Pasted%20image%2020240412091130.png)
![](../image/Pasted%20image%2020240412091236.png)
![](../image/Pasted%20image%2020240412091344.png)


https://mybatis.org/mybatis-3/ko/index.html
![](../image/Pasted%20image%2020240412091855.png)
configuration
![](../image/Pasted%20image%2020240412091824.png)
mapper.. configuration 과 다르다.

https://mvnrepository.com/artifact/org.mybatis/mybatis/3.5.15
![](../image/Pasted%20image%2020240412092059.png)
★maven repisitory에서 관련 라이브러리를 다운 받는다..

![](../image/Pasted%20image%2020240412092152.png)
★3.5.15의 jar 파일
![](../image/240412_Image20240412092211.png)
![](../image/Pasted%20image%2020240412094133.png)

## DTO 클래스(Data Transfer Object)
![](../image/Pasted%20image%2020240412094252.png)
★계층 간(Controller, View, Business Layer) 데이터 교환을 위한 Java Bean을 의미한다. DTO는 로직을 가지지 않는 데이터 객체이고, getter / setter 메소드만 가진 클래스를 의미한다.


## JoinProAction.java
![](../image/Pasted%20image%2020240412112052.png)
★17~18 : 파라미터name / property /  테이블 컬럼 : 3가지가 동일하면 스프링에서는 생략되는 것들이 많아진다.


## MemberDao
![](../image/Pasted%20image%2020240412113332.png)
![](../image/Pasted%20image%2020240412113619.png)
