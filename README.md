# sumtagi-BE

인천 섬 여행 앱 **Sumtagi**의 백엔드 서버입니다.

## 기술 스택

| 분류 | 기술 |
|------|------|
| 프레임워크 | [Next.js 16](https://nextjs.org) (App Router) |
| 언어 | TypeScript 5 |
| 데이터베이스 | [Supabase](https://supabase.com) (PostgreSQL) |
| 인증 | Supabase Auth |
| 배포 | [Vercel](https://vercel.com) |

## 프로젝트 구조

```
sumtagi-be/
├── app/
│   └── api/
│       ├── islands/    # 섬 관련 API
│       ├── users/      # 유저 관련 API
│       └── trips/      # 여행 관련 API
├── lib/
│   └── supabase.ts     # Supabase 클라이언트
└── .env.local          # 환경변수 (로컬 전용)
```

## 시작하기

### 1. 패키지 설치

```bash
npm install
```

### 2. 환경변수 설정

`.env.local` 파일에 Supabase 키를 입력합니다.

```
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
```

> Supabase 키는 프로젝트 Settings → API에서 확인할 수 있습니다.

### 3. 개발 서버 실행

```bash
npm run dev
```

[http://localhost:3000](http://localhost:3000) 에서 확인 가능합니다.

## API 엔드포인트

| Method | 경로 | 설명 |
|--------|------|------|
| GET | `/api/islands` | 섬 목록 조회 |

## 배포

Vercel에 연결 후 환경변수를 동일하게 등록하면 자동 배포됩니다.

```bash
vercel deploy
```
