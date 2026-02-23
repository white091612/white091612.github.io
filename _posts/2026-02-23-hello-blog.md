---
title: "GitHub Pages 블로그를 시작하며"
date: 2026-02-23
categories: [blog]
tags: [github-pages, jekyll, 블로그]
excerpt: "Jekyll과 GitHub Pages를 이용해 개발 블로그를 만들었습니다. 블로그 세팅 과정과 앞으로의 계획을 정리합니다."
toc: true
---

## 블로그를 시작한 이유

개발을 하면서 배운 것들을 체계적으로 정리할 공간이 필요했습니다. 
머릿속에만 두면 금방 잊어버리기도 하고, 같은 문제를 반복해서 검색하는 경우도 많았거든요.

> "배움을 기록하는 가장 좋은 방법은 글로 쓰는 것이다."

그래서 GitHub Pages를 이용한 블로그를 시작하게 되었습니다.

## 기술 스택

이 블로그는 다음 기술로 만들어졌습니다:

| 항목 | 기술 |
|------|------|
| 정적 사이트 생성기 | Jekyll |
| 호스팅 | GitHub Pages |
| CI/CD | GitHub Actions |
| 스타일링 | Custom CSS |

### 왜 Jekyll인가?

- GitHub Pages가 공식 지원
- Markdown으로 글 작성 가능
- 커스터마이징이 자유로움
- 많은 한국 개발자들이 사용 → 레퍼런스가 풍부

## 새 글 작성하기

글을 작성하려면 `_posts/` 폴더에 파일을 만들면 됩니다:

```
_posts/YYYY-MM-DD-제목.md
```

파일 상단에 Front Matter를 작성합니다:

```yaml
---
title: "글 제목"
date: 2026-02-23
categories: [카테고리]
tags: [태그1, 태그2]
toc: true
---
```

그 아래에 Markdown으로 본문을 작성하면 끝입니다! ✍️

## 코드 블록 예시

Jekyll은 코드 하이라이팅을 기본 지원합니다:

```python
def hello_blog():
    """첫 번째 블로그 포스트!"""
    print("Hello, World! 🚀")
    return "블로그 시작!"

if __name__ == "__main__":
    hello_blog()
```

```javascript
// JavaScript도 지원합니다
const blog = {
  name: "White's Dev Blog",
  engine: "Jekyll",
  hosting: "GitHub Pages",
};

console.log(`Welcome to ${blog.name}!`);
```

## 앞으로의 계획

- [ ] 개발 관련 학습 노트 정리
- [ ] 프로젝트 회고록 작성
- [ ] 유용한 팁 & 트릭 공유
- [ ] TIL (Today I Learned) 시리즈

꾸준히 기록하는 습관을 들이는 것이 목표입니다. 🎯
