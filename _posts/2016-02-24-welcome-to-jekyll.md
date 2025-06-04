---
layout: post
title: "난독화가 성능에 미치는 영향향"
date: 2025-06-04
category: Obfuscation
image: assets/img/blog/blog-4-scaled-1.jpg
### if need replace preview image for single image add field full_image, ex:
#full_image: assets/img/works/work4.jpg
author: Sarah Rose
tags: Jekyll
---

코드 난독화는 소스 코드의 가독성과 구조를 의도적으로 변경하여 리버스 엔지니어링을 어렵게 만드는 보안 기법이다. 하지만 이런 구조 변화는 프로그램의 실행 성능에도 영향을 미칠 수 있다. 성능 저하 여부는 사용하는 난독화 기법의 종류와 강도, 적용 범위에 따라 달라진다. 

2.주요 원인 분석 

(1) 코드 복잡도 증가 

불필요한 루프와 조건문 삽입 → 분기 예측 실패율 증가 
CPU 처리량 증가 및 디버깅 어려움 

(2) 런타임 연산 증가 

문자열이나 함수명을 동적으로 복호화 
해석기(VM) 기반 난독화는 코드 실행을 느리게 함 

(3) 코드 크기 증가 

중복 코드, Dummy 함수, 무의미한 명령어 삽입 
메모리와 캐시 사용량 증가 

```ruby
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
```

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
