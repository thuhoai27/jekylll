---
layout: default
title: "마크다운 문법 가이드"
date: 2024-01-28 14:00:00 +0000
categories: guide
---

# 마크다운 문법 종합 가이드

이 포스트에서는 Jekyll 블로그에서 사용할 수 있는 다양한 마크다운 문법을 소개합니다.

## 1. 제목 (Headers)

# H1 제목
## H2 제목
### H3 제목
#### H4 제목
##### H5 제목
###### H6 제목

## 2. 강조 (Emphasis)

*이텔릭체*
_이것도 이텔릭체_

**볼드체**
__이것도 볼드체__

***이텔릭+볼드체***
___이것도 이텔릭+볼드체___

~~취소선~~

## 3. 목록 (Lists)

### 순서 있는 목록:
1. 첫 번째 항목
2. 두 번째 항목
3. 세 번째 항목

### 순서 없는 목록:
* 항목 1
* 항목 2
  * 하위 항목 2.1
  * 하위 항목 2.2
* 항목 3

## 4. 링크 (Links)

[Jekyll 공식 웹사이트](https://jekyllrb.com/)
[마크다운 가이드](https://www.markdownguide.org "마크다운 가이드 호버 텍스트")

## 5. 이미지 (Images)

![Jekyll 로고](https://jekyllrb.com/img/logo-2x.png)

## 6. 인용문 (Blockquotes)

> 첫 번째 수준 인용문
>> 두 번째 수준 인용문
>>> 세 번째 수준 인용문

## 7. 코드 (Code)

인라인 코드: 'console.log("Hello World!");'

코드 블록:
'''javascript
function greeting(name) {
    console.log("Hello, " + name + "!");
}
greeting("Jekyll");
'''

## 8. 표 (Tables)

| 제목 1 | 제목 2 | 제목 3 |
|--------|---------|---------|
| 내용 1 | 내용 2 | 내용 3 |
| 행 2   | 열 2   | 값 2   |
| 행 3   | 열 3   | 값 3   |

## 9. 수평선 (Horizontal Rules)

---
***
___

## 10. 작업 목록 (Task Lists)

- [x] 완료된 작업
- [ ] 미완료 작업
- [x] 또 다른 완료된 작업

## 11. 각주 (Footnotes)

각주를 사용한 문장[^1]
다른 각주를 사용한 문장[^2]

[^1]: 첫 번째 각주 설명
[^2]: 두 번째 각주 설명

## 12. 정의 목록 (Definition Lists)

Jekyll
: 정적 웹사이트 생성기

Markdown
: 텍스트 기반의 마크업 언어

## 13. 이모지 (Emoji)

마크다운에서 이모지도 지원됩니다! :smile: :heart: :+1:

## 14. HTML 직접 사용

마크다운에서는 <kbd>Ctrl</kbd> + <kbd>C</kbd>처럼 HTML도 직접 사용할 수 있습니다.

<div style="padding: 20px; background-color: #f0f0f0; border-radius: 5px;">
  HTML로 스타일이 적용된 div 박스입니다.
</div>