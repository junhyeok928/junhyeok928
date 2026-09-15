<div align="center">

<br />

`JAVA · SPRING BOOT · REACT`

# JUNHYEOK JEON

### 전준혁 · Web Developer

**화면부터 API, 데이터와 배포까지 연결하는 웹 개발자**

Java와 Spring Boot로 서비스 로직을 구현하고,<br />
React로 사용자 화면과 운영자를 위한 관리 도구를 만듭니다.

<br />

<a href="https://github.com/junhyeok928/snapthetitle-app"><img src="https://img.shields.io/badge/VIEW_PROJECT-SnapTheTitle-20383D?style=for-the-badge" alt="대표 프로젝트 SnapTheTitle" /></a>
<a href="https://snapthetitle.com"><img src="https://img.shields.io/badge/VISIT-Website-E8E4DA?style=for-the-badge" alt="SnapTheTitle 웹사이트" /></a>

<br /><br />

**BUILD THE EXPERIENCE. CONNECT THE SYSTEM.**

</div>

---

## 01 / About

웨딩 스냅 브랜드 **SnapTheTitle**의 홈페이지와 관리자 시스템을 구현했습니다.<br />
촬영 사진을 탐색하는 공개 화면부터 콘텐츠 관리, 관리자 인증, 이미지 처리, 배포 구성까지 하나의 프로젝트로 연결했습니다.

| 사용자 경험 | 서비스 로직 | 운영 환경 |
| :--- | :--- | :--- |
| 사진 탐색과 확대 보기 | JWT 관리자 인증 | Docker Compose 서비스 구성 |
| 반응형 사용자·관리자 UI | 콘텐츠 CRUD와 데이터 모델 | Nginx HTTPS·API 프록시 |
| 드래그 앤 드롭 사진 정렬 | WebP 변환과 썸네일 생성 | 업로드 파일 제공·정적 캐시 |

<br />

## 02 / Tech Stack

**프로젝트에서 실제 사용한 기술입니다.**

### Backend

<p>
<img src="https://img.shields.io/badge/Java_17-20383D?style=flat-square" alt="Java 17" />
<img src="https://img.shields.io/badge/Spring_Boot-20383D?style=flat-square&amp;logo=springboot&amp;logoColor=6DB33F" alt="Spring Boot" />
<img src="https://img.shields.io/badge/Spring_Security-20383D?style=flat-square&amp;logo=springsecurity&amp;logoColor=6DB33F" alt="Spring Security" />
<img src="https://img.shields.io/badge/Spring_Data_JPA-20383D?style=flat-square" alt="Spring Data JPA" />
<img src="https://img.shields.io/badge/MySQL-20383D?style=flat-square&amp;logo=mysql&amp;logoColor=FFFFFF" alt="MySQL" />
</p>

REST API · JJWT · BCrypt · Flyway · Scrimage · Gradle

### Frontend

<p>
<img src="https://img.shields.io/badge/JavaScript-20383D?style=flat-square&amp;logo=javascript&amp;logoColor=F7DF1E" alt="JavaScript" />
<img src="https://img.shields.io/badge/React-20383D?style=flat-square&amp;logo=react&amp;logoColor=61DAFB" alt="React" />
<img src="https://img.shields.io/badge/Tailwind_CSS-20383D?style=flat-square&amp;logo=tailwindcss&amp;logoColor=38BDF8" alt="Tailwind CSS" />
<img src="https://img.shields.io/badge/React_Router-20383D?style=flat-square&amp;logo=reactrouter&amp;logoColor=FFFFFF" alt="React Router" />
</p>

Context API · Axios · Fetch API · dnd-kit · Recharts

### Infrastructure

<p>
<img src="https://img.shields.io/badge/Docker-20383D?style=flat-square&amp;logo=docker&amp;logoColor=2496ED" alt="Docker" />
<img src="https://img.shields.io/badge/Docker_Compose-20383D?style=flat-square" alt="Docker Compose" />
<img src="https://img.shields.io/badge/Nginx-20383D?style=flat-square&amp;logo=nginx&amp;logoColor=009639" alt="Nginx" />
<img src="https://img.shields.io/badge/Git-20383D?style=flat-square&amp;logo=git&amp;logoColor=F05032" alt="Git" />
</p>

HTTPS · Let's Encrypt / Certbot · 정적 파일 캐시 · 공유 업로드 볼륨

<br />

## 03 / Featured Project

<a href="https://github.com/junhyeok928/snapthetitle-app">
<img src="https://raw.githubusercontent.com/junhyeok928/snapthetitle-app/main/docs/assets/readme-cover.svg" width="100%" alt="SnapTheTitle — Photography meets engineering" />
</a>

### SnapTheTitle

**웨딩 스냅 홈페이지 & 콘텐츠 관리 시스템**

방문자는 사진과 연도별 상품을 탐색하고, 운영자는 관리자 화면에서 사진과 안내 콘텐츠를 직접 관리합니다. React 프론트엔드와 Spring Boot 백엔드를 **하나의 통합 저장소**에서 관리합니다.

| 구현 영역 | 주요 내용 |
| :--- | :--- |
| **이미지 처리** | 서버에서 WebP 변환과 너비 400px 썸네일 생성, 목록·확대 화면의 이미지 URL 분리 |
| **인증과 권한** | BCrypt 비밀번호 검증, JWT 발급·검증, 관리자 API의 ADMIN 권한 검사 |
| **콘텐츠 관리** | 사진 업로드·노출 순서 변경, 연도별 상품·옵션, FAQ·가이드·제휴 업체 CRUD |
| **방문 통계** | IP 기반 방문 기록, 최근 7일 추이와 유입 경로 차트 |
| **배포 구성** | Docker Compose, Nginx 리버스 프록시, HTTPS와 정적 파일 캐시 |

[**프로젝트 README →**](https://github.com/junhyeok928/snapthetitle-app#readme) &nbsp; · &nbsp; [**서비스 보기 ↗**](https://snapthetitle.com)

<details>
<summary><strong>시스템 구조 펼쳐보기</strong></summary>

```mermaid
flowchart TD
    U[사용자 / 관리자 브라우저] -->|HTTPS| N[Nginx]
    N -->|정적 화면| R[React 빌드 파일]
    N -->|API 요청| B[Spring Boot]
    B -->|JPA| D[(MySQL)]
    B -->|WebP / 썸네일 저장| F[공유 업로드 디렉터리]
    N -->|이미지 제공| F

    classDef dark fill:#20383d,color:#f4f0e7,stroke:#20383d
    classDef light fill:#edf2ec,color:#20383d,stroke:#839981
    classDef warm fill:#f4f0e7,color:#443e32,stroke:#b9aa88
    class U,N dark
    class R,B light
    class D,F warm
```

</details>

<br />

## 04 / Code Highlights

구현 방식은 아래 코드에서 확인할 수 있습니다.

| 관심 영역 | 코드 |
| :--- | :--- |
| 이미지 변환과 첨부파일 저장 | [AttachmentService.java](https://github.com/junhyeok928/snapthetitle-app/blob/main/snapthetitle-backend/src/main/java/com/snapthetitle/backend/service/AttachmentService.java) |
| 서버의 관리자 접근 제어 | [SecurityConfig.java](https://github.com/junhyeok928/snapthetitle-app/blob/main/snapthetitle-backend/src/main/java/com/snapthetitle/backend/config/SecurityConfig.java) |
| React 인증 상태 관리 | [AuthContext.jsx](https://github.com/junhyeok928/snapthetitle-app/blob/main/snapthetitle/src/contexts/AuthContext.jsx) |
| 사진 관리 및 드래그 정렬 | [GalleryManagement.jsx](https://github.com/junhyeok928/snapthetitle-app/blob/main/snapthetitle/src/components/admin/GalleryManagement.jsx) |
| 컨테이너와 서비스 연결 | [docker-compose.yml](https://github.com/junhyeok928/snapthetitle-app/blob/main/docker-compose.yml) |

---

<div align="center">

**전준혁 · JUNHYEOK JEON**

[GitHub](https://github.com/junhyeok928) &nbsp; / &nbsp; [Featured Project](https://github.com/junhyeok928/snapthetitle-app)

</div>
