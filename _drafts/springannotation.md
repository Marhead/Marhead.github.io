@Controller : 컨트롤러 선언

@GetMapping : 매개변수 불러오기

@Bean : 

@RequestParam : 입력 매개변수

@ResponseBody : html <body>부분에 직접 데이터를 넣겠다.

@Test : 테스트 케이스 작성할 때 사용

xml방식 = 태그를 두번 해줘야함 -> 불편함

==>> 최근은 json 방식으로 통일

HttpMessageConverter -> 객체는 자동으로 json

객체 -> json 2 library

1. jackson (spring default)
2. Gson

Thymeleaf
```html
<p th:text=""></p> 타미리프 문법
```



ctrl + p 매개변수 정보보기 intellij hotkey

ctrl + shift + a : getter and setter 자동 설정 불러오기

ctrl + shift + enter : 뒤 자동완성

