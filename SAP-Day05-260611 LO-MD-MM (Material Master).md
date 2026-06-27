# 6. 11. 木. Material Master (전사기준정보 가운데 하나)

## 자재 구성 요소

- 자재 Type
- 자재 View (부서별)
- 자재 Description -> 단일 D/B (SSoT)
- Doc. Mgmt.

---

## 자재 View

기본데이터 - 부서별 View 차이 없음

- Purchasing (E) → ~POrg~ → Plant
  - 구매조직설정의 3개층위 (전사적, CoCd, Plant) 가운데 가장 낮은 층위.
- MRP (D) → Plant
- Accounting (B) → Valuation area (평가영역) -> Plant
  - Valuation area: CoCd 내지 Plant Lv.
  - PP (Production Planning), IS-R(Industry Soln.-Retail) 를 사용하는 경우, Val. Area가 Plant로 해야 함.
- Work Scheduling (A) → Plant
- Storage loc. Stock (Z) → SLoc
- et cetera...

### Sales

Sales Area
- Sales Org.
- Dist. Channel (영업 조직 / 유통 채널 / 제품군)
- Division
  - Material Master
    - General View: MARA-SPART
    - Sales View

### View와 조직구조

- Client - Basic view.
- Plant
  - Purchasing
  - Accounting (Valuation)
  - Work Scheduling
  - MRP
- Storage loc
  - S. Loc. Stock. (수량)

---
### Material Master와 Table구조

| View | Organisation Unit | Tables | Memo |
|---|---|---|---|
| Basic | Client | MARA ||
| Purchasing | Plant | MARC ||
| MRP | Plant | MARC ||
| Work Scheduling | Plant | MARC ||
| Storage Loc. Stock | SLoc | MARD ||
| Sales-SOrg | Sales Org., Dist. Channel | MVKE |영업 관련 정보 관리|
| Sales-Plant | Plant | MARC |출하 관련 정보 관리|
| Acctg. | Plant | MBEW |MARC 아님 !|

* Table 찾는법: F1 -> Tech. Info. (렌치 Icon)

---

# 자재 Master의 생성

- Industry Sector
- Material Type 을 지정.

- Material Type (자재유형)

(예)
- FERT - 완제품
- HALB - 반제품
- ROH - 원자재

- HAWA - 상품
- DIEN - 용역

※ 제품 = 만들어 팜 / 상품 = 띠다 팜.

### 자재유형 비교표

|  | 수량 | 가액 |
|--|------|------|
| NLAG 비재고상품 | / | O | 나사 |
| UNBW 비평가상품 | O | / | 반품물량 |

※ Pipeline 관리. (화학기업)

| SLOC. | 물류부서 |
| Plant | 회계부서 |
| 자재문서 | 회계문서 |
| Material Doc | Acctg. Doc |

### 자재유형

자재 유형에 따라 결정되는 것:
- View
- 필드 속성
- Number Range → External 유의미/ Internal 단순순서
  - Classification 분류
- 구매유형 Procurement Type

### 자재 Master의 용처

- 기본 표 필드
- Transaction 영향
- 생산계획 연계.



---

# 자재 View 상세 (Page 3)

## Base Unit of Measure
UoM

- Carton
- Crate
- Palette

SKU # (Stock Keeping Unit)
- EA (Each) - 개
- PC (Piece)

## Basic View

- Division
- Item Cat. Group
- Gross Wt.

Division (전체) → Group
- Porsche / VW / Skoda / ... -> VW Group

## Acctg. View

Valuation Class (Val Cl.)

## Classification View

Internal Number Range시 이용

- Material / (P.R.T.) 등 분류.



※ BOM : 제품 내 하위 구조도

Explode : (≈ Collapse).
