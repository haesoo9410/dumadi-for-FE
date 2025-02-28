# 🐼 데이터베이스

### DB

- DB(데이터베이스)는 데이터의 집합을 의미합니다.
- DBMS는 이러한 데이터베이스를 관리해주는 소프트웨어입니다.

### RDB

- RDB는 관계형 데이터베이스를 의미하며 데이터베이스간 관계를 맺고 있습니다.
- 2차원 테이블 형태로 표현되며 테이블 간 Join이 가능합니다.

### NoSQL

- 관계를 정의하지 않아 Join이 불가능 하지만 RDB에 비해 속도가 빠릅니다.
- 대표적으로 키벨류 데이터베이스, 다큐먼트 데이터베이스 등이 있습니다.

### DB Normalization

- DB정규화는 테이블을 정규형이라고 불리는 형태에 부합하도록 만들어 가는 것을 의미합니다.
- 테이블이 잘 만들어졌는지 확인하고 고쳐나가는 과정입니다.

### 제 1 정규화

- 테이블의 칼럼이 원자값을 갖도록 테이블을 분해합니다.
- 즉, 속성 하나는 하나의 속성값만을 가져야 합니다.

### 제 2 정규화

- 제 1 정규화를 진행한 테이블에 대해 완전함수 종속을 만족하도록 테이블을 분해합니다.
- 기본키의 부분집합이 결정자가 되어서는 안된다는 것을 의미합니다.

### 제 3 정규화

- 제 2 정규화를 진행한 테이블에 대해 이행적종속을 없애도록 테이블을 분해합니다.
- A가 B를 결정하고 B가 C를 결정하면 A B , B C 로 분리해야 합니다.

### BCNF 정규화

- 제 3 정규화를 진행한 테이블에 대해 모든 결정자가 후보키가 되도록 테이블을 분해합니다.
- 복합키가 기본키로 사용되어 특정 칼럼을 결정할 경우, 그 칼럼이 복합키 중 일부를 결정하는 결정자라면 분리합니다.

### JOIN

- 관계형 데이터베이스에서 둘 이상의 테이블을 연결하여 데이터를 검색하는 것을 의미합니다.
- 적어도 하나의 칼럼을 공유하고 있어야 합니다.

### INDEX

- 추가적인 공간을 활용하여 테이블 검색속도를 향상시키는 자료구조로 주로 B-Tree 계열을 활용합니다.
- 항상 최신의 정렬 상태로 유지해야 하므로 삽입 삭제 업데이트가 자주 일어나면 부적합합니다.

### INDEX에서 해시테이블을 쓰지 않는이유

- 해시는 단 하나의 데이터를 찾을 때는 상수복잡도로 빠를 수 있습니다.
- 하지만 테이블에서 부등호와 같은 조건으로 여러 값을 찾을 경우 정렬되어 있지 않는 구조는 비효율적입니다.
