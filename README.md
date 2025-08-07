# SUBMATE

**SUBMATE**는 각종 OTT 플랫폼의 구독을 함께 원하는 사람들끼리 자동 매칭하고, 대표자(결제자)와 구성원 간의 관계를 효율적으로 관리하여 구독 비용을 절감할 수 있도록 돕는 플랫폼입니다.

---

## 🚀 프로젝트 목적

* 다인 요금제가 존재하는 OTT 플랫폼(예: 라프텔, 넷플릭스 등)의 공동 구독을 간편하게 관리
* 플랫폼 선택, 대기열 등록, 대표자 신청, 그룹 매칭, 비용 안내 기능 포함
* 모바일 환경 중심의 UI 설계 + PWA 확장 고려

---

## 🛠️ 기술 스택

### Frontend

* **Next.js** (React 기반 프레임워크)
* **TypeScript**
* **SCSS Modules** (컴포넌트 단위 스타일링)
* **Zustand** (전역 상태 관리)
* **Firebase Authentication** (이메일 기반 인증)

### Backend

* **NestJS** (TypeScript 기반 서버 프레임워크)
* **Prisma ORM**
* **PostgreSQL** (관계형 데이터베이스)

### Infra & DevOps

* **Vercel** (프론트엔드 배포)
* **Railway** 또는 **Render** (백엔드 배포)
* **Docker** (선택적: 배포 자동화 및 환경 통일)

---

## 📁 디렉토리 구조

```
submate/
├── client/    # 프론트엔드 (Next.js)
└── server/    # 백엔드 (NestJS + Prisma)
```

---

## ⚙️ 개발 및 실행 방법

### 1. 프로젝트 클론

```bash
git clone https://github.com/your-username/submate.git
cd submate
```

### 2. 디렉토리 생성

```bash
mkdir client server
```

### 3. 프론트엔드 설정 (client/)

```bash
cd client
npx create-next-app@latest . --typescript
npm install sass zustand firebase
```

### 4. 백엔드 설정 (server/)

```bash
cd ../server
npm i -g @nestjs/cli
nest new .
npm install @prisma/client
npm install -D prisma
npx prisma init
```

### 5. DB 설정 (Prisma + PostgreSQL)

* `.env`에 `DATABASE_URL` 설정 후 `prisma/schema.prisma` 모델 정의

```bash
npx prisma migrate dev --name init
```

### 6. 실행

* `client/`: `npm run dev`
* `server/`: `npm run start:dev`

---

## 📦 주요 기능 (1차 MVP)

* [ ] OTT 플랫폼 선택 및 대기열 등록
* [ ] 대표자 신청 여부 설정
* [ ] 자동 그룹 매칭 (정원 충족 시)
* [ ] 그룹 정보 표시 (대표자, 구성원, 비용, 결제일 등)
* [ ] Firebase Auth 기반 사용자 인증

---

## ✍️ 제작자

권지은 (Ji-eun Kwon)
📌 GitHub: [https://github.com/builtkwon](https://github.com/builtkwon)
📌 이메일: (원하는 경우 작성)

---

본 프로젝트는 백엔드/프론트엔드 분리 구조를 갖추고 있으며, 모바일 기반 사용자 경험에 최적화되어 있습니다.
