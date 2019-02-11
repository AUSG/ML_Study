# Markov Decision Process

## **1. Introduction**
- Markov Decision Processes formally ***describe an environment*** for reinforcement learning
- Where the environment is ***fully observable***

## **2. Markov Property**
***The future is independent of the past given the present***</br>
***(현재의 미래는 현재의 과거로부터 독립적이다)***

- 시작 S1 부터 미래 St+1에 도달할 확률과, 현재 St에서 St+1에 도달할 확률이 동일하다.
- 현재는 과거의 미래이며, 현재는 과거의 정보들을 가지고있다.

<img src="./images/1.png" width="45%"/>

## **3. State Transition Matrix**
- State s, s' 이 Markov 일 때, State Transition Probability 는 다음을 만족한다.<br>

<img src="./images/2.png" width="30%"/>

- State Transition Matrix P 는 모든 State s 로부터 s' 으로 가는 State Transition Probability 를 정의합니다.

<img src="./images/3.png" width="30%"/>

- State Transition Matrix에서 각각의 행을 구성하는 인자들의 총합은 1 이다.

## **4. Markov Process(or Markov Chain)**

***Markov Property를 만족하는 State들과, 이 State들 간의 State Transition Matrix 으로 구성된 Tuple***

<img src="./images/4.png" width="45%"/>
<br>
<img src="./images/5.png" width="45%"/>
<br>
<img src="./images/5-1.png" width="50%"/>

## **5. Markov Reward Process**
***Markov Chain에 Reward가 추가된 Tuple***

<img src="./images/6.png" width="45%"/>
<br>
<img src="./images/7.png" width="45%"/>

## **6. Return**
- Return G는 어떤 Episode의 Step t 부터 매 Step마다 얻게되는 모든 Reward의 합을 의미한다.
- Discount r은 **7. Discount** 참고

 <img src="./images/8.png" width="45%"/>

## **7. Discount r**
- 0 이상 1 이하의 값, [0, 1]
- 미래의 Reward에 패널티를 가함으로써 현재 시점에서의 기댓값으로 변환한다.
- 먼 미래의 Reward 일 수록 많은 패널티를 얻게 된다.
- 먼 미래에 얻게될 Reward와, 가까운 미래에 얻게될 Reward의 경중을 조정하는 용도.
- r이 0에 가까울 수록 가까운 미래를 더 중요시한다.
- r이 1에 가까울 수록 먼 미래또한 중요시한다.
- Cyclic 상태에서 무한으로 빠지는 것을 방지하여 준다.

## **8. State Value Function of MRP**
***State s에서 앞으로 얻게될 것이라 기대되는 가치***
- Agent는 다음 State s' 으로 이동할때 v(s') 이 가장 큰 State로 이동한다.
- 학습을 반복하면서 Value Function은 업데이트 된다.

<img src="./images/9.png" width="45%"/>
<br>
<img src="./images/10.png" width="50%"/>