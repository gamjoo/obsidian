![](../image/Pasted%20image%2020240412090917.png)
★select 에서만 resultType 속성이 존재한다.

# 퍼시스턴스 프레임워크 (Persistence framework)
![](../image/Pasted%20image%2020240412090941.png)
![](../image/Pasted%20image%2020240412091021.png)
★퍼시스턴스(Persistence) : 데이터의 지속성. 애플리케이션을 종료하고 다시 실행하더라도 이전에 저장한 데이터를 다시 불러올 수 있는 기술.
★프레임워크(Framework) : 라이브러리가 개발에 필요한 도구들을 단순히 나열해 놓은 것이라면, 프레임워크는 동작에 필요한 구조를 어느 정도 완성해 놓은 반제품 형태의 도구.
![](../image/Pasted%20image%2020240412091130.png)
★SQL맵퍼(mapper) : SQL 문장으로 직접 DB 데이터를 다룬다. eg)mybatis
★객체 관계 맵퍼(Object-Relational mapper) : 자바 객체를 통해 간접적으로 DB데이터를 다룬다. eg)하이버네이트(Hibernate)와 탑링크(TopLink)
- 프레임워크에서 제공하는 API 전용 객체 질의어를 사용하여 데이터를 다룬다.
![](../image/Pasted%20image%2020240412091236.png)
★mybatis
- 퍼시스턴스 프레임워크의 일종
- 자바 메서드와 SQL문을 연결하는 SQL 매핑 프레임워크
- JDBC 코드를 캡슐화하여 DB 프로그래밍을 단순화 시킴
- 자바 소스에서 SQL을 분리하여 관리함
- SQL을 개발자가 직접 제어 -> DBMS의 고유기능 사용 -> 최적
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


## member.xml (mapper파일 작성)
![](../image/Pasted%20image%2020240412144811.png)
![](../image/Pasted%20image%2020240412150555.png)
![](../image/Pasted%20image%2020240412151435.png)


## LoginProAction.java
![](../image/Pasted%20image%2020240412160630.png)
(시험문제) HttpServletResponse
(시험문제) request.getParameter("")
![](../image/Pasted%20image%2020240412161449.png)


## LogoutAction.java
![](../image/Pasted%20image%2020240412163745.png)
(시험문제)session.invalidate( )


## ListAction.java
![](../image/Pasted%20image%2020240412164457.png)

## List\<Member> list( )
![](../image/Pasted%20image%2020240412164956.png)


## member.xml
![](../image/Pasted%20image%2020240412170430.png)
★id="list"


## list.jsp
![](../image/Pasted%20image%2020240412172143.png)
![](../image/Pasted%20image%2020240412173746.png)
  