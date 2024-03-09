![[240117_과제.txt]]
# \[1번]
CREATE TABLE PARENT (
	ID VARCHAR2(20) PRIMARY KEY,
	PASSWORD VARCHAR2(12) NOT NULL,
	NAME VARCHAR2(10) NOT NULL,
	BIRTHDAY DATE NOT NULL
);

# \[2번]
CREATE TABLE CHILD (
	ID VARCHAR2(20) REFERENCES PARENT(ID),
	ADDRESS VARCHAR2(20) DEFAULT '서울시',
	GENDER VARCHAR2(2) CHECK(GENDER IN('남','여'))
);

# \[3번]
insert into parent values('abcd','1234','홍길동','88/7/23');
ALTER TABLE PARENT
MODIFY NAME VARCHAR2(12);
insert into parent values('bbbb','5678','신사임당','85/11/01');

insert into parent values('abcd', '1234', '홍길동', '88/07/23');
insert into parent values('bbbb', '5678', '신사임당', '85/11/01');
insert into parent values('cccc', '90as', '성춘향', '93/12/15');
insert into parent values('dddd', 'efgy', '리카엘', '82/05/01');
insert into parent values('ffff', 'wjdgml', '김풍', '85/04/08');

ALTER TABLE CHILD
MODIFY GENDER VARCHAR2(3);
insert into child values('abcd','경상북도','남');
insert into child values('cccc','퐁당시','여');
insert into child values('dddd','불가리아','남');
insert into child values('ffff','제주시','남');
insert into child values('bbbb','기품시','여');
insert into child values('ffff,'제주시','남');


# \[4번]
select constraint_name, constraint_type, table_name, search_condition, R_CONSTRAINT_NAME
from USER_CONSTRAINTS NATURAL JOIN USER_CONS_COLUMNS
where table_name in ('PARENT', 'CHILD')
ORDER BY TABLE_NAME DESC;

# \[5번]
select TABLE_NAME, CONSTRAINT_NAME, COLUMN_NAME
from USER_CONS_COLUMNS
where table_name in ('PARENT', 'CHILD')
ORDER BY CONSTRAINT_NAME;

# \[6번]
DROP TABLE CHILD PURGY;
DROP TABLE PARENT PURGY;
![[Pasted image 20240206083721.png]]
★참조 관계에서 자식 먼저 지우고, 부모를 지워야 한다. 부모 먼저 지우면 에러
★또 다른 해결법 :
DROP TABLE 부모테이블이름 CASCADE CONSTRAINTS;
부모테이블에서 삭제할 때 자신의 기본키나 고유키를 참조하고 있는 테이블의 제약조건을 삭제하고 테이블을 삭제하는 방법. 즉, 자식테이블의 외래키 설정 제약조건이 삭제된다.

# \[7번] - 못 풂
## CROSS JOIN
SELECT TABLE_NAME, CONSTRAINT_NAME, CONSTRAINT_TYPE, R_CONSTRAINT_NAME, SEARCH_CONDITION							
FROM USER_CONSTRAINTS							
WHERE TABLE_NAME IN('EMP','DEPT')

SELECT *			
FROM USER_CONS_COLUMNS			
WHERE TABLE_NAME IN('EMP','DEPT')

COL "자식테이블" FORMAT A20
COL "외래키" FORMAT A20
COL "부모테이블" FORMAT A20
COL "부모키" FORMAT A20

SELECT CHILD.TABLE_NAME “자식테이블”, CHILD.COLUMN_NAME “외래키”, PARENT.TABLE_NAME “부모테이블”, PARENT.COLUMN_NAME “부모키”
from USER_CONSTRAINTS UC, USER_CONS_COLUMNS PARENT, USER_CONS_COLUMNS CHILD
where UC.CONSTRAINT_NAME=CHILD.CONSTRAINT_NAME
AND UC.R_CONSTRAINT_NAME=PARENT.CONSTRAINT_NAME

## ANSI JOIN [[240118_과제#^d98f53|링크:240118과제 참고하기]]
