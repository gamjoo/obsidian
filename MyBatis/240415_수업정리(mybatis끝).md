★DB 테이블 컬럼명 = DTO 클래스(자바빈)의 프로퍼티
- mybatis 활용 조건
- getter / setter 호출해서 작업했던 것들을 mybatis를 통해 처리하면서 코드가 줄어든다.
★spring 에서는 form태그 name 속성 값 = 테이블 컬럼명 = 프로퍼티
- request.getParameter( )를 사용할 필요가 없어진다!!


# 수정 / 삭제 이어서
![](../image/Pasted%20image%2020240415091744.png)
★data 속성과 script를 활용해서 수정/삭제에 필요한 id값을 다음 페이지로 넘김.
![](../image/Pasted%20image%2020240415091928.png)



## UpdateFormAction.java
![](../image/Pasted%20image%2020240415092257.png)


## UpdateProAction.java
![](../image/Pasted%20image%2020240415095026.png)
★16~18 : 스프링들어가면 이런 코드들이 사라진다.


## MemberDao.java
![](../image/Pasted%20image%2020240415100959.png)
★delete / update


## member.xml
![](../image/Pasted%20image%2020240415101525.png)



## DeleteAction.java
![](../image/Pasted%20image%2020240415102437.png)



# mybatis로 동적쿼리 만들기 (MyBatis2)
![](../image/Image20240415103700.png)
![](../image/Image20240415103646.png)

## NewFile.jsp
![](../image/Pasted%20image%2020240415103848.png)


## FrontController.java
![](../image/Pasted%20image%2020240415110516.png)

## Term.java
![](../image/Pasted%20image%2020240415111122.png)
★DTO 클래스 프로퍼티로 없는 정보는 보통 Map을 이용해서 담는다!!
- ArrayList / Map 중요하다!! 꼭 복습하기

## Emp.java
![](../image/Pasted%20image%2020240415111225.png)


## sqlMapConfig.xml
![](../image/Pasted%20image%2020240415112743.png)


## EmpDAO.java
### getSession( ) 메소드
![](../image/Pasted%20image%2020240415113051.png)

### getTermList( ) 메소드
![](../image/Pasted%20image%2020240415113119.png)


## emp.xml
![](../image/Pasted%20image%2020240415113621.png)
★\<select> 엘리먼트의 resultType 속성은 config(환경설정)에서 type 속성에 대한 alias를 주었기 때문에 emp로 간단하게 쓸 수 있다.


## list1.jsp
![](../image/Pasted%20image%2020240415114238.png)
![](../image/Pasted%20image%2020240415114921.png)



## Newfile2.jsp
![](../image/Pasted%20image%2020240415123451.png)
![](../image/Pasted%20image%2020240415123917.png)


## emp.xml
![](../image/Pasted%20image%2020240415124838.png)
★17 : map과 같이 자주 쓰는 클래스는 프레임워크 내부에서 이미 별칭으로 지정해 둠 -> "java.util.Map" 형식으로 쓰지 않고 "map"으로 별칭을 입력할 수 있다


## NewFile3.jsp
![](../image/Pasted%20image%2020240415142148.png)


## Term3.java
![](../image/Pasted%20image%2020240415143104.png)


## EmpDAO.java
### getTermList3( ) 메소드
![](../image/Pasted%20image%2020240415143856.png)



## emp.xml
![](../image/Pasted%20image%2020240415143938.png)


# checkbox 활용
## Check.jsp
![](../image/Pasted%20image%2020240415150253.png)
![](../image/Pasted%20image%2020240415150850.png)
★checkbox name 속성은 동일해야 한다. getParmeterValues( ) 메소드로 값을 가져오면, String 배열 형태로 저장된다.

## Check.java
![](../image/Pasted%20image%2020240415151107.png)
★checkbox의 경우에는 체크하지 않으면 ""빈문자열이 아니라, null을 반환한다!!!


## EmpDAO.java
![](../image/Pasted%20image%2020240415151628.png)


## emp.xml
![](../image/Pasted%20image%2020240415152259.png)


## list.jsp
![](../image/Pasted%20image%2020240415153139.png)
![](../image/Pasted%20image%2020240415153817.png)


## CheckCount.jsp
![](../image/Pasted%20image%2020240415160227.png)


## EmpDAO.java
### getCount( ) 메소드
![](../image/Pasted%20image%2020240415161122.png)


## emp.xml
### id="deptnocheckcount"
![](../image/Pasted%20image%2020240415161647.png)

## CheckCount.java
![](../image/Pasted%20image%2020240415162444.png)


## listcount.jsp
![](../image/Pasted%20image%2020240415165328.png)
