# MABC 2026 결선 가이드

README(시작 안내) / Upstage Console(크레딧 · API 키) / GitHub 연동 / Vercel 배포 / Hermes Agent 설치 가이드를 한 페이지에 탭으로 묶은 참가자용 문서입니다.

- 공개 주소: https://upstage-mabc-final-guide.vercel.app
- `main` 브랜치에 푸시하면 Vercel이 자동으로 다시 배포합니다 (1~2분).

## 파일 구성

| 경로 | 설명 |
|---|---|
| `index.html` | 배포되는 파일 그 자체. **이 파일이 원본입니다.** 이미지가 전부 내장되어 있어 이것만 열어도 됩니다 |
| `media/hermes/` | Upstage 콘솔 · 헤르메스 캡처 원본 (이메일 마스킹본) |
| `media/github/` | GitHub 연동 가이드 캡처 원본 (타임리 · 헤르메스 연동 화면 포함) |
| `media/vercel/` | Vercel 가이드 캡처 원본 (타임리 커넥터 화면 포함) |
| `vercel.json` | 배포 설정 (`cleanUrls`) |

## 고치는 법

1. `index.html`을 VS Code, Cursor 등 텍스트 편집기로 엽니다.
2. 다섯 문서는 각각 아래 블록 안에 있습니다. 찾기(Ctrl/Cmd+F)로 이동합니다.
   - `data-doc="home"` — README (시작 안내)
   - `data-doc="key"` — Upstage Console (크레딧 · API 키)
   - `data-doc="github"` — GitHub 연동
   - `data-doc="vercel"` — Vercel 배포
   - `data-doc="hermes"` — Hermes Agent 설치
3. 절 id 규칙: 시작 안내 `home-intro`·`home-flow`, Upstage `key-sec1`, GitHub `gh-sec1`, Vercel `v-sec1`·`v-sec1-1`, 헤르메스 `sec1`·`sec1-1`.
   다른 문서의 절로 가는 링크는 `<a class="xref" href="#v-sec8">…</a>` 처럼 id만 적으면 탭이 자동으로 바뀝니다.
4. 문서 짜임새는 다섯 탭이 똑같이 지킵니다. 문서를 하나 더 붙일 때도 이 순서입니다.
   - 히어로: `hero-eyebrow` → `h1.headline` → `p.hero-lede` → `.doc-switch`(다른 문서 카드).
     카드는 제목 **아래**입니다. 2열 그리드이고 640px 아래에서 1열이 됩니다.
   - 그다음 소개 문단 → `표기` 안내 상자 → `문서 구성` 표 → 본문. 여기까지가 `<section id="…-intro">` 안입니다.
   - 각 장은 `<section id="…"><div class="section-label">PART N</div><h2 class="headline">…`.
     PART 라벨이 장 사이 여백과 구분선을 담당하므로 장마다 반드시 넣습니다.
   - 절 번호는 `1.1` 모양으로 씁니다 (`1-1` 아님).
   - `[공식]`·`[킷]` 같은 출처 표시는 본문에만 넣고 왼쪽 목차에는 넣지 않습니다.
   - 마지막에서 두 번째 장은 `잘 안 될 때` 표, 마지막은 `체크리스트`(`ul.check-list`), 그 뒤가 `출처`입니다.
5. 자주 쓰는 블록
   - 안내 상자: `<div class="callout callout--note">…</div>` (`note` / `tip` / `warn` / `danger`)
   - 단계: `<div class="steps"><div class="step"><div class="step-num">1</div><div>내용</div></div></div>`
   - 코드: `<div class="code-wrap"><div class="code-label">라벨</div><button class="code-copy">복사</button><pre><code>내용</code></pre></div>`
   - 표: `<div class="table-wrap"><table class="ts-table">…</table></div>`
   - 그림: `<div class="figure"><img src="data:image/jpeg;base64,…" alt="그림 1-1" loading="lazy"><div class="figure-spec">캡션</div></div>`
     작은 캡처(가로 400px 미만)는 `<div class="figure figure--narrow">` 로 감쌉니다. 그냥 두면 본문 폭까지 늘어나 뭉개집니다.
6. 캡처를 넣을 때: 이미지를 base64로 바꾸려면 macOS는 `base64 -i 파일.jpg | pbcopy`,
   Windows는 `certutil -encode` 또는 온라인 변환기를 씁니다.
   `figure-placeholder`(점선 상자)는 **작업 중에만** 씁니다. 참가자에게는 제작 메모로 읽히므로
   배포 전에 실제 캡처로 바꾸거나 지웁니다. 같은 이유로 `[확인 필요]` 같은 제작용 표시도 남기지 않습니다.
7. 저장하고 `main`에 푸시하면 끝입니다. 크게 바꿀 때는 브랜치를 만들어 PR로 올리면 Vercel이 미리보기 주소를 붙여 줍니다.

## 주의

- 캡처에 이메일 · 토큰 값 · API 키 값이 보이면 반드시 가리고 넣습니다.
- 결선 크레딧은 운영진이 참가자 콘솔 계정에 직접 넣습니다. 리딤 코드는 문서에 적지 않습니다.
- 원본 캡처를 `media/`에 함께 올려 두면 나중에 다시 쓸 수 있습니다.
