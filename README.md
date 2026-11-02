<div align="center">
  <h1>이동훈 | Donghun Lee</h1>
  <p>Frontend Developer</p>
  <p><strong>요청이 실패해도 멈추지 않는 화면과,<br/>프레임 단위 상호작용의 state/ref 경계를 설계합니다.</strong></p>

  <a href="https://github.com/Donghunn-Lee"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/></a>&nbsp;<a href="https://velog.io/@dh82680"><img src="https://img.shields.io/badge/Velog-20C997?style=flat-square&logo=velog&logoColor=white"/></a>&nbsp;<a href="mailto:dh82680@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white"/></a>
</div>

<br/>

## About

- 외부 데이터에 의존하는 조회형 서비스(SlateKR)와 프레임 단위 상호작용 프로젝트(AimTest)를 각각 1인 개발로 마쳤습니다.
- 조사 · 코드 생성에 AI를 활용하되 설계 · 검증 · 판단은 직접 합니다. 작업은 세션 단위로 문서화해, 어떤 변경이든 당시의 판단 과정을 추적할 수 있도록 해왔습니다.

---

## Skills

| | |
|---|---|
| **Frontend** | <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/Next.js_(App_Router)-000000?style=flat-square&logo=next.js&logoColor=white"/> <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white"/> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white"/> |
| **Styling** | <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white"/> <img src="https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white"/> <img src="https://img.shields.io/badge/framer--motion-0055FF?style=flat-square&logo=framer&logoColor=white"/> |
| **Data · State** | <img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=flat-square&logo=reactquery&logoColor=white"/> <img src="https://img.shields.io/badge/Zustand-443E38?style=flat-square&logo=react&logoColor=white"/> <img src="https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white"/> |
| **Backend · Infra** | <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white"/> <img src="https://img.shields.io/badge/Neon_PostgreSQL-00E599?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"/> |
| **Quality** | <img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white"/> <img src="https://img.shields.io/badge/ESLint-4B32C3?style=flat-square&logo=eslint&logoColor=white"/> <img src="https://img.shields.io/badge/Prettier-F7B93E?style=flat-square&logo=prettier&logoColor=black"/> |

---

## Projects

### [SlateKR](https://github.com/Donghunn-Lee/slate-kr) — 국내 상장 종목 가격 · 재무 · 공시 조회 웹앱

개인 프로젝트 · 2026.04 ~ 2026.10 &nbsp;|&nbsp; [Live](https://slate-kr.vercel.app) · [GitHub](https://github.com/Donghunn-Lee/slate-kr)

<img width="800" alt="SlateKR 홈" src="https://github.com/Donghunn-Lee/slate-kr/raw/main/docs/images/hero.png" />

약 2,650개 종목과 국내 · 해외 지수 12개를 다루는 조회 서비스. 데이터가 외부 API 여러 곳에서 오고 장중에 계속 바뀌어, 한 곳이 늦거나 실패해도 화면을 유지하는 것이 과제였습니다.
섹션 단위 Suspense로 loading · empty · error · 부분 실패를 구분 — KIS 3초 지연 주입 시 헤더 표시 3.4초 → 0.3초 · 차트 hover 리렌더 0. 설계 결정은 [README 「한눈에 보기」](https://github.com/Donghunn-Lee/slate-kr#한눈에-보기)에.

`Next.js 16 App Router` `TypeScript` `Tailwind CSS v4` `TanStack Query v5` `Zustand` `Zod` `Neon PostgreSQL` `Vitest`

<br/>

### [AimTest](https://github.com/Donghunn-Lee/aimtest) — 브라우저 1인칭 에임 트레이너

개인 프로젝트 · 2025.03 ~ 05 · 2025.10 ~ 2026.02 · 재정비 2026.10 &nbsp;|&nbsp; [Live](https://fps-aim-test.vercel.app) · [GitHub](https://github.com/Donghunn-Lee/aimtest)

<img width="800" alt="AimTest 인게임" src="https://github.com/user-attachments/assets/50a0ffac-d22a-40ac-9fa1-bb16ae795f9d" />

Pointer Lock으로 마우스 델타를 받아 캔버스 rAF 루프 하나로 그리는 구조에서, 프레임마다 바뀌는 값을 어디까지 React 밖(ref · 클래스)에 두고 무엇만 state에 남길지가 과제였습니다.
매 프레임 바뀌는 값은 ref · 클래스에, React state는 UI 값만 — 프레임마다 `setState`하는 곳 0 · 참조 고정으로 렌더 670 → 49회. 설계 결정은 [README 「한눈에 보기」](https://github.com/Donghunn-Lee/aimtest#한눈에-보기)에.

`React 19` `TypeScript` `Vite 8` `Tailwind CSS` `framer-motion` `Express 5 (Vercel Function)` `Neon PostgreSQL` `Vitest`

<br/>

### 팀 프로젝트

Codeit Sprint 프론트엔드 부트캠프에서 진행한 팀 프로젝트입니다.

| | 담당 | 구성 · 기간 | 링크 |
|---|---|---|---|
| **Coworkers** — 업무 진행 상황을 시각화하는 협업 서비스 | 인증 · 접근 제어(Next.js middleware) · 서버/UI 상태 책임 분리(React Query / Zustand persist) · 공통 타입 체계 | FE 5인 · 팀장 · 2025.01 ~ 02 | [Live](https://coworkers-delta.vercel.app) · [GitHub](https://github.com/Team-7-Coworkers/coworkers) |
| **Taskify** — Drag & Drop 기반 협업 대시보드 | 칸반 대시보드(dnd-kit) — DragOver 로컬 갱신 · DragEnd 동기화 · 실패 시 롤백 | FE 5인 · 팀장 · 2024.12 | [Live](https://taskify-11-3-8.netlify.app) · [GitHub](https://github.com/Codeit-Sprint-Part-3-Team-8/Taskify) |

---

## Writing

프로젝트별 개발 일지를 [velog](https://velog.io/@dh82680)에 기록합니다 (SlateKR 187편 · AimTest 25편).

- [[SlateKR #174] 선언만 있던 revalidate와 한 달 멈춰 있던 차트 당일 봉](https://velog.io/@dh82680/SlateKR-174-%EC%84%A0%EC%96%B8%EB%A7%8C-%EC%9E%88%EB%8D%98-revalidate%EC%99%80-%ED%95%9C-%EB%8B%AC-%EB%A9%88%EC%B6%B0-%EC%9E%88%EB%8D%98-%EC%B0%A8%ED%8A%B8-%EB%8B%B9%EC%9D%BC-%EB%B4%89)
- [[SlateKR #178] 모바일 홈 자동 스크롤과 글꼴 로딩에 따른 레이아웃 변동](https://velog.io/@dh82680/SlateKR-178-%EB%AA%A8%EB%B0%94%EC%9D%BC-%ED%99%88-%EC%9E%90%EB%8F%99-%EC%8A%A4%ED%81%AC%EB%A1%A4%EA%B3%BC-%EA%B8%80%EA%BC%B4-%EB%A1%9C%EB%94%A9%EC%97%90-%EB%94%B0%EB%A5%B8-%EB%A0%88%EC%9D%B4%EC%95%84%EC%9B%83-%EB%B3%80%EB%8F%99)
- [[SlateKR #075] intraday 실패 캐시 결함 해결](https://velog.io/@dh82680/SlateKR-075-intraday-%EC%8B%A4%ED%8C%A8-%EC%BA%90%EC%8B%9C-%EA%B2%B0%ED%95%A8-%ED%95%B4%EA%B2%B0)
- [[AimTest #24] 마우스 점프와 결과 창에서 살아나던 루프](https://velog.io/@dh82680/AimTest-24-%EB%A7%88%EC%9A%B0%EC%8A%A4-%EC%A0%90%ED%94%84%EC%99%80-%EA%B2%B0%EA%B3%BC-%EC%B0%BD%EC%97%90%EC%84%9C-%EC%82%B4%EC%95%84%EB%82%98%EB%8D%98-%EB%A3%A8%ED%94%84)

---

## Contact

- 📧 dh82680@gmail.com
- 📝 [velog.io/@dh82680](https://velog.io/@dh82680)
