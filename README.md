# FAF (For All For) 프로젝트

## 프로젝트 개요
FAF는 프로그래밍 챌린지, 커뮤니티, 마켓플레이스를 제공하는 종합 플랫폼입니다.

## 기술 스택
- **Backend**: Spring Boot, MyBatis, MySQL
- **Frontend**: React, Tailwind CSS
- **Authentication**: Spring Security, OAuth2

## 프로젝트 구조
```
FAF/
├── backend/          # Spring Boot 백엔드
├── frontend/         # React 프론트엔드
└── README.md
```

## 설치 및 실행

### 백엔드 설정
1. `backend/env.example` 파일을 `backend/.env`로 복사
2. `backend/application.properties.example` 파일을 `backend/src/main/resources/application.properties`로 복사
3. 환경 변수 설정:
   ```bash
   # Google OAuth2 설정
   GOOGLE_CLIENT_ID=your_google_client_id
   GOOGLE_CLIENT_SECRET=your_google_client_secret
   
   # 데이터베이스 설정
   DB_HOST=localhost
   DB_PORT=3306
   DB_NAME=fafdb
   DB_USERNAME=your_username
   DB_PASSWORD=your_password
   ```

### 프론트엔드 설정
1. `frontend/env.example` 파일을 `frontend/.env`로 복사
2. 환경 변수 설정:
   ```bash
   REACT_APP_API_BASE_URL=http://localhost:8080/FAF
   ```

### 데이터베이스 설정
1. MySQL 데이터베이스 생성
2. `backend/fafdb.sql` 파일 실행하여 테이블 생성

### 실행
```bash
# 백엔드 실행
cd backend
./mvnw spring-boot:run

# 프론트엔드 실행
cd frontend
npm install
npm start
```

## 개발 서버
- **백엔드**: http://localhost:8080/FAF
- **프론트엔드**: http://localhost:3000

## 주의사항
- `.env` 파일과 `application.properties` 파일은 절대 커밋하지 마세요
- 개인정보(API 키, 비밀번호 등)는 환경 변수로 관리하세요
- `localhost:8080`은 개발 환경에서만 사용하세요

## 라이선스
이 프로젝트는 MIT 라이선스 하에 배포됩니다.
