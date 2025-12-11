# BEE Korea Website

Official website for BEE Korea (Biblical Education by Extension).

BEE Korea 공식 웹사이트 (성경적 확장 교육).

## Live Site / 라이브 사이트

https://beekorea.org

## Overview / 개요

This is a static website built with HTML, CSS, and JavaScript. It uses Bootstrap for styling and jQuery for interactivity. The site is available in both Korean and English.

HTML, CSS, JavaScript로 구축된 정적 웹사이트입니다. 스타일링에는 Bootstrap을, 상호작용에는 jQuery를 사용합니다. 한국어와 영어로 제공됩니다.

## Hosting Architecture / 호스팅 아키텍처

**English:**

This repository serves the main website at `www.beekorea.org` (or `beekorea.org`) via GitHub Pages. The static content (HTML, CSS, JavaScript, images) is hosted and delivered from this repository.

The Learning Management System (LMS) at `www.beekorea.org/lms` is served by a separate server and is not part of this repository. The static site includes links and AJAX calls to `/lms/*` endpoints that connect to the external LMS server.

**한국어:**

이 저장소는 GitHub Pages를 통해 `www.beekorea.org` (또는 `beekorea.org`)의 메인 웹사이트를 제공합니다. 정적 콘텐츠(HTML, CSS, JavaScript, 이미지)는 이 저장소에서 호스팅되고 제공됩니다.

`www.beekorea.org/lms`의 학습 관리 시스템(LMS)은 별도의 서버에서 제공되며 이 저장소의 일부가 아닙니다. 정적 사이트에는 외부 LMS 서버에 연결되는 `/lms/*` 엔드포인트로의 링크와 AJAX 호출이 포함되어 있습니다.

## Project History / 프로젝트 역사

**English:**

- **2020-2025**: Website was hosted on AWS CodeCommit and deployed to AWS infrastructure
- **2025**: Migrated to GitHub and GitHub Pages for hosting and deployment
- **2025-present**: Development workflow relies almost exclusively on AI assistance (Claude Code) for making changes and updates

**한국어:**

- **2020-2025**: 웹사이트는 AWS CodeCommit에서 호스팅되고 AWS 인프라에 배포되었습니다
- **2025**: GitHub 및 GitHub Pages로 마이그레이션하여 호스팅 및 배포를 진행합니다
- **2025-현재**: 개발 워크플로우는 변경 및 업데이트를 위해 거의 전적으로 AI 지원(Claude Code)에 의존합니다

## Project Structure / 프로젝트 구조

```
bee-web/
├── index.html              # Korean homepage / 한국어 홈페이지
├── nav.html               # Shared navigation header / 공통 네비게이션 헤더
├── footer.html            # Shared footer / 공통 푸터
├── pages/                 # Korean content pages / 한국어 콘텐츠 페이지
│   └── NNN.html          # Numbered pages / 번호가 매겨진 페이지
├── en/                    # English version / 영어 버전
│   ├── nav.html
│   └── pages/
├── css/                   # Stylesheets / 스타일시트
├── js/                    # JavaScript files / JavaScript 파일
├── images/                # Images and graphics / 이미지 및 그래픽
└── fonts/                 # Custom fonts / 커스텀 폰트
```

## Deployment Workflow / 배포 워크플로우

This project uses GitHub Pages for automatic deployment.

이 프로젝트는 자동 배포를 위해 GitHub Pages를 사용합니다.

### Making Changes / 변경사항 작성

**English:**

**Primary Workflow (AI-Assisted):**

1. Open Claude Code in this directory:
   ```bash
   claude
   ```
2. Instruct Claude to make the desired changes. Examples:
   - "Update the footer to say 'All rights reserved!'"
   - "Add a new page about our programs"
   - "Change the banner image on the homepage"
3. Claude will edit files, commit changes, and push to GitHub automatically
4. Verify deployment at https://beekorea.org after 1-2 minutes

**Alternative Workflow (Manual):**

1. Edit files locally using your preferred editor
2. Test locally by opening `index.html` in your browser (optional)
3. Commit your changes:
   ```bash
   git add .
   git commit -m "Brief description of changes"
   ```
4. Push to GitHub:
   ```bash
   git push github master
   ```

**한국어:**

**주요 워크플로우 (AI 지원):**

1. 이 디렉토리에서 Claude Code를 실행합니다:
   ```bash
   claude
   ```
2. Claude에게 원하는 변경사항을 지시합니다. 예시:
   - "푸터를 'All rights reserved!'로 업데이트해줘"
   - "프로그램에 대한 새 페이지를 추가해줘"
   - "홈페이지 배너 이미지를 변경해줘"
3. Claude가 파일을 편집하고 변경사항을 커밋하고 GitHub에 자동으로 푸시합니다
4. 1-2분 후 https://beekorea.org 에서 배포를 확인합니다

**대체 워크플로우 (수동):**

1. 선호하는 편집기로 로컬에서 파일을 편집합니다
2. 브라우저에서 `index.html`을 열어 로컬에서 테스트합니다 (선택사항)
3. 변경사항을 커밋합니다:
   ```bash
   git add .
   git commit -m "Brief description of changes"
   ```
4. GitHub에 푸시합니다:
   ```bash
   git push github master
   ```

### Automatic Deployment / 자동 배포

**English:**

- GitHub Pages automatically builds and deploys when you push to the `master` branch
- Deployment takes 1-2 minutes
- Check deployment status: [GitHub Actions](https://github.com/BEEKorea/bee-web/actions)

**한국어:**

- `master` 브랜치에 푸시하면 GitHub Pages가 자동으로 빌드 및 배포합니다
- 배포에는 1-2분이 소요됩니다
- 배포 상태 확인: [GitHub Actions](https://github.com/BEEKorea/bee-web/actions)

## Remote Repositories / 원격 저장소

This project is synced with two remote repositories:

이 프로젝트는 두 개의 원격 저장소와 동기화됩니다:

**English:**

- `github` - GitHub (used for deployment via GitHub Pages)
- `origin` - AWS CodeCommit (original repository)

For deployments, only push to GitHub:
```bash
git push github master
```

**한국어:**

- `github` - GitHub (GitHub Pages를 통한 배포에 사용)
- `origin` - AWS CodeCommit (원본 저장소)

배포의 경우 GitHub에만 푸시합니다:
```bash
git push github master
```

## Common Tasks / 일반적인 작업

### Update a page / 페이지 업데이트

**English:**

1. Find the page in `pages/` or `en/pages/`
2. Edit the HTML file
3. Commit and push to GitHub

**한국어:**

1. `pages/` 또는 `en/pages/`에서 페이지를 찾습니다
2. HTML 파일을 편집합니다
3. 커밋하고 GitHub에 푸시합니다

### Add images / 이미지 추가

**English:**

1. Place images in the `images/` folder
2. Reference them in HTML: `/images/your-image.png`
3. Commit and push

**한국어:**

1. `images/` 폴더에 이미지를 넣습니다
2. HTML에서 참조합니다: `/images/your-image.png`
3. 커밋하고 푸시합니다

### Update navigation or footer / 네비게이션 또는 푸터 업데이트

**English:**

1. Edit `nav.html` or `footer.html`
2. Changes apply to all pages automatically
3. Commit and push

**한국어:**

1. `nav.html` 또는 `footer.html`을 편집합니다
2. 변경사항이 모든 페이지에 자동으로 적용됩니다
3. 커밋하고 푸시합니다

## Notes / 참고사항

**English:**

- **Language parity**: If you update Korean content, consider updating the English version in `en/`
- **LMS integration**: The site includes links to `/lms/*` which connects to a separate Learning Management System
- **Cache busting**: The nav/footer includes version parameters to ensure fresh content loads

**한국어:**

- **언어 동등성**: 한국어 콘텐츠를 업데이트하는 경우 `en/`의 영어 버전도 업데이트하는 것을 고려하세요
- **LMS 통합**: 사이트에는 별도의 학습 관리 시스템에 연결되는 `/lms/*` 링크가 포함되어 있습니다
- **캐시 무효화**: nav/footer에는 새로운 콘텐츠가 로드되도록 버전 매개변수가 포함되어 있습니다

## Additional Resources / 추가 리소스

**English:**

- Check the [CLAUDE.md](./CLAUDE.md) file for detailed project guidelines
- Review recent commits for examples: `git log --oneline`
- Visit the live site to see your changes after deployment

**한국어:**

- 자세한 프로젝트 지침은 [CLAUDE.md](./CLAUDE.md) 파일을 확인하세요
- 최근 커밋을 검토하여 예제를 확인하세요: `git log --oneline`
- 배포 후 라이브 사이트를 방문하여 변경사항을 확인하세요
