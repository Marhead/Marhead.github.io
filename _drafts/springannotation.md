---
title: "๐[Spring]-์คํ๋ง ํ์ต Annotation"
excerpt: "Spring ๋ด๋ถ Annotation ๋ด์ฉ ํ์ต"

categories:
    - Spring
    - Tutorial
tags:
    - frameworks
    - java
    - spring
date: 2021-02-03 05:00:00 +0900
---

```@Controller``` : ์ปจํธ๋กค๋ฌ ์ ์ธ

```@GetMapping``` : ๋งค๊ฐ๋ณ์ ๋ถ๋ฌ์ค๊ธฐ

```@Bean``` : 

```@RequestParam``` : ์๋ ฅ ๋งค๊ฐ๋ณ์

```@ResponseBody``` : html <body>๋ถ๋ถ์ ์ง์  ๋ฐ์ดํฐ๋ฅผ ๋ฃ๊ฒ ๋ค.

```@Test``` : ํ์คํธ ์ผ์ด์ค ์์ฑํ  ๋ ์ฌ์ฉ

xml๋ฐฉ์ = ํ๊ทธ๋ฅผ ๋๋ฒ ํด์ค์ผํจ -> ๋ถํธํจ

==>> ์ต๊ทผ์ json ๋ฐฉ์์ผ๋ก ํต์ผ

HttpMessageConverter -> ๊ฐ์ฒด๋ ์๋์ผ๋ก json

๊ฐ์ฒด -> json 2 library

1. jackson (spring default)
2. Gson

Thymeleaf
```html
<p th:text=""></p> ํ๋ฏธ๋ฆฌํ ๋ฌธ๋ฒ
```



ctrl + p ๋งค๊ฐ๋ณ์ ์ ๋ณด๋ณด๊ธฐ intellij hotkey

ctrl + shift + a : getter and setter ์๋ ์ค์  ๋ถ๋ฌ์ค๊ธฐ

ctrl + shift + enter : ๋ค ์๋์์ฑ

