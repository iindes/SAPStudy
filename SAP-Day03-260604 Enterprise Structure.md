# 6.4. 목. Enterprise Structure (조직구조)

## 1. 재무

### Client
- 조직구조 최상단
- 예) 600 
    - Client - Dependent
        - MARA 첫 Field - MANDT

### Company Code (CoCd / BUKRS)
- 재무제표 작성 단위
    - Company (大)와 대응
- FI의 핵심
- Controlling Area와 1:1 대응

### Controlling Area
- CO (Managerial Acctg.) 의 핵심
- FI — CCtr. Cost Center Acctg.
- 비용집계 CO-CCA
- Profit Center
- CO-PC

### CO-PA (Profitability Anal.)
- CO
- 수익성분석
- Operational Concern (여러 Company Code)

## 2. 물류

- 계획 수립의 단위
- 평가의 단위

### Plant
- 공장, 창고 등
- 저장위치
- **판매 및 생산계획 수립 (Sales & Operation Plan (S&OP)) 의 단위**
- **재고평가 (Valuation) 의 단위**
- 부가세 신고 사업장(Business Place)의 단위

### Purchasing Organization
- MM
- 구매조직설정의 3개층위 (전사적, CoCd, Plant)
    - Client의 경우 구매전담회사를 둠.
        - MRO (Maintenance 유지보수, Repair 고장수리, Operation 운영)
        - Shipbuilding의 경우 Overhaul (창정비)

### Sales Organisation (SD)
- + 유통채널 - Distribution Channel
- + 제품군 - Product Division
- = SALES AREA

### 여신관리 / 담보
- FI, SD
- 他社와 거래用

### Level 구분
- Client - Level
- CoCd
- Sales Area

/OSPRO - Configuration

### Enterprise Structure
- Ref. 정의
- Ass. 정의 비교

## 2. Material Master 관련 테이블
- MARA - Client (SPART - Division)
- MARC - Plant
- MARD - Storage Loc.

## 3. Plant (T001W)
- 단위 관련
- Val.
- Company Code 단위 평가범위
- **판매 및 생산계획 수립 (Sales & Operation Plan (S&OP)) 의 단위**
- **재고평가 (Valuation) 의 단위**
    - 예하 SLoc서 재고수량 관리 (MARG)
- 부가세 신고 사업장(Business Place)의 단위

## 4. Purchasing Org
- MM
- 여러 CoCd에 연결 가능 = Client
- Plant 別
- MRO
    - Maintenance
    - Repair
    - Operation / Overhaul (조선)

- Buying Power 규모의 경제


## 5. Storage Location
- Material Master
- Qty.
- Trading Goods → 외부 구매

# Overview Diagram: Enterprise Structure

## 구성 요소
- 클라이언트 (Client)
- 회사 (Company)
- 경영단위 (Operating Concern)
- 여신관리영역 (Credit Control Area)
- 회사코드 (Company code)
- 구매조직 (Purchasing Organization)
- 관리회계영역 (Controlling Area)
- 기능영역 (Functional Area)
- 플랜트 (Plant)
- 코스트센터 (Cost Center)
- 손익센터 (Profit Center)
- 출하지점 (Shipping Point)
- 저장위치 (Storage Location)
- 작업장 (Work Center)
- 영업영역 (Sales Area)
- 영업조직 (Sales Organization)
- 유통채널 (Distribution Channel)
- 제품군 (Division)
- 영업사무소 (Sales Office)
- 영업그룹 (Sales Group)

## Legend
- 확정 조직
- 가변 조직
- 1:N
- N:1

# Organizational Unit in each Modules

## FI
- 회사
- 회사코드
- 여신관리영역
- 기능영역

## CO
- 경영단위
- 관리회계영역
- 코스트센터
- 손익센터

## SD
- 영업영역
- 영업조직
- 유통채널
- 제품군
- 영업사무소
- 영업그룹

## MM
- 구매조직
- 출하지점
- 저장위치

## PP
- 플랜트
- 작업장

## 모듈 표기
- CO-PA
- CO
- FI
- FI/SD
- CoA
- MM-PUR
- LE-SHP
- MM-IM/PP/CO-PC
- CO-CCA
- FI-PCA
- CO-PCA
- MM-IM
- SD
- PP