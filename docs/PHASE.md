# 🗂️ PHASE LOG

프로젝트 진행 단계와 **완료한 작업** 기록입니다.
앞으로 할 일은 [BACKLOG.md](./BACKLOG.md)를 참고하세요.

- **프로젝트**: 이예찬 포트폴리오 (https://pgaey.github.io)
- **스택**: Astro 6 + Tailwind CSS 4 (`@tailwindcss/vite`)
- **패키지 매니저**: pnpm
- **배포**: GitHub Pages (GitHub Actions `deploy.yml`, `main` push 시 자동)
- **Node**: 22.12.0+

---

## ✅ Phase 0 — 초기 구축 & 마이그레이션 (완료)

Jekyll(Chirpy 테마) 기반 사이트를 Astro로 전면 전환하고 배포까지 성공.

- [x] Jekyll Chirpy → Astro 포트폴리오로 전환 (`25d0778`)
- [x] GitHub Actions Astro 빌드 워크플로우 구성, Node 22 지정 (`814816c`)
- [x] pnpm 빌드 스크립트 트러블슈팅 (esbuild, sharp) (`05cc6e8`)
- [x] `onlyBuiltDependencies` → `pnpm-workspace.yaml`로 이동 (`41a8316`)
- [x] pnpm 11 `allowBuilds`로 빌드 스크립트 허용 (`9715bbc`)
- [x] GitHub Pages 배포 성공

### 트러블슈팅 메모
- **pnpm 빌드 스크립트 차단**: pnpm 10+/11에서 `esbuild`, `sharp` 등 postinstall 스크립트가 기본 차단됨.
  → `pnpm-workspace.yaml`에 `allowBuilds: { esbuild: true, sharp: true }`로 명시 허용.
- **CI Node 버전**: `withastro/action@v3`에 `node-version: 22` 지정 필요.

---

## ✅ Phase 1 — 기본 페이지 골격 (완료)

단일 페이지(`src/pages/index.astro`) 포트폴리오 레이아웃 구현.

- [x] 상단 고정 네비게이션 (About / Skills / Projects 앵커)
- [x] Hero 섹션 (이름, 역할, 소개, GitHub/이메일 버튼)
- [x] About 섹션
- [x] Skills 섹션 (Frontend / Testing / Infra·DevOps / Backend 그룹)
- [x] Footer
- [x] 데이터-주도 마크업 (`skillGroups` 배열 → `.map()` 렌더링)

---

## 🚧 Phase 2 — 콘텐츠 완성 (진행 예정)

포트폴리오의 핵심 콘텐츠를 채우는 단계. **다음 시작점.**

- [ ] 🔴 경력(Experience) 섹션 추가
- [ ] 🔴 Projects 섹션 실제 콘텐츠 (현재 "준비 중" placeholder)
- [ ] 🟡 About 문구 실제 경력에 맞게 조정
- [ ] 🟡 README 실제 내용으로 교체

> 상세 항목은 [BACKLOG.md](./BACKLOG.md) 참고.

---

## 🔮 Phase 3 — 다듬기 & SEO (예정)

- [ ] 다크 모드, 애니메이션, 반응형 점검
- [ ] OG 메타태그 / 파비콘 / sitemap
- [ ] 이력서 PDF 다운로드

---

## 배포 메모

GitHub Actions(`.github/workflows/deploy.yml`)는 다음 두 경우에 동작:
1. **`main` 브랜치 push** (`on: push: branches: [main]`)
2. **수동 실행** (`workflow_dispatch` — Actions 탭에서 "Run workflow")

→ `test`, `test1`, `dependabot/*` 등 **다른 브랜치 push로는 배포가 트리거되지 않음.**
PR을 main에 머지하거나 main에 직접 push할 때만 자동 배포된다.
