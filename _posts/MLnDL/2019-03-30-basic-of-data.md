---
title : "Basic of data : definition & scale"
category :
  - ML
tag :
  - data
  - data scale
  - basic
sidebar_main : true
author_profile : true
use_math : true
header:
  teaser : https://i.imgur.com/AwkwrNc.jpg
  overlay_image : https://i.imgur.com/AwkwrNc.jpg
published : true
---

데이터는 무엇일까요?

## 1. 데이터란 무엇인가?

유튜브 강의를 찍으려고 자료를 준비하던 중 "데이터란 무엇입니까?" 라는 질문을 생각해보았습니다.
쉬운 질문이지만, 구체적인 정의는 어려웠습니다.

최근 공부하는 분야를 통틀어 표현하자면 Data Science입니다.
기존에 했던 공부들도, 지금하는 공부도 모두 데이터에 관한 학문입니다.

하지만 데이터가 무엇인지를 고민해본적이 없었습니다.
하지만 DS에 있어 데이터에 대한 기본적인 이해는 필수적입니다.

이번에는 가볍게 데이터를 한번 살펴보도록 하겠습니다.

### 1-1. 사전적 정의

![data_image in wiki](https://upload.wikimedia.org/wikipedia/commons/6/6d/Data_types_-_en.svg)

Data를 위키피디아에서는 다음과 같은 정의를 내리고 있습니다.

> Data is a set of values of subjects with respect to qualitative or quantitative variables.

한국에서는 Data를 번역하면 **자료, 정보** 라는 결과를 얻을 수 있습니다. (Oxford)
표준국어대사전에서 자료와 정보의 정의 중 필요한 부분을 가져왔습니다.

**자료**

> [명사] 1.연구나 조사 따위의 바탕이 되는 재료.

**정보**

> [명사]
> 1. 관찰이나 측정을 통하여 수집한 자료를 실제 문제에 도움이 될 수 있도록 정리한 지식. 또는 그 자료.
> 3. **컴퓨터** 어떤 자료나 소식을 통하여 얻는 지식이나 상태의 총량. 정보 원천에서 발생하며 구체적 양.

### 1-2. 정의에서 알 수 있는 포인트

위 영문 정의에서 2가지 부분에서 초점을 둘 수 있습니다.

1. set of values : 데이터는 하나 또는 그 이상으로 이루어짐
2. qualitative or quantitative : 질적, 양적으로 구분할 수 있음

한글 정의에서는 다음과 같은 포인트를 알 수 있습니다.

1. 관찰이나 측정을 통한 수집, 정보 원천 : 정보는 그냥 나오는 것이 아님
2. 도움이 될 수 있도록 정리한 : 정리를 통해 실제 문제에 도움

간단한 포인트지만 이런 포인트들에 대한 이해는 중요합니다. 이제 이런 정의에서부터 간단하게 구분을 해보도록 하겠습니다.

## 2. 데이터의 분류 : 구조적/비구조적

<figure class="half">
    <img src="https://img-prod-cms-rt-microsoft-com.akamaized.net/cms/api/am/imageFileData/RE2zRLE?ver=9a84&q=90&m=2&h=768&w=1024&b=%23FFFFFFFF&aim=true">
    <img src="https://farm1.staticflickr.com/757/22795899224_7608e54874_b.jpg">
    <figcaption>구조적인 RMDB식 데이터 vs 비구조적인 자연 데이터</figcaption>
</figure>

데이터를 가장 크게는 2가지로 나눌 수 있습니다.
하나는 관측, 측정 결과에서 정리를 통해 실제 문제에 바로 사용할 수 있는 **구조적(structured)** 데이터와 그런 전처리 과정이 필요한 **비구조적(unstructured)** 데이터입니다.

비구조적 데이터는 컴퓨터로 분류하기에는 아직 힘든 데이터입니다. 사진, 오디오, 영상, 텍스트 문서 등등이 이에 속합니다.
현실 세계의 대부분 데이터는 비구조적 데이터로 구성되어 있다고 볼 수 있습니다.
이런 비구조적 데이터는 분석을 위해 구조적 데이터로 변환과정(전처리라고 부르는)을 거쳐야 합니다.

구조적 데이터는 보통 테이블 구조, RDMBS 에서 사용할 수 있는 데이터들을 의미합니다.

이에 대해 더 좋은 글은 링크로 남겨두겠습니다. ([structured vs. unstructured data](https://www.datamation.com/big-data/structured-vs-unstructured-data.html))

## 3. 데이터의 분류 : 정량적/정성적

이런 데이터를 다시 분류해보겠습니다.

데이터는 양적(**quantitative**)과 질적(**qualitative**)으로 나눌 수 있습니다.

수치형/범주형 데이터라고도 합니다.
번역에 따라 정량적 데이터, 정성적 데이터라고도 합니다.

### 3-1. 수치형(양적) 데이터

**Quantitative Data** 또는 **Numerical Data** 라고 하며, 수치로 *측정* 가능한 자료입니다.
수치로 표현 가능한 것도 두 가지가 있습니다.

1. **연속형 데이터 (continuous data)** : 말 그대로 값이 끊어지지 않고 연속적으로 이루어지는 데이터
  - 길이, 무게, 온도 등이 이에 속합니다.
2. **이산형 자료 (discrete data)** : 정수로 나누어지는 데이터
  - 주사위 눈금, 횟수 등이 이에 속합니다.

### 3-2. 범주형(질적) 데이터

**Qualitative Data** 또는 **Categorical Data** 라고 합니다. 수치로 측정이 불가능한 자료입니다.
수치로 측정할 수 없는 자료도 두 가지로 나눌 수 있습니다.

1. **명목형 데이터 (nominal data)** : 범주간에 순서 혹은 양적인 의미가 없는 데이터입니다.
  - 혈액형, 종교 등이 이에 속합니다.
2. **순서형 데이터 (ordinal data)** : 범주간에 순서적인 의미가 있는 데이터입니다.
  - 영화 별점, 성적 데이터 등이 이에 속합니다.
  - 헷갈릴 수 있겠지만 별점 5가 4보다 높은 것은 맞지만, 얼마나 더 높은지는 기준에 따라 다른 것입니다.

## 4. 척도/수준 (scale, level)

위에서 데이터에 대한 수량화 여부에 따른 세부 분류 총 4가지를 알아보았습니다.
이 데이터에 대한 정보는 크게 4가지 척도/수준으로 살펴볼 수 있습니다.

본래 **척도** 라는 것은 특성을 수량화하기 위한 수단입니다.
즉, DS에서는 데이터 분석에 용이하게 질적 데이터를 양적 데이터로 변환하는 것을 목표로 합니다.

척도의 종류는 다음과 같습니다.

1. 명목 (nominal)
2. 서열 (ordinal)
3. 등간 (interval)
4. 비율 (ratio)

명목과 서열은 **질적 척도** 에 속하고, **등간과 비율** 은 양적 척도에 속합니다.

이를 더 알아보겠습니다.

### 4-1. 명목 (nominal)

> 자료가 구분이 된다.

<figure>
    <img src="https://i.imgur.com/ObY9C8U.jpg">
    <figcaption>국기는 구분할 수 있지만 비교할 수 없습니다.</figcaption>
</figure>

**명목 척도** 는 단어 그대로 이름(범주)만을 사용합니다. 성별, 국적, 지역, 품사 등등이 이에 속합니다.
수치로 표현할 수 있지만, 그렇다고 수학 연산이 가능한 데이터가 아닙니다.

#### 수학 연산

수치적으로 계산할 수 없으니, 보통 포함 관계나 양적 비교, 비교 연산(equalize) 등을 사용합니다.

#### 대푯값

데이터를 처리하다보면 데이터의 경향을 설명하는 자료가 필요한 경우가 많습니다. NaN 값을 채울 때 더더욱 유용하게 사용됩니다.

이런 명목형 데이터에서 사용할 수 있는 중심값은 가장 많이 있는 데이터, **최빈값** 입니다. 수치로 계산할 수 없으니 제한되는 정도가 많습니다.

### 4-2. 서열 (ordinal)

> 구분을 넘어 비교도 가능하다.

<figure>
    <img src="https://i.imgur.com/1ao6NSq.jpg">
    <figcaption>순위는 비교할 수 있지만, 1등이 2등보다 2배 잘한 것은 아닙니다.</figcaption>
</figure>

**서열 척도** 는 조금 다르게 속성에 따라서 순위를 결정할 수 있는 척도입니다. 명목/서열 척도는 범주형의 데이터 분류와도 비슷합니다. 순서만 유지된다면 원하는 값으로 변경해도 상관이 없습니다.

차이나 간격에 대한 수치적인 계산을 할 수 없습니다.

예시로 1등과 2등, 2등과 3등의 차이는 같을 수 없는 것과 같은 것입니다. 1등이 100등보다 100배 잘하는 것은 아니기 때문입니다.

순위, 만족도, 별점 등등이 이에 속합니다.

#### 수학 연산

순서가 있다는 것은 **비교** 를 할 수 있고, 비교를 할 수 있으면 **정렬** 을 할 수 있습니다.
하지만 비교와 정렬은 절대적인 값의 비교는 불가능하다는 점을 알아야 합니다. 여전히 +/- 등의 가감연산은 불가능합니다.

#### 대푯값

정렬을 할 수 있으니 정렬했을 때, 순서로 중앙에 있는 **중앙값** 을 사용할 수 있습니다.
당연히 **최빈값** 도 사용할 수 있습니다. 절대적인 값을 비교할 수는 없기에 평균값은 사용할 수 없습니다.

별점 등의 데이터에 있어서 평균값을 사용하는 것은 이를 서열 척도가 아닌 등간 척도로 보는 것입니다.

### 4-3. 등간 (interval)

> 각 값의 차이를 측정할 수 있다.

<figure>
    <img src="http://res.freestockphotos.biz/pictures/16/16307-close-up-of-a-white-thermometer-pv.jpg">
    <figcaption>섭씨 온도에서 100도가 200도보다 2배 뜨거운 것은 아닙니다. 하지만 0도와 100도 차이는 100도와 200도 차이와 같습니다.</figcaption>
</figure>

**등간 척도** 는 값 사이에 상대적인 차이가 있어, 비교와 크기 표현을 할 수 있습니다.
여기서는 데이터간의 값 차이가 같다면, 같은 차이를 의미합니다.

연도, 리커트 척도, 섭씨 온도(절대온도는 비율척도가 될 수 있습니다.) 등등이 이에 속합니다.

#### 수학 연산

이제 비교를 포함하여, 가감연산이 가능합니다. 즉, 정량적 연산이 가능합니다.
아직 절대 영점은 없기에 곱셈/나눗셈 연산은 할 수 없습니다. 하지만 산술평균(나눗셈) 연산이 가능합니다.

#### 대푯값

명목, 서열의 특징을 그대로 가지고 있기에 **최빈값, 중앙값** 을 사용할 수 있고, 하지만 이제 절대적인 값이 있으므로 이를 이용해 **산술평균값** 을 사용할 수 있습니다.

### 4-4. 비율 (ratio)

> 비율로 나타낼 수 있다.

<figure>
    <img src="https://images.pexels.com/photos/9352/glass-time-watch-business.jpg?cs=srgb&dl=clock-hours-minutes-9352.jpg&fm=jpg">
    <figcaption>시간은 언제나 절대적인 값을 가지고 있습니다.</figcaption>
</figure>

**비율 척도** 는 포괄적인 정보를 제공하는 최상위 수준의 척도입니다. 데이터 값의 비율이 실제적인 의미를 가집니다.
구분, 비교, 차이, 계산(가감승제 또는 사칙연산) 모두 가능합니다.

시간, 월 소득, 연령, 켈빈온도 등이 이에 속합니다.

#### 수학 연산

비교와 사칙연산 모두 사용가능합니다.

#### 대푯값

최빈값, 중앙값, 산술평균값을 포함하여 **기하평균, 조화평균** 등의 비교적 복잡한 대푯값을 가질 수 있습니다.

또한 위의 네가지 척도를 제외하고 절대 영점과 절대 척도를 가지는 **절대 척도** 도 있다고 합니다.

## 5. Conclusion

데이터 과학 분석 글을 보면 위의 용어들이 많이 나오기에 영어로 알아두는 것도 중요합니다.
각 용어는 번역에 따라 다르게 표현되기도 하기도 하므로 문맥을 따르는 것이 가장 좋습니다.

쓰고 보니 너무 쉬운 이야기를 쓴 것 같지만, 데이터의 기초에 대해 아는 것은 중요하다고 생각합니다. :-)

## Reference

- [structured vs. unstructured data](https://www.datamation.com/big-data/structured-vs-unstructured-data.html)