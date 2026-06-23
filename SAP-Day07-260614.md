# 6. 14. 일 B.P. Hands-On

- /obp → Organisation
- /oxk01.

## Material Master

-> Client.

## Vendor

### Acct. Mgmt.

- Reconciliation Acct. 조정계정
  - Payable Lcl. / Overseas
### Payment. Trans.
- Terms of Payment.
  - 대금지급조건
  - 결제조건
### Correspondence
- Dunning → 돈 달라고 통보

### Status

- Posting Block - 거래정지
- Deleting Block - 삭제 Flag.

BP 10000656

---

# 3. PUR → GR → IR → AP

## PUR: PO

설계
- Mat.
- Qty
- Price

## GR: 입고

받아라
- Mat.
- Qty

## IR: 송장

돈줘
- Max
- Qty.
- Price

### LIV
송장검증

## AP : 매입채무

--

## MD-MM

- Basic: MARA
- Acct.: MBEW
- MRP: MARC
- Sales: MVKE

ZA123HALB01

## MD-BP

- General: 000000
- Supp. FI: FLVN00

10000656

# 권한관리
개별 부여에서 role식 일괄부여형태
---

# BOM (Bill of Material) 자재명세서

/ocs01

- 자재
- 설비
- 영업

* Usage
* Tech. Type
* Item Cat.

Alt BOM - 자재상황변경시.

## BOM 종류

1. 설계 BOM
2. Test BOM
3. Production (양산) BOM
4. 설계 BDM
5. 영업 BOM

| \ | 개별가 | 합계가 |
|---|---|---|
|ERLA | / | o |
| LUMF | o | / |

* Phantom Group: 짜잘한 자재를 관리편의를 위해 가상그룹으로 묶음

---

BOM <- Part list
- 위계
-  Qty

---

S.A.P. 화면구조

- Overview
- Header
- Item Detail

---

# Condition Master

- Price
- Discount (-)
- Surcharge (+)
- Tax

- UKM000 → 여신관리

---

# 명령어 정리

- /ocs01 - BOM 생성
- /ocs02 - BOM 변경
- /ocs03 - BOM 조회

- /ocs11 - 단일 레벨 조회
- /ocs12 - 모든 레벨 조회
