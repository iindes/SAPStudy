# 6.13. 토

## Core Module

- SD : Sales & Dist.
- MM : Materials Mgmt.
- PP : Production Planning
- FI : Fin. Acctg.
- CO : Managerial Acctg.

- QM
- PM : 설비관리
- PS (Project Sys.)
- TR (TReasury) : 자금관리

/nse11

---

## MM

- 01 : 생성
- 02 : 변경
- 03 : 조회 (특정기에)
- 06 : 삭제마크 → 조건 단위로도 가능.
  - Archiving.
    - DB → 외부 저장장치 (CD 등, 감사시 들여다 봄)

### 삭제 안되는 이유

- 기준정보 삭제시 관련된 transaction 조회.
- 법적 보관 기준 충족.
  - 예) 상법 → 세액관련서류 5年.
  - 분식 회계사 SAP 지양해야

---

/mmam → Transaction 미실시 건에 한해 변경 가능
/mm60 → 여러가지 조회

# Business Partner- 기준정보


- Vendor Master
- Customer Master

/obp

### Category

- 자연인
- 조직
- 조합


---

## Customer Master

View
- Gen.
- Sales
- Fin. Acctg.

---

## EA : Enterprise Application

- Vendor (Supplier)
- Customer
  - PLM
  - SRM / ERP / CPM
  - SCM
  - MDM

- SCM
  - SCP
  - SCE (Execution)


## 3대 통합
| MDM | Master Data Mgmt. | Data의 통합 |
|---|---|---|
| EAI | Enterprise Application Interface | Process의 통합 |
| | Portal | People의 통합 |


## Acct Group.

→ Business Partner Grouping.

---

## 수출장려정책 (韓.) : 부가세 면세.

- 수출 완제품 (직수출)
- 수출 완제품 用 반제품 (3견수출)

---

## Partner Function.

- Sold-to Party : 판매처
- Ship-to Party : 인도처 / 납품처
- Bill-to Party : 청구처
- Payer : 지급처

# Vendor Master

## Vendor Master 구성

- 채무단리 / FI - AP
- 구매단리 / MM → PUR

## MM
- PUR : Purchasing 구매
- IM : Inventory Mgm. 저장공간
- LIV: Logistic Invoice Verification 송장검증

## FI
- AP : Accont. Payable 매입채무
- AR : Acct. Receivable 매출채권
- GL : General Ledger 총계정원장 Book

- CoA : Chart of Account 계정리부표

→ View.
- 일반
- 구매조직
- 회사코드

→ Copy From. (With Ref.)
(FLCU / FLUN only)
