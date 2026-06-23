# 6.6. 토


## Meta Data / Master Data / Transaction Data
- Code Key - Value (JSON)
- K, V <->
- ERP = System of Record
  - 기록은 시스템
  - (Busi.) Transac.
- OLTP <-> OLAP 운영
  - 의사결정을 하기 위함
- 자주쓰는 데이터, 동일한 형태로

## XML
- eXtensible Markup Language
- 이기종 I/F (헤테로)
- SOA -> SOAP (Protocol)

## Vendor / Customer
- Vendor
  - General Info - Client 별
  - Company - CoCd 별
  - Purchasing - (Plant 별)
- Customer
  - General
  - CoCd
  - Sales Area (SaOrg. / PDCh)

## Master 항목
- 전사기준정보
    - Material
    - Vendor
    - Customer
    - Employee
    - Chart of Acct.
- -> MDM (Master Data Mgmt.)

- 모듈기준정보 - Bill of Material

## BOM
- 완제품을 만들기 위한 부재들의 목록

---

# Master Data

- FI - Chart of Account 계정과목표
  - General Ledger - (Book)

--- --- ---

# 데이터의 유형 Type of Data
## 분류 Classification

### Code (Meta Data)
- 단위 업무 프로세스에서 동일한 대표 값으로 공유하는 코드 성격의 데이터입니다. 주로 코드 키 code Key와 값 Value로 구성되어 있습니다.
- 예 ) Purchase Group (구매그룹)
  - P01 : 포장자재 구매담당 Buyer
  - P02 : 설비자재 구매담당 Buyer
  - P03 : 사무용품 구매담당 Buyer

### Master Data
- 전사 통합자원관리 시스템 기능을 지원하기 위해 구성되는 데이터의 기준과 업무의 기준이 되는 모든 정보로 각 시스템 및 데이터의 소통을 위해 사전에 정의된 기준을 말합니다. 프로세스가 효과적으로 실행되기 위해서는 Process간에 주고 받는 마스터데이터가 정확성 Accuracy, 신속성 Timeliness, 신뢰성 Reliability, 활용성 Utilization을 지니고 있어야 합니다.
- 예 ) Vendor Master (업체마스터)
  - 11010, OO컨설팅
  - General Information : 업체명, 대표자 정보, 주소, 연락처, 거래 은행정보
  - Company Information : Tax 정보, 은행정보, 지급관련 정보, 조정계정 정보
  - Purchasing Information : 구매관련 데이터, 배송처 및 지급처 정보

### Transaction Data
- Master Data, Code를 이용하여 업무를 실행하였을 때 발생하는 데이터입니다.
- 예 ) Purchase Order (구매 오더)
  - PO : 4500000010
  - Material 정보, Vendor 정보, 수량, 단가, 배송처, 담당 Buyer, 구매조직, 구매유형

---

# 기준정보 Master Data란 무엇인가?
마스터 데이터는 기업 운영의 기준 — 모든 트랜잭션의 출발점

## 기준정보의 정의

### 기업 운영의 절대적 기준
- 기준정보는 기업 운영의 기준점이자, 모든 비즈니스 프로세스를 연결하는 핵심 자산입니다.

### 모든 트랜잭션의 출발점
- 구매, 생산, 판매 등 모든 비즈니스 거래는 마스터 데이터에서 시작됩니다.
- 마스터 데이터 - 구매 / 생산 / 판매

## SAP 기준정보는

### SAP 핵심 프로세스와 연계
- SAP 마스터 데이터는 SAP 표준 데이터 모델, 권한, 검증 로직, 워크플로우, 감사체계와 결합되어 데이터 정합성과 신뢰성을 보장합니다.

### 풍부한 비즈니스 컨텍스트(Context)
- SAP 마스터 데이터는 구매, 생산, 판매, 재무 등 전사 핵심 프로세스의 실행에 기준으로 사용되는 트랜잭션과 직접 연결되어 있습니다.

## 미래 가치

### AI 시대를 위한 필수 연료
- SAP 기준정보
- SAP 마스터 데이터는 신뢰성과 일관성이 검증된 고품질 데이터로, AI 기반 비즈니스 인사이트 도출에 최적화된 데이터 자산입니다.

---

# 기준정보 Master Data
## What is Master Data?
Master Data is key non-transactional information about your business

### 제품/자재 정보
- 제품/자재 특성, 규격, 중량
- 색상, 모양 등.
- 제품/자재

### 고객 정보
- 고객 이름, 주소
- 전화 번호, 기타 static 정보
- 고객

### 공급업체 정보 공급업체
- 공급업체 이름, 상위조직, 주소
- 전화 번호, 기타 속성정보

### 직원 정보
- 사번, 이름, 직책/직급, 주소
- 부서 등.
- 임직원

### MDM (Master Data Management)
- 제품/자재, 고객, 공급업체, 직원 정보를 연결

---

# 기준정보 Master Data
## 정의 Definition

- Business Transaction에 자주, 동일한 형태로 사용되는 정보로서, 여러 개의 Control Data code; Metadata와 관련 정보를 가지면서 장기간 동일하게 유지되는 Data

### Master Data 란?
- 자신의 고유한 Number를 가지고 Process에 의해 변화하지 않으며 업무수행에 근간이 되는 Data

### 구성 항목
- Material Master 자재
- Vendor Master 공급업체
- Customer Master 고객
- Bill Of Materials 자재명세서
- Chart of Account 계정과목표
- Employee Master 임직원

### 설명
- SAP는 Master data (기준정보)를 기준으로 업무 Process 및 경영 전반적인 계획과 실적을 통합 관리하는 System임
- Master가 부정확 시 경영에 대한 계획 및 실적 관리가 불가능함

---

# 기준정보 Master Data
## 기준정보의 용도 Usage of Master Data

- 여러 문서 (Sales order, Purchase Order, Production Order etc.) 생성, 표준 원가 산정, MRP 수행 등 주요 업무 수행 시 기본값 Default value 등으로 활용함

### 손익 분석 영역
- Customer Master
- 손익 분석 (고객별, 제품별,.)
- 판가
- Margin
- 기타 비용
- 표준 원가
- Gap 분석 보정
- 실적 원가
- Vendor Master

### BOM 영역
- BOM (필요부품, 소요량, 단가)
- 자재비
- LEVEL 0 : 제품
- LEVEL 1 : 반제품
- LEVEL 2 : 자재
- Material Master
- Vendor Master

### Routing 영역
- Routing (작업장, 공정경로, 공수,...)
- 노무비, 경비
- Op.10 / Op.20
- 원료1, 원료2
- W/C 1, W/C 2, W/C
- 제품
- Work Center
- W/C 20 / W/C10
- BD, SM, AN, PBL, ABS

### 계획 영역
- 판매계획
- 주문입력
- MRP
- 생산 계획
- 구매발주

---

# 기준정보 Master Data
## 전사기준정보 General Master Data vs. 모듈 기준정보 Module Master Data

- Master Data는 모든 Module에서 공통적으로 활용하는 전사기준정보 General Master와 각 Module 단위로 사용하는 모듈 기준정보 Module Master Data로 구분할 수 있음

### (Module) Master Data
- MM
  - (Purchasing) Info Record
  - Source List
  - Quota Arrangement
  - Service Master
- SD
  - Price Condition
  - Credit Master
  - Customer-Material Info Record
- PP
  - BOM
  - Routing
  - Work center
- PM
  - Functional Location
  - Equipment
  - BOM
- QM
  - Catalog(Code Group)
  - Selected Set
  - Inspection Characteristic
  - Class Characteristic
  - Inspection Method

### General Master Data
- Material
- Customer
- Vendor