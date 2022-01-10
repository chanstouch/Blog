---
title: nlp-intro3
description: 임베딩Embedding
slug: nlp-intro3
img: not-yet-generated.png
datetime: 2021.11.25.
category: NLP
author: 정 찬


---



**nlp-intro2**에서 간단하게 딥러닝이 무엇인지, 통계적 방법론의 한계를 어떻게 넘을 수 있는지 이야기했습니다. 이 과정에서 **Embedding** 개념을 곁들였는데요. 구체적으로 어떻게 구현되는지 **차원축소**와 대표적인 **Word Embedding** 기법에 대해 설명하겠습니다. Staff 정윤님께서 Embedding 기법에 대한 분류와 Word2Vec, GloVe 구현을 해 두셨기 때문에 다루지 않은 기법 위주로 설명하겠습니다.



## Index

1. **차원 축소Dimensionality Reduction**

   1.1. 유사도Similarity

   1.2. 차원 축소 기법들

   1.3. 차원 축소의 이점

2. **Word Embedding**

   2.1. 임베딩Embedding 개념 되짚기

   2.2. 임베딩 분류

   2.3. 간단한 임베딩 구현



## 1.  차원 축소Dimensionality Reduction

**Embedding**을 배우면서 **"차원을 줄인다"**는 표현을 사용했죠? NLP에서는 벡터의 길이가 길어질 수록, 즉 vocabulary의 단어가 많아질 수록 계산이 어려운 단점이 있었습니다. 그렇다면 어떻게 줄일 수 있을까요? 바로 대표적인 차원축소 방법인 주성분 분석Principal Component Analysis입니다.





### 1.1. 주성분 분석Principal Component Analysis

이름에서 알 수 있듯이 주요한 성분이 무엇인지 알아내는 방법입니다. 예컨대 3차원에서 2차원으로 차원을 낮출 때, 어떤 데이터를 기준으로 해야 원래 구조를 가장 잘 유지할 수 있을까요?

![차원축소 그래프로 이해하기](./nlp-intro3/pca1)

[사진출처](https://angeloyeo.github.io/2019/07/27/PCA.html)

위 그래프가 대강 x, y축을 갖는 2차원 평면이라고 합시다. 그러면 노란색 긴 선이 어떻게 그어지냐에 따라서 점들과 갖는 오차가 달라집니다. 

> ...? 이거 회귀분석 아닌가요..?

Bravo~ 정답입니다. 

정사영? 내적?

https://angeloyeo.github.io/2019/07/27/PCA.html





### 1.2. 유사도Similarity

유사도Similarity는 "비슷한 + 정도"입니다. 하지만 우리에게 주어진 데이터는 0과 1로 이루어진, 그저 빈도만 알 수 있는 데이터입니다. 이때 우리는 대표적인 차원축소 방법인 주성분 분석Principal Component Analysis으로 유사도를 알 수 있습니다.









**이거 아마 word2vec**

우리는 살아오면서 어떤 대상들에게 의미를 부여하고, 비슷한 것 끼리 분류합니다. 예컨대 사과는 오렌지, 포도와 유사하게 시큼 달달하며, 나무의 꽃이 맺힌 다음에 생깁니다. 하지만 렌치🔧와는 조금 내외하는 사이입니다. 이처럼 우리는 분류를 통해 단어들이 가까운지, 먼지 유사도를 판단합니다.



하지만 one-hot vector에서는 그냥 존재 하면 1로 표현하면 그 의미까지 파악할 수 없었습니다. 하지만 우리는 그 단어들 주변에 어떤 단어들이 같이 나오는지 그 빈도를 확인하면서 유사도를 파악할 수 있습니다.

예를 들어

> 나는 __________________ 스무디를 마시고 싶다.

자, 여기서 _________________에 들어갈 수 있는 단어는? 사과, 오렌지, 포도, 매실 정도가 있겠네요. 그렇다면 저런 문장 구조일 때, 밑줄에 들어가는 단어들의 빈도를 파악하면 비슷하다고 판단할 수 있습니다.



글이나 문서의 유사도는 각각이 어떤 방법으로 수치화 했는지, 문서간의 차이나 유사도를 어떻게 계산했





[차원축소](https://goofcode.github.io/similarity-measure)

https://velog.io/@jekim5418/NLP-Word-Embedding

https://kh-kim.gitbook.io/natural-language-processing-with-pytorch/00-cover-5/02-dimension-reduction

https://hellchujang.tistory.com/15

https://wiserloner.tistory.com/1362





**하지만 인공신경망을 이용한 딥러닝**은 단어나 구문이 문단 내에서 어떻게 사용되는지 직접 관찰하면서 <u>의미를 학습할 수 있습니다</u>. 즉, 미리 의미를 정해주지(supervised learning) 않아도 알아서 학습합니다. 많은 데이터를 학습시키면, 신경망 안에서 단어의 의미와 관계, 맥락을 학습합니다. 이렇게 컴퓨터에게 언어를 이해시키는 과정을 ?????????이라고 합니다.

https://jiho-ml.com/weekly-nlp-13/ 참고하기 4,5,6,7,9,10,11,12,13,14,17

> 나는 사과



### 1.1. 유사도





### 1.2. 차원 축소 기법들





### 1.3. 차원 축소의 이점





## 2. Word Embedding



### 2.1. 임베딩Embedding 개념 되짚기





### 2.2. 임베딩 분류





### 2.3. 간단한 임베딩 구현









누군가는 또 이런 의문이 드시겠군요.

> 아니~ 그럼 임계점은 어떻게 정하는데요!

[딥러닝을 이용한 자연어처리-1](https://www.blog.cosadama.com/deep-learning-from-scratch2-1) 보시면, ReLU, Sigmoid 관련한 내용이 있으니 한번 확인해 보시면 좋을 것 같습니다:)

(신경망 학습이나 뉴런을 여러 겹 쌓으면(다층 퍼셉트론) 학습하기 어렵기 때문에 고안된 오차역전파법 등은 나중에 설명 드리겠습니다.)





[임베딩 개념](https://heehehe-ds.tistory.com/entry/NLP-%EC%9E%84%EB%B2%A0%EB%94%A9embedding)

[임베딩 종류](https://heehehe-ds.tistory.com/entry/NLP-%EC%9E%84%EB%B2%A0%EB%94%A9Embedding-%EB%B0%A9%EC%8B%9D%EC%9D%98-%EC%A2%85%EB%A5%98?category=848536)

[임베딩 분류](https://ebbnflow.tistory.com/249)

[간단한 코드구현](https://dacon.io/codeshare/1847)
