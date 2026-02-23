# White's Dev Blog

[![Deploy Jekyll to GitHub Pages](https://github.com/white091612/white091612.github.io/actions/workflows/deploy.yml/badge.svg)](https://github.com/white091612/white091612.github.io/actions/workflows/deploy.yml)

> 🔗 **https://white091612.github.io**

개발 기록과 학습 노트를 정리하는 블로그입니다.

## 🚀 Quick Start

### 새 글 작성하기

`_posts/` 폴더에 `YYYY-MM-DD-제목.md` 형식으로 파일을 만들면 됩니다.

```bash
# 예시
touch _posts/2026-02-24-my-new-post.md
```

파일 상단에 Front Matter를 추가합니다:

```yaml
---
title: "글 제목"
date: 2026-02-24
categories: [dev]
tags: [tag1, tag2]
toc: true        # 목차 표시 여부
---

여기에 Markdown으로 본문을 작성합니다.
```

### 배포하기

```bash
git add .
git commit -m "Add new post: 글 제목"
git push origin main
```

`main` 브랜치에 push하면 GitHub Actions가 자동으로 빌드 & 배포합니다.

### 로컬에서 미리보기 (선택사항)

Ruby가 설치되어 있다면:

```bash
bundle install
bundle exec jekyll serve
# → http://localhost:4000 에서 확인
```

## 📁 프로젝트 구조

```
├── _config.yml          # 사이트 설정
├── _posts/              # 블로그 글 (여기에 글 작성!)
│   └── 2026-02-23-hello-blog.md
├── _layouts/            # 레이아웃 템플릿
│   ├── default.html
│   ├── post.html
│   └── page.html
├── _includes/           # 재사용 컴포넌트
│   ├── header.html
│   ├── footer.html
│   └── toc.html
├── assets/
│   ├── css/main.css     # 스타일시트
│   ├── js/theme.js      # 다크모드 토글
│   └── images/          # 이미지 폴더
├── about.md             # 소개 페이지
├── categories.md        # 카테고리 페이지
├── tags.md              # 태그 페이지
├── index.html           # 메인 페이지
├── Gemfile              # Ruby 의존성
└── .github/workflows/   # GitHub Actions
    └── deploy.yml
```

## ✨ Features

- 🌗 다크/라이트 모드 (시스템 설정 자동 감지)
- 📱 반응형 디자인
- 🏷️ 카테고리 & 태그 시스템
- 📑 자동 목차 (TOC)
- 🎨 코드 구문 강조
- 📰 RSS Feed
- 🔍 SEO 최적화
- ⚡ GitHub Actions 자동 배포
