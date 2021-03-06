---
layout: post
title: Compile, Build
tags: [compile, build]
---

* 컴파일러 (Compiler)  
컴파일러는 특정 프로그래밍 언어로 쓰여 있는 문서르 다른 프로그래밍 언어로 옮기는 프로그램을 만ㄹ한다. 원래의 문서를 소스코드 혹은 원시 코드라고 부르고, 출력된 문서를 목적 코드라고 부른다. 목적 코드는 주로 다른 프로그램이나 하드웨어가 처리하기에 용이한 형태로 출력되지만 사람이 읽을 수 있는 문서 파일이나 그림 파일 등으로 옮기는 경우도 있다. 원기 코드에서 목적 코드로 옮기는 과정을 컴파일이라고 한다.
컴파일러는 소스 프로그램을 읽어서 즉시 결과를 출력하는 인터플터와는 구분된다. 그러나 현대에 들어 많은 인터프리터가 JIT 컴파일 등의 기술로 실시간 컴파일을 수행하므로, 컴파일러와 인터프리터 사이의 기술적 구분은 사라져 가는 추세이다.
소스 코드를 컴파일하는 이유는 대부분 사람에게 이해하기 쉬운 형태의 고수준 언어로부터 실행가능한 기계어 프로그램을 만들기 위해서이다. 좁은 의미의 컴파일러는 주로 고수준 언어로 쓰인 소스 코드를 저수준 언어(어셈들리어, 기계어 등)로 번역하는 프로그램을 가리킨다.

* 컴파일러의 실행 단계  
구문 분석: 소스코드 파일을 읽어 개별 문법요소(연산자, 괄호, 식별자 등) 단위로 자른후, 이 문법요소들을 해석하여 추상 구문 트리를 생성한다. 이 과정에서 문법에 맞지 않는 소스 코드느 ㄴ사용자에게 알려준다.
최적화: 추상 구문 트리를 분석햐여 최적화를 수행한다. 도달할 수 없는 코드를 식별하거나, 상수 표현식을 미리 계산해 두거나, 루프 풀기 등의 대부분의 최적화가 이 단계에서 수행된다.
코드 생성: 최적화된 구문 트리로부터 목적 코드를 생성한다. 목표 언어가 기계어일 경우, 레지스터 할당, 연산 순서 바꾸기 등 하드웨어에 맞는 최적화가 이 단계에서 수행된다. 대부분의 하드웨어 최적화 알고리즘은 NP 복잡도를 갖지만, 휴리스틱을 통해 많은 최적화가 수행된다.
링킹: 목적 코드가 기계어 일 경우, 여러 라이브러리 목적 코드를 묶어 하나의 실행 파일을 생성하게 된다. 이 과정은 링커에 의해 수행되며, 어떤 사람들은 링커를 컴파일러의 일부로 간주하지 않기도 한다.

출처: https://ko.wikipedia.org/wiki/%EC%BB%B4%ED%8C%8C%EC%9D%BC%EB%9F%AC

* 빌드 (Build)  
빌드는 소스코드를 실행가능한 소프트웨어 산출물로 만드는 과정 혹은 결과를 의미한다.위의 컴파일러의 실행 단계에서 목적코드들을 묶어 하나의 실행 파일을 생성하는 것을 의미한다.
