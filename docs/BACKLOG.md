# 📋 BACKLOG

이 사이트(이예찬 포트폴리오)의 **앞으로 할 일** 목록입니다.
완료한 작업의 상세 기록은 [PHASE.md](./PHASE.md)를 참고하세요.

> 우선순위: 🔴 높음 · 🟡 중간 · ⚪ 낮음
> 상태: `TODO` · `WIP`(진행 중) · `DONE`(완료 시 PHASE.md로 이동)

---

## 콘텐츠

| 상태 | 우선 | 작업 | 메모 |
| :--: | :--: | :--- | :--- |
| TODO | 🔴 | **경력(Experience) 섹션 추가** | 회사/기간/역할/주요 성과. About~Skills 사이 또는 Skills 아래 배치 |
| TODO | 🔴 | **Projects 섹션 실제 콘텐츠 채우기** | 현재 "준비 중" placeholder. 프로젝트 카드(제목/설명/기술스택/링크) 2~3개 |
| TODO | 🟡 | About 문구 다듬기 | 현재 3년차 기준 문구. 실제 경력에 맞게 조정 |
| TODO | ⚪ | 학력/자격증/수상 섹션 (선택) | 필요 시 |

## 기능 / UX

| 상태 | 우선 | 작업 | 메모 |
| :--: | :--: | :--- | :--- |
| TODO | 🟡 | 다크 모드 토글 | Tailwind `dark:` 변형 활용 |
| TODO | 🟡 | 이력서 PDF 다운로드 버튼 | `public/`에 PDF 두고 Hero에 링크 |
| TODO | ⚪ | 스크롤 시 섹션 페이드인 애니메이션 | Intersection Observer 또는 CSS |
| TODO | ⚪ | 반응형 점검(모바일/태블릿) | 현재 `max-w-3xl` 단일 레이아웃 |

## SEO / 메타

| 상태 | 우선 | 작업 | 메모 |
| :--: | :--: | :--- | :--- |
| TODO | 🟡 | OG 이미지 / 메타태그 보강 | `og:image`, `twitter:card` 등 |
| TODO | ⚪ | `sitemap.xml` / `robots.txt` | `@astrojs/sitemap` 통합 고려 |
| TODO | ⚪ | 파비콘 실제 이미지로 교체 | 현재 이모지 SVG |

## 정리 / 유지보수

| 상태 | 우선 | 작업 | 메모 |
| :--: | :--: | :--- | :--- |
| TODO | 🟡 | README 실제 내용으로 교체 | 현재 Astro 기본 스타터 README |
| TODO | ⚪ | 불필요 원격 브랜치 정리 | `test`, `test1` 등 |
| TODO | ⚪ | Footer 연도 동적 처리 | 현재 `© 2025` 하드코딩 |

---

## 다음에 시작할 작업 (Next up)

1. 🔴 **경력 섹션 추가** — `src/pages/index.astro`에 `experiences` 데이터 배열 + 섹션 마크업
2. 🔴 **Projects 섹션 채우기** — placeholder 제거하고 실제 프로젝트 카드 구현
3. 🟡 README 교체

> 새 작업을 시작하기 전에 이 파일을 먼저 읽고, 완료하면 해당 항목을 PHASE.md로 옮기세요.
