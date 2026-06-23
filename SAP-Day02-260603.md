# SAP Information Technology & SAP System

## 1. SAP 개요
- SAP의 특징: Client
- Master Data: Transaction을 처리하기 위해서 반복적으로 사용되는 정보
- Change & Transport System (CTS)
- Client간 데이터 옮기기

## 2. System Landscape (3-System Landscape / Transport)

| System | Transport | Client | 내용 |
| :--- | :---: | :--- | :--- |
| **DEV** (개발) | — | CUST, DEVL, UTST, SAND | Customising, Manage master configuration, Write ABAP program, Test data, Unit test, Sandbox |
| **QAS** (품질관리, QA) | transport | QTST, TRAN | Quality Testing, Training |
| **PRD** (운영시스템) | transport | PROD | Operation |

## 3. Data in SAP System

### 3-1. Client-dependent Data (Client-Specific)
- User Master
- Customizing (Process configurations)
- Application
  - Master Data (기준정보)
  - Transaction Data (거래의 기록)

### 3-2. Client-independent Data (Cross-Client)
- Customizing (System configuration, Cross-Client Configuration)
- Repository (ABAP programs, DDic)

## 4. SAP System - Architecture and Processes

### 4-1. 클라이언트
- SAP GUI (DIAG)
- Web Browser (HTTP, HTTPS, SMTP, SOAP, XML, ...)

### 4-2. SAP Web Application Server (SAP Instance)
- Dispatcher
- Queue
- Work Process: 5-1 참조

### 4-3. Database Server (Any DB) --> 현재
- Oracle
- Informix
- DB2
- MS SQL Server
- MAX DB

## 5. Work Process

- SPOOL: Simultaneous Peripheral Operations On-Line
- Enqueue / Dequeue — Locking (OS 학습간 중요)

### 5-1. Work Process Type 표
| Work Process Type | Work Process Code | Use |
| --- | --- | --- |
| Dialog | D (DIA) | Executes dialog programs (ABAP) |
| Background | B (BTC) | Executes time-dependent or event-controlled background jobs |
| Update | V1 (UPD), V2 (UPD2) | Asynchronous database changes (is controlled by a COMMIT WORK statement in a dialog work process) |
| Enqueue | E | Executes locking operations (if SAP transactions have to synchronize themselves) |
| Spool | S (SPO) | Print formatting (to printer, file or database) |

- V (update): sync (V1), async (V2)

### 5-2. SAP Instances 구성
- Dialog Instance: Client Specific
- Central Instance: Cross Client

## 6. 통신 프로토콜 및 마크업
- HTTP, HTTPS, SMTP (e-Mail), SOAP, XML
- SOA = Service Oriented Architecture
- XML = Extensible Mark-up Language
- Heterogeneous System
- SOAP: SOA 상에서 XML형식으로 인터페이스하는 프로토콜
  - 40-60%가 형식 꺽쇠 내용(<>)에 이용되어 비효율
- Markdown <-- Markup
- 마크업 언어

## 7. Transaction Code 및 기타
- /n --> 현재창에서 열기
- /o --> open, 새창에서 열기
- /nex --> exit
- /nsm04 --> 현재 사용자 및 세션
- /nsm50 --> 작업 프로세스 모니터링
- /ose11 --> ABAP Dict.
- /osu3 --> 본인 사용자 프로필 설정

## 8. OSI 7 Layer

| 계층 | 계층 이름 (영문) | 주요 역할 | 전송 단위 (PDU) | 대표 프로토콜 / 장비 |
| :---: | :--- | :--- | :---: | :--- |
| **7** | **응용 계층** (Application Layer) | 사용자가 네트워크에 접근할 수 있도록 인터페이스를 제공하는 계층 | 데이터 (Data) | HTTP, FTP, SMTP, DNS, DHCP |
| **6** | **표현 계층** (Presentation Layer) | 데이터의 형식을 정의하고, 암호화/복호화 및 압축을 수행하는 계층 | 데이터 (Data) | JPEG, MPEG, SSL/TLS, ASCII |
| **5** | **세션 계층** (Session Layer) | 통신 장치 간의 상호작용을 설정, 유지, 동기화 및 종료하는 계층 | 데이터 (Data) | NetBIOS, SSH, TLS |
| **4** | **전송 계층** (Transport Layer) | 송신자와 수신자 간의 신뢰성 있는 데이터 전송을 보장하는 계층 (흐름 제어, 오류 제어) | 세그먼트 (Segment) | TCP, UDP ※ 장비: L4 스위치 |
| **3** | **네트워크 계층** (Network Layer) | 데이터를 목적지까지 가장 안전하고 빠른 경로로 전달하는 계층 (라우팅) | 패킷 (Packet) | IP, ICMP, ARP, BGP ※ 장비: 라우터, L3 스위치, DISPATCHER |
| **2** | **데이터 링크 계층** (Data Link Layer) | 물리적 매체를 통한 이웃 노드 간의 신뢰성 있는 데이터 전송을 보장하는 계층 (MAC 주소 사용) | 프레임 (Frame) | Ethernet, HDLC, PPP ※ 장비: 스위치, 브릿지 |
| **1** | **물리 계층** (Physical Layer) | 데이터를 전기적, 기계적 신호로 변환하여 실제 전송 매체를 통해 비트를 전송하는 계층 | 비트 (Bit) | 케이블 규격, RS-232 ※ 장비: 허브, 리피터, 케이블 |