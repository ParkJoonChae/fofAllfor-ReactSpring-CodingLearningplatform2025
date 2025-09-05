# FAF Frontend

## 프로젝트 개요
FAF 프론트엔드는 React 기반의 프로그래밍 학습 플랫폼입니다.

## 기술 스택
- **React**: 19.1.0
- **Tailwind CSS**: 유틸리티 퍼스트 CSS 프레임워크
- **Framer Motion**: 애니메이션 라이브러리
- **Axios**: HTTP 클라이언트

## 설치 및 실행

### 1. 의존성 설치
```bash
npm install
```

### 2. 환경 변수 설정
1. `env.example` 파일을 `.env`로 복사
2. 환경 변수 설정:
   ```bash
   # API 설정
   REACT_APP_API_BASE_URL=http://localhost:8080/FAF
   REACT_APP_API_TIMEOUT=30000
   REACT_APP_LLM_TIMEOUT=120000
   
   # 개발 서버 설정
   REACT_APP_DEV_SERVER_URL=http://localhost:3000
   ```

### 3. 개발 서버 실행
```bash
npm start
```

### 4. 빌드
```bash
npm run build
```

## 개발 서버
- **프론트엔드**: http://localhost:3000

## 주의사항
- `.env` 파일은 절대 커밋하지 마세요
- API 키 등 민감한 정보는 환경 변수로 관리하세요
- `localhost:8080`은 개발 환경에서만 사용하세요

## 라이선스
이 프로젝트는 MIT 라이선스 하에 배포됩니다. 