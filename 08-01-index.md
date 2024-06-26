# 인덱스

데이터 검색에서 발생하는 비효율적인 데이터 입출력 문제를 해결하기 위한 목적으로 시작 

* 인덱스 : DBMS 에서 요청된 레코드에 빠르게 접근할 수 있도록 지원하는 데이터와 관련된 주가적인 구조
* 인덱싱 : 인덱스를 구성하고 생성하는 작업

## 인덱스의 평가 기준

* 접근 시간 : 데이터를 찾는 데 걸리는 시간
* 유지 비용 : 새로운 데이터 삽입 및 기존 데이터 삭제 연산으로 인한 인덱스 구조 갱신 비용
* 공간 비용 : 인덱스 구조에 의해 사용되는 부가적인 공간비용

## 순서 인덱스

특정 값에 대해 정렬된 순서 구조

탐색키를 정렬하여 해당 탐색키와 탐색키에 대한 레코드와의 인계를 통하여 인덱스 생성

* 밀집 인덱스
* 희소 인덱스
* 다단계 인덱스

인덱스 엔트리 : 레코드에 대한 빠른 접근을 할 수 있는 레이블

### 밀집 인덱스

모든 레코드에 대해 *탐색키 값 : 포인터* 쌍을 유지

### 희소 인덱스

인덱스의 인트리가 일부의 탐색키 값만 유지

### 다단계 인덱스

인덱스에 대한 인덱스를 만드는 방법

밀집 인덱스와 희소 인덱스의 혼용하여 내부 인덱스와 외부 인덱스를 둠

## B+ 트리

트리 구조인데 맨 밑의 노드(단말 노드)들이 연결 리스트 형태로 되어있음

=> 루트 노드로 부터 모든 단말 노드의 경로 길이가 같음

* 순서 인덱스는 파일이 커질수록 데이터 탐색에 있어서 비용이 커지는 문제점을 해결하기 위해 제안
* 상용 DBMS 에서도 널리 사용되는 대표적인 순서 인덱스



