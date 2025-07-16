# 📡 BADATA: 1인 가구를 위한 데이터 공유·거래 통합 플랫폼

&nbsp;  
&nbsp;  

<div align="center">
  <img src="https://github.com/user-attachments/assets/02721348-01fc-458d-aba8-f66654e625a7" width="200" />  
  <br/>
  <strong>LG유플러스 유레카 2기</strong><br/>
  융합프로젝트 2조 바다 컨셉 + LG U+ = <strong>2SeaU</strong>
</div>

&nbsp;  
&nbsp;  



## 🧑‍🤝‍🧑 팀원 소개 및 역할

| 이름 | 역할 | 주요 담당 |
|------|------|------------|
| **박은서** | 총괄 팀장 | 회원가입 / 거래 등록 / UX 흐름 설계 및 QA 총괄 |
| **이시현** | 프론트엔드 팀장 | 프로젝트 설계, 거래 메인 페이지 UI 및 관련 기능 구현|
| **이진우** | 백엔드 팀장 | ERD 설계, 보안 흐름 설계, 렌탈·기부 API 핵심 로직 |
| **이은채** | 프론트엔드 | 거래 게시판, OCR 연동 UI, 리워드 코인 기능 |
| **박지회** | 프론트엔드 | 홈 / 마이페이지 / SOS UI 및 리워드 시각화 |
| **김도연** | 백엔드 | 마이페이지 API, OCR 처리, 저금통 설계 |
| **조윤주** | 백엔드 | 거래 CRUD API, 가맹점 필터링, 리워드 시스템 |

&nbsp;  
&nbsp;  



## 🧠 기획 배경

- **문제 인식**: 자취 중 데이터를 버리거나 급히 필요했던 상황에서 느낀 개인 간 데이터 공유의 부재  
- **시장 인사이트**: 데이터 공유는 디지털 경쟁력의 핵심. 현실적 보안/접근성/속도 문제 해결 필요  
- **솔루션**: 위치 기반 공유기 대여 + 개인 거래 게시판 + SOS 시스템으로 순환형 데이터 플랫폼 구현  

> 📎 참고 기사  
> [Databricks - Data Sharing](https://www.databricks.com/kr/glossary/data-sharing)  
> [LG U+ 유독 데이터 요금제](https://www.lguplus.com/mobile/plan/addon/addon-data/Z202211243)

&nbsp;  
&nbsp;  



## 📅 개발 일정

| 기간 | 내용 |
|------|------|
| 6/30 ~ 7/6 | 1차 기획 스프린트 (ERD, 디자인, 초기 환경 세팅) |
| 7/8 ~ 7/14 | 1차 개발 (거래 도메인, 로그인 구현) |
| 7/15 ~ 7/16 | 1차 QA |
| 7/17 ~ 7/23 | 2차 개발 (대여/SOS 도메인) |
| 7/24 ~ 7/25 | 2차 QA |
| 7/26 ~ 7/29 | 성능 최적화 |
| 7/30 ~ 8/2 | 사용자 베타 테스트 + 분석 |
| 8/2 ~ 8/4 | 트러블슈팅 정리 |
| 8/5 ~ 8/6 | 최종 결과물 제작 및 발표 |

&nbsp;  
&nbsp;  



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

&nbsp;  
&nbsp;  



## 💻 프론트엔드 기술 스택

| 분류 | 스택 | 설명 |
|------|------|------|
| 프레임워크 & 언어 | ![Next.js](https://img.shields.io/badge/Next.js-000000?logo=nextdotjs&logoColor=white)<br>![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white) | App Router 기반 SSR & CSR 혼합 프레임워크 / 정적 타입을 통한 안정적인 코드 |
| 상태관리 & 서버 상태 | ![Zustand](https://img.shields.io/badge/Zustand-000000?logo=zotero&logoColor=white)<br>![React Query](https://img.shields.io/badge/React_Query-FF4154?logo=reactquery&logoColor=white) | 전역 상태 관리 (클라이언트 상태), 서버 상태 동기화 및 캐싱 처리 |
| API 통신 | ![Axios](https://img.shields.io/badge/Axios-5A29E4?logo=axios&logoColor=white) | RESTful API 요청/응답 핸들링 및 인터셉터 기반 에러 제어 |
| 스타일링 & UI | ![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-06B6D4?logo=tailwindcss&logoColor=white)<br>![Shadcn UI](https://img.shields.io/badge/Shadcn_UI-111827?logo=react&logoColor=white) | 유틸리티 CSS / 커스터마이징 가능한 Headless UI 컴포넌트 |
| 컴포넌트 개발 | ![Storybook](https://img.shields.io/badge/Storybook-FF4785?logo=storybook&logoColor=white) | 독립형 UI 컴포넌트 개발 및 문서화 도구 |
| 코드 품질 관리 | ![ESLint](https://img.shields.io/badge/ESLint-4B32C3?logo=eslint&logoColor=white)<br>![Prettier](https://img.shields.io/badge/Prettier-F7B93E?logo=prettier&logoColor=black)<br>![Husky](https://img.shields.io/badge/Husky-000000?logo=git&logoColor=white) | 린트/포맷 자동화, 커밋 전 검사로 코드 일관성 유지 |
| 번들러 & 배포 | ![Turbopack](https://img.shields.io/badge/Turbopack-000000?logo=vercel&logoColor=white)<br>![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white) | 고속 번들링 + 서버리스 자동 배포 환경 제공 |

&nbsp;  
&nbsp;  



## 🛠 백엔드 기술 스택

| 분류 | 스택 | 설명 |
|------|------|------|
| 언어 & 프레임워크 | ![Java](https://img.shields.io/badge/Java_17-007396?logo=openjdk&logoColor=white)<br>![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?logo=springboot&logoColor=white) | OOP 기반 백엔드 언어 / DI 기반 빠른 개발 |
| 보안 & 인증 | ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?logo=springsecurity&logoColor=white) | JWT 인증 및 역할 기반 인가 처리 |
| DB & ORM | ![JPA](https://img.shields.io/badge/JPA-orange?logo=hibernate&logoColor=white)<br>![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white) | ORM 추상화 + RDBMS |
| 캐시 & 실시간 | ![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white) | 세션/실시간 캐싱 |
| 인프라 / 배포 | ![AWS](https://img.shields.io/badge/AWS_EC2_RDS_S3-232F3E?logo=amazonaws&logoColor=white)<br>![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white) | EC2/RDS/S3 기반 인프라 구축 및 자동화 |
| API 명세 | ![Swagger](https://img.shields.io/badge/Swagger-85EA2D?logo=swagger&logoColor=black) | 명세 자동화 및 테스트 문서화 |

&nbsp;  
&nbsp;  



## 🤝 협업 도구

| 도구 | 설명 |
|------|------|
| ![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white) | 버전 관리 및 협업 |
| ![Jira](https://img.shields.io/badge/Jira-0052CC?logo=jira&logoColor=white) | 이슈/스프린트 기반 태스크 관리 |
| ![Notion](https://img.shields.io/badge/Notion-000000?logo=notion&logoColor=white) | 위키 / 회의록 / API 문서 통합 |
| ![Figma](https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=white) | UI 디자인 및 프로토타이핑 |
| ![Slack](https://img.shields.io/badge/Slack-4A154B?logo=slack&logoColor=white) | 메신저 및 이슈 공유 |
| ![Discord](https://img.shields.io/badge/Discord-5865F2?logo=discord&logoColor=white) | 음성 회의 및 실시간 협업 |

&nbsp;  
&nbsp;  



## 📎 문서 및 자료 링크

- [📁 Google Drive](https://drive.google.com/drive/folders/1aFjriUQpHDcrI7Rt68YGSPTwnH0dJ4bn?pli=1)  
- [🗺 ERD Cloud](https://www.erdcloud.com/d/NnvfEkHaQgXSXHWCm)  
- [📜 API 명세서 (Notion)](https://www.notion.so/API-225672106a2081389214daa0b7ed286d?source=copy_link)  
- [🎨 Figma 디자인](https://www.figma.com/design/SfCoh6OwnZCvbfryBysNpe/BADATA_2SeaU-%EC%9C%A0%EB%A0%88%EC%B9%B4-%EC%B5%9C%EC%A2%85-%EC%9C%B5%ED%95%A9%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-2%EC%A1%B0-?node-id=0-1&p=f)  



<div align="center">

**Team 2SeaU / BADATA**  
_LG U+ 유레카 2기 최종 융합 프로젝트_

</div>
