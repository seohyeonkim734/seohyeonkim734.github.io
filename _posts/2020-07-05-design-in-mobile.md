---
layout: post
title:  Design in Mobile Application
date:   2020-07-05
category: Mobile
image: assets/img/blog/blog-2.jpg
author: Ryan Adlard
tags:
  - app
  - mobile
---

 Junk Code 삽입이란?
Junk Code 삽입(정크 코드 삽입)은 프로그램의 실행에는 영향을 주지 않지만,
코드를 분석하는 사람을 헷갈리게 하기 위해 의미 없는 코드를 일부러 삽입하는 난독화 기법이다.

정의
Junk Code 삽입은 실제 동작에 영향을 미치지 않는 불필요한 코드(무의미한 명령어, 조건, 함수 등)를
의도적으로 추가하여 분석과 해킹을 어렵게 만드는 기법이다.

예시
원래 코드:
c
int sum = a + b;

🧪 Junk Code 삽입 후:
c
int temp = 0;
for (int i = 0; i < 10; i++) {
    temp += i;  // 의미 없음
}
int sum = a + b;

혹은 더 교묘하게:
c
if (a > b || b > a || a == b) {
    // 어떤 경우에도 항상 실행되는 블록
    int noise = 123456;  // 아무 의미 없음
}
int sum = a + b;

목적과 효과
1.리버스 엔지니어링 방해
해커가 코드를 분석하려 할 때, 의미 없는 코드가 많으면 핵심 로직을 찾기 어려워진다.

2.자동 분석 도구 무력화
디컴파일러, 정적 분석기 등이 쓸데없는 코드에 시간을 낭비하게 만든다.

3.코드 흐름 흐리기
진짜 로직과 가짜 로직이 섞이면 분기 조건 판단도 어려워진다.

단점
항목	설명
성능 저하	지나치게 많이 삽입하면 실행 속도가 느려질 수 있음
유지보수 불편	나중에 코드를 수정할 때 분석이 더 힘들어짐
보안 완벽 아님	경험 많은 해커는 Junk Code를 필터링할 수 있음

사용 도구 (예시)
C/C++: Obfuscator-LLVM, Tigress

Python: pyarmor + 수동 삽입

Java: Allatori, Zelix KlassMaster

JavaScript: JavaScript Obfuscator
```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Ryan')
#=> prints 'Hi, Ryan' to STDOUT.
```
