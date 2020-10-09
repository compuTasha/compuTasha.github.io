---
title:  "수리통계학, Ch 1-1"
excerpt: "probability set function"

categories:
  - Math
tags:
  - statistics
  - mathematical_statistics
last_modified_at: 2020-10-09T08:06:00-05:00
---


# Chapter 1 Probability and Distribution

### chapter 1 개요

1.1 ~ 1.4 : 확률

1.5 ~ 1.10 : 확률 변수를 통한 확률 분포 이야기

---

# 1.0 Concepts

## set function

- function : 어떤 것을 어떤 것으로 옮겨 주는 존재 (mapping, rule)
- set function : 집합을 어떤 값으로 옮겨 주는 function
- **probability set function : set을 0에서 1사이의 값으로 옮겨 주는 function**

## domain def.

- ex) f(x) = x+1

    실수 → 실수 : domain은 실수들의 집합

- set function 예시
    1. f(집합) = # of 집합

        f({1,2}) = 2, f({1,5,7}) = 3

        집합 → 자연수 U {0} : **domian은 집합의 집합**

    2. 길이

        f({x|1≤x≤2}) = 1 

        집합 → 실수 

    3. 넓이

        f({(x,y)|1≤x≤2, 2≤y≤3}) = 1

        집합 → 실수, 사각형 안 점들의 집합을 넓이 1로 대응

## probability set function def.

- 확률 함수 : **집합(사건)을 확률값으로 옮겨 주는 함수**, **set → probability**

    ex) f({앞면}) = $\frac 12$ 

## probability set function expression

![%E1%84%89%E1%85%AE%E1%84%85%E1%85%B5%E1%84%90%E1%85%A9%E1%86%BC%E1%84%80%E1%85%A8%E1%84%92%E1%85%A1%E1%86%A8%20ch%201-1%20fc39b43f755a4c8391c0d8e653a0bfa8/Untitled.png](%E1%84%89%E1%85%AE%E1%84%85%E1%85%B5%E1%84%90%E1%85%A9%E1%86%BC%E1%84%80%E1%85%A8%E1%84%92%E1%85%A1%E1%86%A8%20ch%201-1%20fc39b43f755a4c8391c0d8e653a0bfa8/Untitled.png)

- f({H}) = $\frac 12$  를 **{H} → $\frac 12$**  로 표현
    - 함숫값이 확률이라는 것을 강조하기 위해서 나중에는 f 대신 **P** 로 표현한다

    ---

---

# 1.1 Introduction

## 1.1 introduction from book

- 여러 가지 조사 연구는 본질적으로 동일한 조건에서의 반복 실험이 대체적으로 표준이 된다는 것이 특징이다. 예를 들어, 의학 연구에서는 복용된 약의 효과에 관심이 있을 것이며, 경제학자는 여러 시간적 구간(time interval)에서 세 가지 특정 필수품의 가격에 관심이 있을 것이고, 농경학자는 화학 비료가 양곡 생산에 미치는 효과를 연구하고자 할 것이다. 연구자가 이와 같은 정보를 이끌어 낼 수 잇는 유일한 방법은 실험이다. 실험은 **outcome(실현값)**을 결과로 얻는데, outcome이 실험의 실행 전에는 정확히 예측할 수 없다는 것이 실험의 특징이다.
- outcome을 정확히 예측할 수 없는 한 가지 실험을 생각해 보자. 그러나 이 실험에는 가능한 모든 outcome들의 집합을 실험의 실행에 앞서서 기술할 수 있다고 생각하자. 만일 이와 같은 실험을 같은 조건에서 반복할 수 있다면 이를 **random experiment(확률실험)**이라 하고, 가능한 모든 outcome들의 집합을 experiment space(실험공간) 또는 **sample space(표본공간)**라 한다.

## probability

- 확률 혹은 가능성 (0~1로 표현)
- probability가 주어지기 위한 상황 : random experiment

## random experiment

- 시행 전에는 그 결과를 예측할 수 없지만, 가능한 결과들의 집합은 알 수 있는 실험

    ex) 동전 던지기, H인지 T인지 알 수는 없지만 일단 결과는 둘 중에 하나임

## outcome, sample space

- outcome : random experiment를 시행하여 얻은 결과
- sample space : 이런 가능한 모든 outcome들의 집합, the collection of every possible outcome

## Example 1.1.2

![%E1%84%89%E1%85%AE%E1%84%85%E1%85%B5%E1%84%90%E1%85%A9%E1%86%BC%E1%84%80%E1%85%A8%E1%84%92%E1%85%A1%E1%86%A8%20ch%201-1%20fc39b43f755a4c8391c0d8e653a0bfa8/Untitled%201.png](%E1%84%89%E1%85%AE%E1%84%85%E1%85%B5%E1%84%90%E1%85%A9%E1%86%BC%E1%84%80%E1%85%A8%E1%84%92%E1%85%A1%E1%86%A8%20ch%201-1%20fc39b43f755a4c8391c0d8e653a0bfa8/Untitled%201.png)

- 해석
    - 빨간 주사위 하나와 흰 주사위 하나를 동시에 던지는 경우, 그 실현값을 순서쌍(ordered pair: 빨간 주사위 점의 개수, 흰 주사위의 점의 개수)이라 하자. 두 주사위를 같은 조건에서 반복하며 던질 수 있다고 가정한다면 이 두 주사위를 던지는 것은 확률 실험이고, 표본공간은 36개의 가능한 순서쌍, 즉 (1,1), ... , (1,6), (2,1), ... , (2,6), ... , (6,6)으로 이루어진다.
- outcome : (1,1), ... , (6,6) = 총 36가지
- sample space = {(1,1), ... , (6,6)}

    sample space의 원소는 총 36개

## event

- 사건: sample space의 부분 집합, a subset of the sample space
- Example 1.1.2 를 참고하면, subset의 개수는 $2^{36}$개

## $\mathcal{C}$, $c$, $C$ expression

$\mathcal{C}$ : sample space

$c$ : $\mathcal{C}$(sample space)의 내부 원소, 즉 outcome

$C$ : $\mathcal{C}$(sample space)의 부분집합, subset of $\mathcal{C}$, 즉 event

## best way to describe random experiment

$\therefore$ 가능한 결과들(outcome)에 대해 가능한 정도(probability)를 알려주는 것 → 확률로써 이 실험을 표현

→ 당연히, 가능한 결과 및 가능성은 실험에 따라 다르다 (상황에 따라서)

---

# 1.2 Set Theory

확률을 함수로 정의하기로 했는데 그 함수의 정의역이 집합이기 때문에 집합부터 짚고 가자

## set = event

- probability theory에서는 사건을 set으로 표현한다
- 앞면이 나올 사건(집합) → {H}

    앞면이 나올 사건(집합)의 확률 → P({H}) 

    앞면이 나올 사건의 확률은 $**\frac 12$  →** P({H}) = $**\frac 12**$ 

- set 연산 결과 → set → 사건

    복잡해 보이는 사건 → 간단한 사건들의 연산 → set들의 연산

---