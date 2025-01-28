---
layout: default
title: "Jekyll 테마와 레이아웃 커스터마이징 가이드"
date: 2024-01-28 15:00:00 +0000
categories: tutorial
---

# Jekyll 테마와 레이아웃 커스터마이징 가이드

이 포스트에서는 Jekyll 블로그의 테마와 레이아웃을 커스터마이징하는 방법에 대해 상세히 알아보겠습니다.

## 1. Jekyll의 디렉토리 구조 이해하기

Jekyll 사이트의 기본 디렉토리 구조는 다음과 같습니다:

```
jekyll_blog/
├── _config.yml        # 설정 파일
├── _layouts/         # 레이아웃 파일들
├── _includes/        # 재사용 가능한 부분 템플릿
├── _posts/           # 블로그 포스트
├── _sass/           # Sass 부분 파일들
└── assets/          # 정적 파일들 (이미지, CSS, JS 등)
```

## 2. _config.yml 설정하기

사이트의 기본 설정은 _config.yml 파일에서 관리합니다:

```yaml
title: 나의 Jekyll 블로그
description: 웹 개발과 프로그래밍에 대한 이야기
baseurl: ""
url: "https://yourblog.com"
theme: minima

# 블로그 설정
permalink: /:year/:month/:day/:title/
paginate: 5

# 소셜 미디어 링크
social:
  github: yourusername
  twitter: yourusername
  linkedin: yourusername
```

## 3. 레이아웃 커스터마이징

### 기본 레이아웃 (default.html)

레이아웃은 _layouts 디렉토리에 저장되며, HTML과 Liquid 템플릿 문법을 사용합니다:

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>{{ page.title }}</title>
    <link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">
</head>
<body>
    <header>
        {% include header.html %}
    </header>
    
    <main>
        {{ content }}
    </main>
    
    <footer>
        {% include footer.html %}
    </footer>
</body>
</html>
```

## 4. Sass/SCSS를 사용한 스타일링

Jekyll은 Sass/SCSS를 기본적으로 지원합니다. _sass 디렉토리에 스타일 파일을 만들어보세요:

```scss
// _sass/_variables.scss
$primary-color: #2c3e50;
$secondary-color: #3498db;
$text-color: #333;

// _sass/_layout.scss
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.post {
    margin-bottom: 2em;
    padding: 20px;
    background: white;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
```

## 5. 포스트 메타데이터 활용하기

포스트에서 사용할 수 있는 다양한 메타데이터:

```yaml
---
layout: post
title: "포스트 제목"
date: 2024-01-28 15:00:00 +0900
categories: [jekyll, tutorial]
tags: [웹개발, 블로그]
author: "작성자 이름"
image: "/assets/images/cover.jpg"
description: "포스트에 대한 간단한 설명"
---
```

## 6. 유용한 플러그인 추천

Jekyll 사이트를 향상시키는 추천 플러그인들:

1. jekyll-seo-tag: SEO 최적화
2. jekyll-sitemap: 사이트맵 생성
3. jekyll-feed: RSS 피드 생성
4. jekyll-paginate: 페이지네이션
5. jekyll-archives: 카테고리/태그 아카이브

Gemfile에 플러그인 추가하기:

```ruby
group :jekyll_plugins do
  gem 'jekyll-seo-tag'
  gem 'jekyll-sitemap'
  gem 'jekyll-feed'
  gem 'jekyll-paginate'
end
```

## 7. 반응형 디자인 적용하기

미디어 쿼리를 사용한 반응형 디자인 예시:

```scss
// 모바일 우선 접근
.container {
    width: 100%;
    padding: 15px;
}

// 태블릿
@media (min-width: 768px) {
    .container {
        max-width: 720px;
        padding: 20px;
    }
}

// 데스크톱
@media (min-width: 1024px) {
    .container {
        max-width: 960px;
        padding: 30px;
    }
}
```

## 8. 성능 최적화 팁

1. 이미지 최적화
2. 불필요한 플러그인 제거
3. 캐싱 설정
4. 압축된 에셋 사용

```yaml
# _config.yml
sass:
    style: compressed # CSS 압축
    sass_dir: _sass
```

## 9. 사용자 경험 향상을 위한 팁

1. 검색 기능 추가
2. 관련 포스트 표시
3. 소셜 미디어 공유 버튼
4. 댓글 시스템 통합 (Disqus 등)
5. 다크 모드 지원

## 마무리

Jekyll의 진정한 강점은 그 유연성에 있습니다. 이 가이드를 통해 여러분만의 독특한 블로그를 만드는데 도움이 되길 바랍니다. 추가 질문이나 의견이 있다면 댓글로 남겨주세요!