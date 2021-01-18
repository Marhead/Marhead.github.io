---
title: "[프로그래머스]-3진법뒤집기"
excerpt: "프로그래머스 월간 코드 챌린지 시즌 1 [3진법뒤집기] 문제 해결"

categories:
    - P.S
    - Programmers
tags:
    - p.s
    - python
date: 2021-01-18 16:00:00 +0900
---

## 문제 설명
---
자연수 n이 매개변수로 주어집니다. n을 3진법 상에서 앞뒤로 뒤집은 후, 이를 다시 10진법으로 표현한 수를 return 하도록 solution 함수를 완성해주세요.

제한사항
- n은 1 이상 100,000,000 이하인 자연수입니다.

## 문제 풀이
---
- *10진수*를 *n진수*로 변환 할 때, n으로 나눈 나머지들을 역순 으로 모은 게 *n진수*로 나타낸 수이다.
  - 45 % 3 = 0
  - 15 % 3 = 0
  - 5 % 3 = 2
  - 1 % 3 = 1
  - ==> 1200(3)
- 문제 상황에서는 한번 뒤집어야 하나, 그때그때 나온 값들을 그대로 문자열에 담아두어 숫자로 활용
- 새로 사용하는 메서드
  ```python
  R, Q = divmod(N, n)
  # R 은 몫, Q는 나머지, N은 피연산자, n은 연산자
  ```
  ```python
  int(string_object, n)
  # string_object를 n진수로 받아들여 십진수로 변환함
  ```

## 풀이 코드
---
```python
def solution(n):
    answer = ''

    while n >= 1:
        n, rest = divmod(n, 3)
        answer += str(rest)

    answer = int(answer, 3)

    return answer
```
-----
출처 : [프로그래머스 3진법 뒤집기](https://programmers.co.kr/learn/courses/30/lessons/68935)