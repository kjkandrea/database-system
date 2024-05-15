# 관계형 모델

## 논리적 데이터 모델링 단계

DBMS 에서 사용하는 데이터 모델에 맞추어 데이터를 표현하는 과정

## 릴레이션의 특징

* 레코드의 유일성 : 중복된 레코드 존재 불가능
* 레코드의 무순서성 : 레코드의 순서가 의미 없음
* 컬럼의 무순서성 : 컬럼은 순서가 없고, 이름과 값의 쌍
* 컬럼값의 원자성 : 모든 값들은 나눌 수 없는, 단 하나의 의미

### 키 (Key)

* 유일성 (Uniqueness)
* 최소성 (Irreducibility) : 더이상 축소할 수 없음

#### 키의 종류

* 수퍼키 (super key) : 유일성 만족
* 후보키 (candidate key) : 유일성, 최소성 만족
* 기본키 (PK; Primary key) : 레코드의 구분을 위해 선택된 후보키
* 외래키 (FK; foreign key) : 참조된 다른 릴레이션의 기본키

### 관계형 모델의 제약조건

* 영역 제약 조건 : 컴럼에 정의된 영역(domain)이 요구하는 값으로만 컬럼 값이 결정
* 키 제약 조건 : 키는 레코드를 구별하는 값으로 구성. 키 컬럼값 수정 불가
* 개체 무결성 제약조건 : 어떠한 기본키 값도 널(null)이 될 수 없음
* 참조 무결성 제약조건 : 반드시 존재하는 레코드의 기본키만 참조 가능

### 널(Null) 의 개념

'없음' 또는 '0'이 아닌 미지의 값에 대한 표현

* 입력된 적이 없는 값
* 적용 불가능한 값

## 논리적 데이터 모델링

* RDBMS의 구현 모델에 맞추어 데이터의 구조와 관계를 표현
* 작성된 ERD를 RDBMS 가 수용가능한 모델로 변환

## 데이터 연산

### 관계 대수 (relational algebra)

* `σ` : 셀렉트 연산.  
  * 조건에 맞는 레코드들을 추출
* `∏` : 프로젝트 연산
  * 특정 컬럼을 추출
* `∪` : 합집합 연산
* `∩` : 교집합 연산
* `−` : 차집합 연산
* `×` : 카티시언 프로덕트 연산
  * 두 릴레이션에 포함된 레코드 간의 모든 조합을 생성하는 이항 연산자
* `⋈` : 조인 연산
  * 두 릴레이션에서 조건을 만족하는 레코드를 결합한 레코드로 구성된 릴레이션을 생성
* `g` : 집계 함수
  * 사칙연산을 값들의 집합 또는 레코드의 집합에 적용하는 연산


* `∧` : and
* `∨` : or
