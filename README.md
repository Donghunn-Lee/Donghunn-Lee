<div align="center">
  <h1>이동훈 | Donghun Lee</h1>
  <p>Frontend Developer</p>
  <p><strong>요청이 실패해도 멈추지 않는 화면과,<br/>프레임 단위 상호작용의 state/ref 경계를 설계합니다.</strong></p>

  <a href="https://github.com/Donghunn-Lee"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white"/></a>&nbsp;<a href="https://donghunn-lee-blog.vercel.app"><img src="https://img.shields.io/badge/Blog-20C997?style=flat-square&logo=rss&logoColor=white"/></a>&nbsp;<a href="mailto:dh82680@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat-square&logo=gmail&logoColor=white"/></a>
</div>

<br/>

## About

- 외부 데이터에 의존하는 조회형 서비스(SlateKR)와 프레임 단위 상호작용 프로젝트(AimTest)를 각각 1인 개발로 마쳤습니다.
- 방향과 범위, 설계안의 채택 여부, 결과 확인은 직접 맡습니다. 설계안은 Claude와 논의해 정하고, 조사와 코드 생성은 Claude Code에 위임합니다([SlateKR 개발 방식](https://github.com/Donghunn-Lee/slate-kr#개발-방식)). 작업은 세션 단위로 문서화해, 어떤 변경이든 당시의 판단 과정을 추적할 수 있도록 해왔습니다.

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

### [SlateKR — 국내 상장 종목 가격 · 재무 · 공시 조회 웹앱]

개인 프로젝트 · 2026.04 ~ 2026.11 &nbsp;|&nbsp; [Live(가상 데이터 데모)](https://slate-kr.vercel.app) · [GitHub](https://github.com/Donghunn-Lee/slate-kr)

<img width="800" alt="SlateKR 홈" src="https://github.com/Donghunn-Lee/slate-kr/raw/main/docs/images/hero.png" />

국내 상장 종목과 국내 · 해외 지수 12개를 다루는 조회 서비스. 종목 상세 한 페이지가 DB · DART · 시세 API 세 곳에서 데이터를 받아, 한 곳이 늦거나 실패해도 화면을 유지하는 것이 과제였습니다.
섹션 단위 Suspense로 loading · empty · error · 부분 실패를 구분 — 시세 API 응답을 3초 늦춘 조건에서 헤더 표시 약 3.4초 → 0.3초 · 차트 hover 리렌더 0.
국내 시세는 재배포가 허용되지 않아 가격 계열만 결정론적 생성기로 대체했습니다(재무 · 공시는 DART 실데이터). Live 상단 배너의 장애 시뮬레이션으로 가격 API 지연 · 실패 시의 화면을 직접 볼 수 있습니다. 설계 결정은 [README 「한눈에 보기」](https://github.com/Donghunn-Lee/slate-kr#한눈에-보기)에.

`Next.js 16 App Router` `TypeScript` `Tailwind CSS v4` `TanStack Query v5` `Zustand` `Zod` `Neon PostgreSQL` `Vitest`

<br/>

### [AimTest — 브라우저 1인칭 에임 트레이너]

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
| **Coworkers** — 업무 진행 상황을 시각화하는 협업 서비스 | 인증 · 접근 제어(Next.js middleware) · 서버/UI 상태 책임 분리(React Query / Zustand persist) · 공통 타입 체계 | FE 5인 · 팀장 · 2025.01 ~ 02 | [Live](https://coworkers-11-4-7.vercel.app) · [GitHub](https://github.com/Team-7-Coworkers/coworkers) |
| **Taskify** — Drag & Drop 기반 협업 대시보드 | 칸반 대시보드(dnd-kit) — DragOver 로컬 갱신 · DragEnd 동기화 · 실패 시 롤백 | FE 5인 · 팀장 · 2024.12 | [Live](https://taskify-11-3-8.netlify.app) · [GitHub](https://github.com/Codeit-Sprint-Part-3-Team-8/Taskify) |

---

## Writing

프로젝트별 개발 일지를 [블로그](https://donghunn-lee-blog.vercel.app)에 기록합니다 — [SlateKR 시리즈](https://donghunn-lee-blog.vercel.app/blog/slatekr/) · [AimTest 시리즈](https://donghunn-lee-blog.vercel.app/blog/aimtest/).

- [[SlateKR #188] 시세 데이터 약관 전수 조사와 라이브 중단](https://donghunn-lee-blog.vercel.app/blog/slatekr/188/)
- [[SlateKR #174] 선언만 있던 revalidate와 한 달 멈춰 있던 차트 당일 봉](https://donghunn-lee-blog.vercel.app/blog/slatekr/174/)
- [[SlateKR #178] 모바일 홈 자동 스크롤과 글꼴 로딩에 따른 레이아웃 변동](https://donghunn-lee-blog.vercel.app/blog/slatekr/178/)
- [[SlateKR #075] intraday 실패 캐시 결함 해결](https://donghunn-lee-blog.vercel.app/blog/slatekr/075/)
- [[AimTest #24] 마우스 점프와 결과 창에서 살아나던 루프](https://donghunn-lee-blog.vercel.app/blog/aimtest/24/)

---

## Contact

- 📧 dh82680@gmail.com
- 📝 [donghunn-lee-blog.vercel.app](https://donghunn-lee-blog.vercel.app)
