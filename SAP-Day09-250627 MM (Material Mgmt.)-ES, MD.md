# 6.27. 土 Material Mgmt. - Enterprise Structure, Master Data
# **구매자 기준**

## S&Op (Sales & Operation)

- Operation
  - Op. Planning
- Sales
  - Sales Planning

1年

W1 *
W2 * *
.. * * *
13 * * *
14   * *
...         *
52          *

"13 Wk Rolling Window"

## Material Mgmt. 조직 구성

- Client - 최상위 단위 Table
  - Client-Depend. Table은 첫 Field MANDT
- CoCd
- (Pur. Org.) → Level 선택 유동적. MRO 참조
- Plant
  - S&Op, Valuation의 기준
- Storage Loc
- **Purchasing Group (Buyer)** . New!


---

## MM - Master Data

### 전사기준정보

- Material
  - Classification
- Vendor

### 모듈기준정보

- Info Record
- Source List 공급원목록
- Quote

#### INFO. RECORD - "구매에 필요한 핵심 정보"

- Purchasing Info. Record *
- QM Info Record (품질관리)
- Doc. Info Record

- Price
- Purchasing Condition

##### CONTRACT 납품계약

- Material
- Price
- Qty
→ Outline Agreement / 개괄계약

##### SCHEDULE LINE 납품일정

#### Srce. List 공급원목록
- 공급원 — Vendor
  - 계약 그 자체
  - Supplying Plant. (일감 몰아주기!!)

#### Quota Arrang.

- "Vendor를 분산하는 행위"
e. g.
- A 社 6
- B 社 3
- C 社 1
v.
Sole Vendor 단일공급업체 (위험)

---

## Vendor

- General
- CoCd
- Purchasing

/ome 구매
mm 제2
mr LIV
  - Logistics
  - Invoice
  - Veri.

<<숫자 첫자리>>
| 번호 | 내용 |
|------|------|
| 0 | Src. |
| 1 | Info. |
| 2 | PO |
| 3/4 | 계약 |
| 5 | PR |

<<숫자 두번째자리>>
  - 1 생성
  - 2 수정
  - 3 조회

## Srce List

/ome11