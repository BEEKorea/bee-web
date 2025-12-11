# Repository Guidelines

## Project Structure & Module Organization
- Root: `index.html` (production), shared partials `nav.html`, `footer.html` (English under `en/`).
- Pages: Korean in `pages/NNN.html`, English in `en/pages/NNN.html` (use `_base.html` as a template reference).
- Assets: CSS `css/`, JS `js/`, images `images/`, fonts `fonts/`, vendor theme `bootstrap4/`, videos `videos/`.
- Configuration: `js/config.js` contains environment-specific settings (e.g., LMS backend URL).

## Configuration
- `js/config.js` defines `CONFIG.LMS_BASE_URL` for the LMS backend.
- To switch environments, update the URL in this file:
  - Canary: `https://lms-canary.beekorea.org`
  - Production: `https://lms.beekorea.org`

## Workflow: Production Updates & Reverts
- Production-first: changes are pushed directly to production; no local run required.
- 푸쉬: stage all changes, commit, and push to `origin master`.
  - Example: `git add -A && git commit -m "홈페이지 문구 수정" && git push`
  - If no message is given, use a concise, descriptive one from the diff.
- 되돌려: revert production to the previous state.
  - Last commit: `git revert HEAD && git push origin master`
  - Specific commit: `git log --oneline` → copy hash → `git revert <hash> && git push origin master`
- Guardrails: avoid modifying vendor files (`bootstrap4/`, minified assets) unless intentional.

## Coding Style & Naming Conventions
- HTML/CSS/JS with 2-space indent, UTF-8, LF endings.
- File names lowercase-with-hyphens, e.g., `images/banner-4.png`.
- Numbered pages follow `pages/###.html` and mirror in `en/pages/###.html` when applicable.
- Site styles in `css/style.css`; site scripts in `js/script.js` or `js/main.js`.

## Testing Guidelines
- After 푸쉬, manually verify the live site: header/footer includes, images/links, and home page AJAX tables (`/lms/*`).
- Quick responsive spot-check at mobile, tablet, desktop.
- Basic accessibility: meaningful link text; images include `alt`.

## Commit & Pull Request Guidelines
- Commits: small, focused, imperative mood; include path hints (e.g., `pages: update 206.html schedule`). Korean messages are welcome.
- PRs are optional; if used, include summary, affected paths, and screenshots for visible changes. Note KR/EN parity when relevant.

## Agent-Specific Notes
- Korean shorthands understood: “푸쉬” (deploy), “되돌려” (revert). You can also say “열어봐 <경로>”, “수정해줘 <설명>”, “새 파일 만들어 <경로>”, “삭제해 <경로>`”.
- Language: Any user-facing questions and final summaries must be in Korean.
- KR/EN 대응: 어떤 변경이든 해당 페이지/파일에 한국어 또는 영문 대응본이 있으면, 함께 변경 제안하고 동기화 여부를 사용자에게 확인한다.
