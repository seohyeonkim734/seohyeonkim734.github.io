---
layout: post
title:  "문자열 암호화"
date:   2020-06-04
category: Obfuscation
image: assets/img/blog/blog6.jpg
author: Ryan Adlard
tags: Jekyll
---

문자열 암호화란?
문자열 암호화는 사람이 읽을 수 있는 평문(plain text)을
읽을 수 없는 암호문(cipher text)으로 변환하여 정보를 안전하게 보호하는 기술입니다.

왜 문자열을 암호화할까?

보안	개인정보, 비밀번호 등 민감한 데이터를 보호
위변조 방지	데이터가 중간에 바뀌었는지 확인 가능
저장 안전성	서버나 DB에 저장 시 노출 방지
통신 안전	네트워크를 통해 전송되는 정보 보호

주의할 점
암호화만으로 완벽한 보안은 아님

키 관리와 저장도 매우 중요함

암호화 알고리즘은 검증된 것을 사용해야 함

```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Ryan')
#=> prints 'Hi, Ryan' to STDOUT.
```
