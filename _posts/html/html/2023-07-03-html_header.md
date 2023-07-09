---
layout: single
title:  "[HTML]-<head>에 들어갈 것들"
categories:
    - HTMLCSS
tag: [html, css,]
---

<h4 class='notice--info'>:label: head 태그에 들어가는 것들</h4>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    !! 이곳에 채울 것들이셈
</head>
<body>
    요긴 다 알잖슴
</body>
```

## CSS 파일들

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="stylesheet" href="style.css">
    <!-- 같은 위치의 'style.css'파일 참조하셈 -->

    <link rel="stylesheet" href="css/style.css">
     <!-- 현 HTML 파일과 같은 위치에 있는 css폴더 안에 있는 style.css 파일을 참조하셈 -->

     <link rel="stylesheet" href="/css/style.css">
     <!-- 메인 파일부터 시작해서 ex) main/css/style.css 파일을 참조하셈 -->
</head>
```

css파일을 첨부할 수 있다. <BR>

물론 **자바스크립트**를 첨부 할 수 있다.

## CDN
```html
<!DOCTYPE html>
<html lang="en">
<head>
 
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
    <!-- google font -->


    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js" integrity="sha512-16esztaSRplJROstbIIdwX3N97V1+pZvV33ABoG1H2OyTttBxEGkTsoIVsiP1iaTtM8b3+hu2kB6pQ4Clr5yug==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
    <!-- library -->
</head>
```
각종 cdn을 첨부하여 참조 할 수 있게 해준다.

## style 태그
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <style>
        /* 스타일을 써줄 수 있으셈     */
    </style>
</head>

<body>
    <style>
        /* 스타일을 써줄 수 있으셈     */
    </style>
</body>
```
혼자 연습할때 css파일 만들기 귀찮으면 style태그를 열어서 
작성하는게 좋더라.

참고 <BR>
body태그 안에서도 동작은 하는데  브라우저는 html파일을 **위에서 부터** 읽기 때문에 잠깐 깨질 수도 있다.

## 사이트 제목
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>사이트 제목</title>
</head>
```
부라우저 탭에 뜨는 이름
{: .notice--info}

## 여러가지 meta태그들
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- 사이트 인코딩 방식 -->

    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- 반응형 만들때 사용, 전자기기로 접속시 스마트폰
     기기의 실제 가로폭을 보고 렌더링하라는 명령어 -->

    <meta name="description" content="웃는게 이쁜사람">
    <!--사이트의 검색결과 화면에 띄워지는 글귀를 수정 하고 싶을 때 사용한다. 
    description은 구글 검색시 파란 제목으로 뜨는 것-->

    <meta name="keywords" content="HTML,CSS,JavaScript,자바스크립트,코딩">
  <!--keywords는 검색에 도움을 주는 키워드 등등이다.-->

</head>
```
## OPEN GRAPH
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta property="og:image" content="/이미지경로.jpg">
  <meta property="og:description" content="사이트설명">
  <meta property="og:title" content="사이트제목">
</head>
```
카톡으로 url을 보내면 뜨는 형식이다.


![OPEN GRAPH SAMPLE](/assets/images/jekyll/230703_03/230703_03_01.png){: width="50%"}

## Favicon
```html
<!DOCTYPE html>
<html lang="en">
<head>
    
    <link rel="shortcut icon" href="../images/logo/title_logo.png" type="image/x-icon">

    <!-- 내 포폴에서 쓰는 파비콘이다.  -->
</head>
```
![favicon](/assets/images/jekyll/230703_03/230703_03_02.png){: width="50%"}

> 아직 공부한지 1년채 안됬습니다. 부족한 점이 있다면 댓글로 **'비판','지적'** 과 반드시 :fire: **feedback** 주시면 감사하겠습니다.
