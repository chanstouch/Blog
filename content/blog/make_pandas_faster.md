---

title: Pandas 빠르게 만드는 방법(feat.판다스_최적화)
description: for문으로 1시간째 기다리고 있다구요?
slug: make-pandas-faster
img: make-pandas-faster.png
datetime: 2022. 01. 26.
category: Pandas
author: 정 찬

---


## Intro

Pandas로 반복 작업을 하다가 시간이 엄청 긴 코드를 발견할 때가 있습니다. 간단한 데이터는 반복문(for)으로 처리해도 시간이 그리 오래 걸리지 않지만, 데이터가 만, 10만, 100만 등 커질수록 굉장히 느려지죠.

> 얼마나 어떻게 느려지는지 보여주기


## 프로그래밍 언어는 어떻게 컴퓨터에 명령을 전달할까?

중앙연산장치CPU, 쉽게 말해 컴퓨터는 실행 명령어가 0과 1로 이루어져 있습니다. '더하기'라는 기능도 10001처럼 기계어 수준에서는 0과 1의 집합입니다.

기계어 명령어는 Intel, AMD 같은 CPU 칩을 만드는 회사들이 만듭니다. 그래서 cpu 회사, 버전, x86, x64 등 아키텍처에 따라 명령어셋이 다를 수 있습니다.

프로그래밍 언어는 우리가 사용하는 말과 유사한 고급 언어로 작성한 소스코드를 OS가 이해하는 0과 1로 된 기계어로 번역해줍니다.

## 인터프리터Interpreter와 컴파일러Compiler

우리가 많이 접하는 프로그래밍 언어는 인터프리터interpreter와 컴파일compile 방식으로 나뉩니다.
- 인터프리터: 
    - 번역 시점: 고급 언어로 작성된 코드를 한 줄씩 번역
    - 수정 용이: 한 줄씩 번역하기 때문
- 컴파일러:
    - 과정: 프로그램 작성 -> 컴파일 -> 실행
    - 번역 시점: 실행 시점에 한 번
파이썬은 인터프리터interpreter 언어입니다. 이름처럼 인터프리터는 소스 코드를 한 줄씩 기계어로 번역합니다. 



1. 반복문1: for, while
2. 반복문2: iterrows()
3. apply()
4. 벡터화1: Pandas Series
5. 벡터화2: Numpy Array


[이곳](https://aldente0630.github.io/data-science/2018/08/05/a-beginners-guide-to-optimizing-pandas-code-for-speed.html)과 [이곳](https://purplechip.tistory.com/44) 그리고 [이곳](https://seong6496.tistory.com/179)을 참고했다.

[cython, numda](https://ichi.pro/ko/pandas-kodeuleul-choejeoghwahagiwihan-jonghab-gaideu-108405235388004)

[](https://towardsdatascience.com/understanding-the-need-for-optimization-when-using-pandas-8ce23b83330c)
[](https://imasoftwareengineer.tistory.com/43)

