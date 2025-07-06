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

### 💻 Frontend

- Next.js (App Router)
- TypeScript
- Zustand / React Query / Axios
- Tailwind CSS / Shadcn UI
- Storybook
- ESLint / Prettier / Husky
- Turbopack
- Vercel

### 🔧 Backend

- Java 17 / Spring Boot / Spring Security
- JPA / Hibernate / Spring Boot Test
- PostgreSQL + PGVector / Redis
- AWS EC2, RDS, S3
- Swagger / ERDcloud
- GitHub Actions

### 🤝 협업 도구

- GitHub, Jira, Notion, Figma, Slack, Discord

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
