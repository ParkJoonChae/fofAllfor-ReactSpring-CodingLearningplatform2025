# FAF 프로젝트 설정 가이드

## 🚀 빠른 시작

### 1. 환경 변수 파일 설정

#### 백엔드 설정
```bash
# backend/env.example을 backend/.env로 복사
cp backend/env.example backend/.env

# backend/application.properties.example을 backend/src/main/resources/application.properties로 복사
cp backend/application.properties.example backend/src/main/resources/application.properties
```

#### 프론트엔드 설정
```bash
# frontend/env.example을 frontend/.env로 복사
cp frontend/env.example frontend/.env
```

### 2. 환경 변수 값 설정

#### 백엔드 (.env)
```bash
# Google OAuth2 설정
GOOGLE_CLIENT_ID=your_actual_google_client_id
GOOGLE_CLIENT_SECRET=your_actual_google_client_secret

# 데이터베이스 설정
DB_HOST=localhost
DB_PORT=3306
DB_NAME=fafdb
DB_USERNAME=your_actual_username
DB_PASSWORD=your_actual_password

# 이메일 설정
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USERNAME=your_actual_email@gmail.com
EMAIL_PASSWORD=your_actual_app_password
```

#### 프론트엔드 (.env)
```bash
# API 설정
REACT_APP_API_BASE_URL=http://localhost:8080/FAF
REACT_APP_API_TIMEOUT=30000
REACT_APP_LLM_TIMEOUT=120000
```

### 3. 데이터베이스 설정
```sql
-- MySQL에서 실행
CREATE DATABASE fafdb;
USE fafdb;

-- backend/fafdb.sql 파일 실행
source backend/fafdb.sql;
```

## ⚠️ 주의사항

### 절대 커밋하지 말아야 할 파일들
- `backend/.env`
- `frontend/.env`
- `backend/src/main/resources/application.properties`
- `backend/target/`
- `frontend/node_modules/`
- `frontend/build/`

### 환경 변수 관리 원칙
1. **개인정보는 환경 변수로**: API 키, 비밀번호, 데이터베이스 접속 정보
2. **예시 파일 제공**: `*.example` 파일로 설정 방법 안내
3. **기본값 설정**: 개발 환경에서 바로 실행 가능하도록 기본값 제공

## 🔧 개발 환경 실행

### 백엔드 실행
```bash
cd backend
./mvnw spring-boot:run
```

### 프론트엔드 실행
```bash
cd frontend
npm install
npm start
```

## 📱 접속 정보
- **백엔드 API**: http://localhost:8080/FAF
- **프론트엔드**: http://localhost:3000

## 🆘 문제 해결

### 일반적인 문제들
1. **포트 충돌**: 8080 또는 3000 포트가 사용 중인 경우
2. **데이터베이스 연결 실패**: MySQL 서비스 실행 확인
3. **환경 변수 인식 안됨**: 서버 재시작 필요

### 로그 확인
- 백엔드: `backend/logs/` 폴더
- 프론트엔드: 브라우저 개발자 도구 콘솔
