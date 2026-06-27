6. 23. (수) Mat. Mgmt.

- IT Overview
- SAP
- Enterprise Structure
- Master Data
- Logistics Master Data
  - Material Master: LO-MD-MM
  - Business Partner: LO-MD-BP
  - Bill of Materials: LO-PP-BOM
- MM (Materials Management) - PLURAL

---

# 0. Logistics

## ERP - SD

1. Inquiry
2. Quotation / RFQ (Request for Qt.) (내용이 상이한 수 있음)
   - Material
   - Price
   - Qty
   - Delivery Date

2 1/2. 계약관리 (Outlying Agreement)
- Contract
- Sch. Agr. (납품일자)
- J.I.T.
- Serialisation

<< 하기 3개는 필수 >> -> Order Mgmt. System (OMS)
3. Sales Order (내부용) / Purchase Order (고객 -> 회사)
   - Business Partner
   - Material
   - Price
   - Qty
   - Delivery Date
4. Delivery
   - **Outbound Delivery**
      - 출하 문서
   - **Picking**
      - 완제품 창고에서 출하할 제품/상품을 꺼내옴
   - Packing (Optional)
      - 포장
   - Loading (Optional)
      - 적하 (포장된 제품/상품을 컨테이너 등 운송 장비에 싣)
   - **Goods Issue**
      - 출고 (우리의 손을 떠났음을 기록)
      - 생성되는 문서:
         - Material Doc.: Qty. Chng. -> Plant 실무자가 관심
         - Accounting Doc.: Value Chng. (비용의 증가 (CoGS) \ 재고의 감소) -> 재무팀이 관심
5. Billing / Invoice
- Accounting Doc.: Value Chng. (매출채권 증가 \ 수익 증가) -> 재무팀이 관심

# **The account-based SAP applications store credit balances (revenue, liabilities and owner’s equity) with NEGATIVE signs in the data basis!!!!!**

### 생산전략

- Make to Stock (MTS): 재고생산
- Make to Order (MTO): 수주생산

---

## PP

- 0-1. Forecasting (Input)
   - Make to Stock: 재고생산
- 0-2. Sales Order (Input)
   - Make to Order: 수주생산

1. Master Planning (MP, 기준생산계획)
   - FERT only
2. Material Requirement Planning (MRP, 자재소요량계획)
   - BoM에 의거
   2-1. 반제품(HALB) 및 원자재(ROH) 재고수량 파악
3. Planned Order
   - Material
   - Qty
   - Date

   자재유형 (Material Type)
   - ROH → Purchase Requisition
   - HAWA → Purchase Requisition
   - HALB → Production Order
   - FERT → Production Order

(/omm03 MRP-II View 내 Procurement Type이 F인 경우) -> PUR

(/omm03 MRP-II View 내 Procurement Type이 E인 경우)
4. Production Order

5. 실적



---

## MM - PUR

1. Purchase Requisition
2. Request for Quotation / Quotation
**3. Purchase Order**
- 법적 구속력이 있음.
- 상법상 5년 보관 의무가 있음.
4. Goods Receipt / Inbound Delivery
5. Logistics Invoice Verification

PO: Material, Price, Qty
GR: Material, Qty → Material Document
Invoice: Material, Price

상기 3자를 비교

---

## MM - IM (Inventory Mgmt.)

- Goods Receipt (입고) for...
   - Purchcase Order (구매입고) - 101F
   - Production Order (생산입고) - 101E
- Issue (출고) / Comsumption (예- 상위 자재가 됨)
- Transfer Posting (이전 전기) - Status Chng.
- Stock Transfer (재고 이전) - Physical Chng.
- Physical Inventory (재고조사)
  - Closed: 폐창식
  - Open: 개창식

---

## WM (Warehouse Mgmt.) 창고관리

非필수 모듈

- QM (Quality Mgmt.): 품질관리
- PM (Plant Maintenance): 설비관리

관련 모듈: MM / PP / SD



## 물(物)과 재(財), 인(人)의 통합

- Business Transaction
  - Accounting Transaction
    - Dr / Cr
    - 자산(Asset) / 부채·자본(Capital)
    - 손익(Profit/Loss) / 비용(Expenses) / 수익(Revenues)
  - Accounting Doc.: 회계문서 Val.
- Material Doc.: 자재문서 Qty.

### Automatic Account Assignment 자동계정전정

"자재문서가 회계적으로 의미 있는 경우 회계문서를 자동 생성"

# **"S.A.P. is an Integrated System !!!!!" - K. Nam, 2026.**

→ SSOT (Single Source of Truth)

---

# 1. Materials Mgmt.

## MM의 6요소 - Material Mgmt.'s Component

- Master Data
- Consumption Based Planning (ReOrder Point, ROP에 의거)
- Purchasing
- Service
- Inventory Management
- Logistics Invoice Verification

### ReOrder Point (ROP)

예) 10일 ↓ Ø 주문후 3일

| 일자 | 1 | 2 | 3 | 4 | 5 | 6 -> 보험차원 하루 추가하여 이때 주문 | 7 | 8 | 9 | 10 |11|
|------|---|---|---|---|---|---|---|---|---|---|---|
| 재고 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 11 |10|


---

# 참고 - 전사기준정보 / 모듈기준정보

## 전사기준정보

- Material Master
- Customer → Business Partner
- Vendor → Business Partner
- Employee

## 모듈기준정보

MM:
- Info Record
- Source List
- Quota Arrangement

---

## 자재특성

- Stock Material
- Consumable → 재고관리 안함