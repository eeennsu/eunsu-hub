# eunsu-hub

`eunsu.pro` 루트 도메인 링크 허브. 이력서 · 블로그 · GitHub 로 분기하는 정적 랜딩 페이지.

## 목적

- 방은수 브랜드 허브
- 서브도메인(`resume.eunsu.pro`, `eunstory.eunsu.pro`) 대상 dofollow 백링크 확보
- "방은수 이력서" 쿼리 검색 노출 강화

## 배포

Vercel 정적 프로젝트로 배포. 빌드 스텝 없음. 저장소 루트 그대로 서빙.

```
Framework Preset: Other
Build Command: (empty)
Output Directory: ./
Install Command: (empty)
```

배포 후 Vercel Domains 에서 `eunsu.pro` 연결.

## 구조

- `index.html` — 랜딩 페이지
- `robots.txt` — 크롤러 허용 + 사이트맵 참조
- `sitemap.xml` — 루트 URL 등록
- `vercel.json` — 보안 헤더

## 유지보수

링크 추가 시 `index.html` 의 `<nav>` 블록과 JSON-LD `sameAs` 배열에 함께 등록.
