# JCHS-Music-Player-Client

> 음악 스트리밍 웹, Shazam 차트·미리 듣기 (React · Vite)

음악 스트리밍 플랫폼의 웹 클라이언트다. 제천고 코딩 동아리 "코딩연구소" 시절인 2023년에 만들었다. 현재 코드는 자체 서버가 아니라 RapidAPI의 Shazam Core API에서 차트·검색·아티스트 정보를 받아 오고, 미리 듣기 음원을 재생한다.

## 주요 기능
- 홈: 한국 인기 차트
- 곡·아티스트 검색
- 아티스트 상세
- 하단 플레이어: 재생·일시정지, 이전·다음 곡, 반복·셔플, 탐색 바, 볼륨

## 기술 스택
| 영역 | 기술 |
|---|---|
| 언어 | JavaScript |
| 프레임워크 | React 18, Vite 2, React Router 6, Redux Toolkit (RTK Query), Tailwind CSS 3, MUI 5 |
| 인프라 | Shazam Core API (RapidAPI) |

## 구조
```
src/
  router/               라우트 (/home, /search/:query, /artist/:id)
  pages/                TopCharts · Search · ArtistDetail
  components/           곡 카드, 사이드바, 검색창 등
  components/player/    하단 플레이어
  redux/services/api.js Shazam Core API 쿼리
  redux/features/       재생 상태
```

## 실행
```bash
yarn install
yarn dev
```
`src/redux/services/api.js`의 `X-RapidAPI-Key` 자리에 RapidAPI 키를 넣는다.

## 관련 저장소
- [JCHS-Music-Player-Server](https://github.com/son-daehyeon/JCHS-Music-Player-Server) — 음악 스트리밍 API 서버 (Spring Boot)

---
2023 · 개인 프로젝트 · 보관됨
