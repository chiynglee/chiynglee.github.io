---
title:  "github page"
excerpt: "github page를 이용한 블로그 만들기 (no local pc)"
toc: true
toc_sticky: true
categories:
  - Study
tags:
  - Github
  - Jekyll
---
참고 : [GitHub Pages 블로그 따라하기](https://devinlife.com/howto/)

# Github 준비

## Github 가입

[Github](https://github.com) 접속 후, 회원 가입

## 테마를 github repository로 복사

1. Github 로그인
2. [minimal-mistakes](https://github.com/mmistakes/minimal-mistakes)의 github repository에 접속
3. 오른쪽 상단 "Fork" 클릭
4. 복사본을 저장할 github 계정을 선택



# 포스트 작성

## TOC (Table of Contents) 추가

해당 포스트의 목록(차례)을 표기

minimal-mistakes 테마에서는 오른쪽 사이드 바 형태로 출력

해당 포스트 .md 파일의 헤더에 아래 내용 추가
```yaml
toc: true
toc_sticky: true
```
> - TOC : toc 표기 결정
> - toc_sticky : toc 사이드 바를 고정. 작은 화면에서 사이드 바가 화면 밖으로 넘어가 좌우 스크롤이 발생하는 방지

## 스타일 설정

### 포스트 제목 밑에 날짜 표기

참고 : [jekyll 블로그 포스팅 날짜로 바꾸기](https://heoseongh.github.io/gitblog/jekyll-setting-postDate/)

Default : 마지막으로 포스트를 읽은 시간으로부터 얼마나 지났는지를 표기 (예 : less than 1 minute read)

포스팅 날짜를 표기하도록 변경
- 포스트 파일 이름에 있는 날짜를 표기함 (yyyy-mm-dd-title.md)
- 수정할 파일 : `/_config.yml`
- `read_time`을 `false`로 변경
- `show_date: true` 추가

```yaml
# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: false          # 마지막 읽은 시간 표시 제거
      show_date: true           # 포스팅 날짜 표시 추가
      comments: # true
      share: true
      related: true
```

