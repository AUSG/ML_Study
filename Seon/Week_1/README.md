# Introduction to Reinforcement Learning

***“강화학습은 환경과의 상호작용으로부터 학습하는 것에 대한 전산적인 접근법”***

## **1. 강화학습이란?**

<img src="./images/1.png" width="49%"/>
<img src="./images/2.png" width="49%"/>

- 다양한 분야가 융합된 학문
- 머신러닝의 한 분야

### **강화학습, 지도학습, 비지도학습의 차이**
학습에 사용하는 데이터의 관점에서 차이를 말할 수 있다.
- 지도학습 : Label이 있는 데이터를 사용한다.
- 비지도학습 : Label이 없는 데이터를 사용한다.
- 강화학습 : Agent가 환경(Environment)과의 상호작용을 통해 State, Reward를 바탕으로 학습을 진행한다.

### **행동심리학에서의 강화(Reinforcement)의 의미**

- 행동심리학에서 강화(Reinforcement) 는 생물이 어떤 자극에 반응해 미래의 행동을 바꾸는 것을 말한다.
- 예를들어 뜨거운 주전자를 만져본 아이는 주전자가 뜨겁다는 것을 깨닫고 다음부터 주전자를 만질 때 조심한다.

### **강화학습의 구성요소**
<img src="./images/3.png" width="40%"/>

- Agent : 학습을 하는 주체, Environment 에서 Action을 취하고 Reward, State를 얻는다.
- Environment : Agent가 학습을 하고 극복하고자 하는 환경, Action에 따른 State와 Reward를 Agent에게 반환해준다.
- Reward : Agent의 Action에 따라 Environment가 반환해주는 값, 학습의 척도이다.
- State : Agent의 Environment 내에서의 상태이다.

## **2. 강화학습의 특징**
- 학습을 지도해주는 감독관이 없으며 ***보상(Reward)*** 을 통해 학습한다.
- 학습에 대한 피드백이 즉각적이지 않다.
- 학습에 시간이 포함되어 있다.(Sequential)
- 매 순간 Agent의 행동은 항상 그 다음 행동과 보상에 영향을 끼친다.

## **3. 보상(Reward)**
- Agent의 행동(Action)에 대한 Scalar Feedback Signal
- Agent가 State에서 얼마나 잘 행동(Action) 하는지에 대한 척도
- Agent는 매 State 마다 바로 다음 State에서 보이는 단기적인 Rewrad 보다 최종 목적지에 도달했을 때의 누적 Reward가 가장 크도록 행동한다.