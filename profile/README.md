# 📡 BADATA: 1인 가구를 위한 데이터 공유·거래 통합 플랫폼


<div align="center">
<img src="https://github.com/user-attachments/assets/02721348-01fc-458d-aba8-f66654e625a7" width="200" />
  
**LG유플러스 유레카 프론트엔드 개발자 2기**  
융합프로젝트 2조 바다 컨셉 + LG U+ = **2SeaU**
</div>

---

## 🧑‍🤝‍🧑 팀원 소개 및 역할

| 이름   | 역할        | 주요 담당 |
|--------|-------------|-----------|
| 박은서 | 총괄 팀장   | 회원가입/거래 등록/UX 흐름 설계 및 QA 총괄 |
| 이시현 | FE 팀장     | 카카오 로그인, 지도 기반 가맹점 UI/UX |
| 이진우 | BE 팀장     | ERD, 보안 흐름, 렌탈/기부 API 핵심 로직 |
| 이은채 | FE          | 거래 게시판, OCR 연동 UI, 리워드 코인 |
| 박지회 | FE          | 홈/마이페이지, SOS UI, 리워드 시각화 |
| 김도연 | BE          | 마이페이지 API, OCR 처리, 저금통 설계 |
| 조윤주 | BE          | 거래 CRUD API, 가맹점 필터링, 리워드 시스템 |

---

## 🧠 기획 배경

- **문제 인식**: 자취 중 데이터를 버리거나 급히 필요했던 상황에서 느낀 개인 간 데이터 공유의 부재
- **시장 인사이트**: 데이터 공유는 디지털 경쟁력의 핵심. 현실적 보안/접근성/속도 문제 해결 필요
- **솔루션**: 위치 기반 공유기 대여 + 개인 거래 게시판 + SOS 시스템으로 순환형 데이터 플랫폼 구현

> 📎 참고 기사  
> [Databricks - Data Sharing](https://www.databricks.com/kr/glossary/data-sharing)  
> [LG U+ 유독 데이터 요금제](https://www.lguplus.com/mobile/plan/addon/addon-data/Z202211243)

---

## 📅 개발 일정

| 기간        | 내용 |
|-------------|------|
| 6/30 ~ 7/6  | 1차 기획 스프린트 (ERD, 디자인, 초기 환경 세팅) |
| 7/8 ~ 7/14  | 1차 개발 (거래 도메인, 로그인 구현) |
| 7/15 ~ 7/16 | 1차 QA |
| 7/17 ~ 7/23 | 2차 개발 (대여/SOS 도메인) |
| 7/24 ~ 7/25 | 2차 QA |
| 7/26 ~ 7/29 | 성능 최적화 |
| 7/30 ~ 8/2  | 사용자 베타 테스트 + 분석 |
| 8/2 ~ 8/4   | 트러블슈팅 정리 |
| 8/5 ~ 8/6   | 최종 결과물 제작 및 발표 |

---

## 🧩 핵심 기능

### ✅ 회원 관리
- 카카오 로그인 및 선호도/위치 정보 수집
- 비회원 제한 기능 및 마이페이지 정보 시각화

### ✅ 거래 게시판
- 데이터 및 기프티콘 판매 등록
- OCR 이미지 인식 → 게시글 자동 작성
- 관심 글 저장, 태그/검색/추천 기반 탐색

### ✅ 공유기 대여 기능
- LGU+ 가맹점 지도 기반 공유기 필터링
- 렌탈 가능 시간/기기 수량 기반 조건 검색
- 예약 → 웨이팅 기능까지 연동

### ✅ 데이터 SOS 시스템
- 100MB 단위 요청/기부 가능
- 기부자에겐 20MB 코인 보상 지급
- 월말 데이터 소멸 시 자동 저금통 저장 → 코인 적립
- 적립 코인으로 리워드 상품 구매 가능

---

## 🛠 기술 스택

## 💻 Frontend 기술 스택 (기능별 정리)

| 🗂️ 카테고리 | 스택 | 설명 |
|------------|------|------|
| **프레임워크 & 언어** | ![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)<br>![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white) | App Router 기반 SSR & CSR 혼합 프레임워크 / 정적 타입을 통한 안정적인 코드 |
| **상태관리 & 서버 상태** | ![Zustand](https://img.shields.io/badge/Zustand-000000?logo=Zustand&logoColor=white)<br>![React Query](https://img.shields.io/badge/React_Query-FF4154?logo=reactquery&logoColor=white) | 전역 상태 관리 (클라이언트 상태), 서버 상태 동기화 및 캐싱 처리 |
| **API 통신** | ![Axios](https://img.shields.io/badge/Axios-5A29E4?logo=axios&logoColor=white) | RESTful API 요청/응답 핸들링 및 인터셉터 기반 에러 제어 |
| **스타일링 & UI** | ![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-06B6D4?logo=tailwindcss&logoColor=white)<br>![Shadcn UI](https://img.shields.io/badge/Shadcn_UI-111827?logo=react&logoColor=white) | 클래스 기반 유틸리티 CSS 프레임워크 / Headless UI 기반의 커스터마이징 가능한 UI |
| **컴포넌트 개발** | ![Storybook](https://img.shields.io/badge/Storybook-FF4785?logo=storybook&logoColor=white) | 독립형 UI 컴포넌트 개발 및 문서화 도구 |
| **코드 품질 & 형식** | ![ESLint](https://img.shields.io/badge/ESLint-4B32C3?logo=eslint&logoColor=white)<br>![Prettier](https://img.shields.io/badge/Prettier-F7B93E?logo=prettier&logoColor=black)<br>![Husky](https://img.shields.io/badge/Husky-000000?logo=git&logoColor=white) | 코드 스타일 검사 / 자동 정렬 / Git hook 기반 사전 검사 |
| **빌드 & 배포** | ![Turbopack](https://img.shields.io/badge/Turbopack-000000?logo=vercel&logoColor=white)<br>![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white) | 고속 번들러 / 서버리스 기반 자동 배포 플랫폼 |

---

## 🔧 Backend 기술 스택 (기능별 정리)

| 🗂️ 카테고리 | 스택 | 설명 |
|------------|------|------|
| **언어 & 프레임워크** | ![Java](https://img.shields.io/badge/Java_17-007396?logo=openjdk&logoColor=white)<br>![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white) | 객체지향 기반 백엔드 언어 / 빠른 개발을 위한 DI 기반 프레임워크 |
| **보안 & 인증** | ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?logo=springsecurity&logoColor=white) | JWT 인증, 권한 기반 인가 처리 |
| **DB & ORM** | ![JPA](https://img.shields.io/badge/JPA-orange?logo=hibernate&logoColor=white)<br>![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white) | ORM을 통한 DB 추상화 / 오픈소스 RDB |
| **캐시 & 실시간 데이터** | ![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white) | 세션 관리 및 휘발성 저장소로 고속 접근 지원 |
| **인프라 / 배포** | ![AWS](https://img.shields.io/badge/AWS_EC2_RDS_S3-232F3E?logo=amazonaws&logoColor=white)<br>![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white) | EC2, RDS, S3로 인프라 구축 / GitHub 기반 CI-CD 자동화 |
| **API 명세화** | ![Swagger](https://img.shields.io/badge/Swagger-85EA2D?logo=swagger&logoColor=black) | Swagger를 통한 API 문서 자동화 및 테스트 |

---

## 🤝 협업 도구

| 도구 | 역할 | 설명 |
|------|------|------|
| ![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white) | 형상 관리 | 소스코드 버전 관리 및 PR 기반 협업 |
| ![Jira](https://img.shields.io/badge/Jira-0052CC?logo=jira&logoColor=white) | 이슈/태스크 관리 | 스프린트 기반 업무 트래킹 |
| ![Notion](https://img.shields.io/badge/Notion-000000?logo=notion&logoColor=white) | 문서 협업 | 회의록, 기획 문서, API 정리 등 통합 위키 |
| ![Figma](https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=white) | UI 설계 | 컴포넌트 디자인 및 프로토타입 공유 |
| ![Slack](https://img.shields.io/badge/Slack-4A154B?logo=slack&logoColor=white) | 메신저 | 팀 채널 기반 실시간 소통 도구 |
| ![Discord](https://img.shields.io/badge/Discord-5865F2?logo=discord&logoColor=white) | 보이스 협업 | 실시간 음성 회의 및 화면 공유 |



---

## 📎 문서 및 자료 링크

- [WBS (Google Drive)](https://example.com)
- [플로우차트 (Figma)](https://example.com)
- [API 명세서 (Notion)](https://example.com)
- [ERD (ERDCloud)](https://example.com)
- [Storybook](https://example.com)

---

**Team 2SeaU / BADATA**  
_LG U+ 유레카 프론트엔드 개발자 2기 종합 프로젝트_

