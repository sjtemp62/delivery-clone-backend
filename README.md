# 🛵 Delivery Clone Backend (배달 앱 클론 프로젝트)

## 🚀 프로젝트 개요
이 프로젝트는 배달 앱의 핵심 기능을 클론코딩하며 **Spring Boot 백엔드 개발 및 DevOps 환경을 학습**하는 1인 프로젝트입니다.  
실제 배달 플랫폼에서 사용되는 **마이크로서비스 아키텍처, 보안, 메시지 큐, CI/CD 배포, 대규모 데이터베이스 운영** 등을 경험하는 것이 목표입니다.

## 🎯 프로젝트 목표
- **Spring Boot 기반의 RESTful API 설계 및 구현**
- **JPA, JDBC를 활용한 다양한 데이터베이스 연동**
- **Spring Security를 통한 JWT 및 세션 기반 인증**
- **Kafka를 활용한 비동기 메시징 시스템**
- **Redis를 활용한 캐싱 및 세션 관리**
- **Docker & Kubernetes를 활용한 컨테이너 오케스트레이션**
- **Nginx와 로드밸런서를 이용한 트래픽 관리**
- **CI/CD 파이프라인 구축 (GitHub Actions, AWS CodePipeline)**
- **Swagger로 API 문서 자동화**

---

## 📌 버전별 목표
이 프로젝트는 **단계적으로 목표를 확장**하면서, Git Flow를 적용하여 버전별로 관리됩니다.

### **🟢 Version 1.0 (기본 API 구축 - MVP)**
✅ `회원가입 / 로그인 (JWT & 세션)`
✅ `음식점 등록 및 메뉴 관리 (CRUD)`
✅ `사용자가 주문하기 & 결제 모의 구현`
✅ `배달 상태 업데이트 (Redis 활용)`
✅ `Swagger API 문서화`
✅ `MySQL + JPA 연동`
✅ `기본 CI/CD 구축`

🔹 **브랜치 전략**
- `main`: **배포 가능 상태** (1.0 완성 시 merge)
- `develop`: **개발 브랜치** (모든 feature 브랜치 병합)
- `feature/authentication`, `feature/order`, `feature/delivery` 등

---

### **🟡 Version 2.0 (확장 및 최적화)**
✅ `Kafka 기반 비동기 메시지 처리 (배달 요청)`
✅ `Redis 캐싱 적용 (쿼리 최적화)`
✅ `PostgreSQL 연동`
✅ `Swagger 문서 자동 배포`
✅ `Docker 기반 환경 구성`
✅ `Kubernetes 클러스터 설정`

---

### **🔵 Version 3.0 (고급 기능 & 확장)**
✅ `OracleDB 연동 및 멀티DB 지원`
✅ `Nginx 기반 로드밸런서 적용`
✅ `고객센터 실시간 채팅 (WebSocket)`
✅ `AWS S3 기반 이미지 업로드`
✅ `Kubernetes 기반 마이크로서비스 아키텍처 도입`

---

## 🛠️ 기술 스택

### **📌 Backend**
- **Framework**: Spring Boot 3.0
- **ORM**: JPA (Hibernate) & JDBC
- **Security**: Spring Security (JWT + Session)
- **API 문서화**: Swagger 3.0
- **Messaging**: Kafka (배달 요청 비동기 처리)

### **📌 Database**
- **Primary DB**: MySQL → PostgreSQL → OracleDB (버전별로 확장)
- **Caching**: Redis

### **📌 DevOps & CI/CD**
- **Containerization**: Docker + Kubernetes
- **Load Balancing**: Nginx
- **CI/CD**: GitHub Actions + AWS CodePipeline
- **Infrastructure**: AWS EC2, RDS, S3

---

## 📂 프로젝트 구조
delivery-clone-backend/  
 ├── src/  
 │   ├── main/  
 │   │   ├── java/com/example/delivery/  
 │   │   │   ├── controller/   # API 컨트롤러  
 │   │   │   ├── service/      # 비즈니스 로직  
 │   │   │   ├── repository/   # 데이터베이스 (JPA, JDBC)  
 │   │   │   ├── entity/       # 엔티티 (DB 모델)  
 │   │   │   ├── config/       # 설정 파일 (Security, DB, CORS 등)  
 │   │   │   ├── dto/          # 요청/응답 객체  
 │   │   │   ├── exception/    # 예외 처리 (Custom Exception)  
 │   │   │   ├── util/         # 유틸리티 클래스 (JWT, 파일 업로드 등)  
 │   │   ├── resources/  
 │   │   │   ├── static/       # 정적 파일 (Swagger UI, 에러 페이지)  
 │   │   │   ├── templates/    # Thymeleaf 템플릿 (필요할 경우)  
 │   │   │   ├── application.yml  # 환경 설정 파일  
 │   │   │   ├── data.sql      # 초기 데이터 (DB Seed)  
 │   ├── test/java/com/example/delivery/  
 │   │   ├── controller/       # API 테스트 (MockMvc)  
 │   │   ├── service/          # 서비스 레이어 테스트  
 │   │   ├── repository/       # 데이터베이스 테스트  
 ├── .gitignore        # Git 무시 파일  
 ├── README.md         # 프로젝트 문서  
 ├── Dockerfile        # 도커 배포 설정  
 ├── docker-compose.yml # Docker 환경 구성 파일  
 ├── swagger.yaml      # API 문서 (Swagger)  
 ├── scripts/          # 배포 및 설정 스크립트 (shell, SQL)  
 ├── logs/             # 로그 파일 저장 (로컬 테스트용)  
 ├── build.gradle  # 프로젝트 빌드 설정

---

## 🚀 Git Flow 전략
💡 **1인 프로젝트라도 Git Flow를 적용하여 버전별 개발을 체계적으로 관리합니다.**

### **📌 브랜치 전략**
- `main` → **배포 가능 상태** (완전한 버전이 될 때만 머지)
- `develop` → **모든 개발이 모이는 브랜치**
- `feature/xxx` → **각 기능별 개발 브랜치** (예: `feature/authentication`)
- `hotfix/xxx` → **긴급 버그 수정**
- `release/xxx` → **배포 직전 테스트 브랜치**