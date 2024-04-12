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

## sqlMapConfig.xml
★https://mybatis.org/mybatis-3/ko/getting-started.html
![](../image/Pasted%20image%2020240412113619.png)
![](../image/Pasted%20image%2020240412120130.png)
★1번 체크박스 체크(2023-12 IDE eclipse는 체크 해제가 디폴트로 되어 있음음)

### 설명
![](../image/Pasted%20image%2020240412120156.png)
![](../image/Pasted%20image%2020240412121209.png)
![](../image/Pasted%20image%2020240412121902.png)
![](../image/Pasted%20image%2020240412122152.png)


## member.xml
![](../image/Pasted%20image%2020240412122746.png)
★SQL 맵퍼 파일은 루트 앨리먼트 \<mapper>를 작성하는 것으로 시작한다. 프로젝트에서 기본적으로 여러 개의 \<mapper>를 가지기 때문에 중복되는 이름을 가진 SQL문이 존재할 수 있다. 따라서 각 \<mapper>마다 namespace 속성을 이용하여 \<mapper>를 구분한다.


### memberDao_설명
![](../image/Pasted%20image%2020240412123244.png)
![](../image/Pasted%20image%2020240412124926.png)![](../image/Pasted%20image%2020240412140550.png)


## MemberDao (2)
![](../image/Pasted%20image%2020240412142536.png)
★36 : namespace.id 형태. 다음 매개변수로 파라미터를 입력한다
![](../image/Pasted%20image%2020240412143014.png)


### memberDao_설명
![](../image/Pasted%20image%2020240412144020.png)

## MemberDao(3)
![](../image/Pasted%20image%2020240412144404.png)


## member.xml (mapper파일 작)
![](../image/Pasted%20image%2020240412144811.png)
