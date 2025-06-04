---
layout: post
title:  식별자 난독화
date:   2020-06-04
category: Obfuscation
image: assets/img/blog/blog8.jpg
author: Ryan Adlard
tags: code
---

식별자 난독화란?
식별자(Identifier) 난독화는 프로그래밍 코드에서 함수명, 변수명, 클래스명 등 식별자들을 알아보기 어렵게 바꾸는 작업이다.

예시로 살펴보면
원래 코드:
def calculate_total(price, quantity):
    return price * quantity

난독화 후 코드:
def a(x, y):
    return x * y

또는 좀 더 극단적으로:
def _x3GzQ(a1, b2):
    return a1 * b2

왜 식별자 난독화를 할까?
1.리버스 엔지니어링 방지
코드가 공개되거나 유출되었을 때, 식별자가 직관적이면 해커가 코드를 쉽게 이해할 수 있다.

calculate_total()이라는 이름은 무슨 일을 하는지 바로 알 수 있지만, x3GzQ()는 추측하기 어렵다.

2.소프트웨어 보안 강화
핵심 로직을 보호하여 불법 복제, 해킹, 취약점 분석을 어렵게 만든다.

3.지적 재산 보호
독창적인 알고리즘이나 로직을 다른 사람이 쉽게 훔쳐서 사용하는 걸 방지한다.

어떻게 수행하나?
자동화된 도구를 통해 식별자를 무작위 문자열로 바꾼다.

예시 도구:
JavaScript: UglifyJS

Python: pyarmor, obfuscator

Java: ProGuard

.NET: Dotfuscator

주의사항
디버깅 어려움: 난독화된 코드는 사람이 보기 어렵기 때문에 버그 수정이나 유지보수가 힘들 수 있다.

완전한 보안 아님: 난독화는 장애물일 뿐, 뚫을 수 없는 방패는 아니다. 다른 보안 기법과 함께 사용하는 것이 좋다.

```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Ryan')
#=> prints 'Hi, Ryan' to STDOUT.
```
