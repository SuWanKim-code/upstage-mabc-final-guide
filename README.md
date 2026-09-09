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
4. 자주 쓰는 블록
   - 안내 상자: `<div class="callout callout--note">…</div>` (`note` / `tip` / `warn` / `danger`)
   - 단계: `<div class="steps"><div class="step"><div class="step-num">1</div><div>내용</div></div></div>`
   - 코드: `<div class="code-wrap"><div class="code-label">라벨</div><button class="code-copy">복사</button><pre><code>내용</code></pre></div>`
   - 표: `<div class="table-wrap"><table class="ts-table">…</table></div>`
   - 그림: `<div class="figure"><img src="data:image/jpeg;base64,…" alt="그림 1-1" loading="lazy"><div class="figure-spec">캡션</div></div>`
5. 캡처 자리: `figure-placeholder`를 찾으면 점선 상자가 나옵니다. 그 상자를 위 그림 블록으로 바꿉니다.
   이미지를 base64로 바꾸려면 macOS는 `base64 -i 파일.jpg | pbcopy`, Windows는 `certutil -encode` 또는 온라인 변환기를 씁니다.
6. 저장하고 `main`에 푸시하면 끝입니다. 크게 바꿀 때는 브랜치를 만들어 PR로 올리면 Vercel이 미리보기 주소를 붙여 줍니다.

## 주의

- 캡처에 이메일 · 토큰 값 · API 키 값이 보이면 반드시 가리고 넣습니다.
- 결선 크레딧은 운영진이 참가자 콘솔 계정에 직접 넣습니다. 리딤 코드는 문서에 적지 않습니다.
- 원본 캡처를 `media/`에 함께 올려 두면 나중에 다시 쓸 수 있습니다.
