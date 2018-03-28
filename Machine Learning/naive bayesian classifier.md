# 0. 정리 강의 url

https://youtu.be/hO9SVW6nnhM

https://youtu.be/3JWLIV3NaoQ

# 1. 확률 (Probability) 쉽게 이해하기

![Probability](https://i.imgur.com/DAeaCr1.png)

사과가 2개이고 바나나가 하나인 상황

P(apple) = 2/3

P(banana) = 1/3

##### Conditional Probabilty (조건부 확률)

어떤사건 B가 일어났을때 사건 A가 일어날 확률을 의미 기호로 P(A|B)로 표현

the probability of a event (A), given that another (B) has already occured

조건부 확률은 두가지로 나눠짐

- 서로 영향을 끼칠때, 서로 영향을 끼치지 않을때

##### calculating the intersection (when two events are independent) 이벤트끼리 서로 영향을 끼치지 않는 경우

![when two events are independent](https://i.imgur.com/Av67Lxl.png)

초록색 티셔츠를 입던 무슨 티셔츠를 입던 잿팟이 터질 확률은 1% (초록색 티셔츠를 입는것은 잭팟 터질 확률에 영향을 끼치지 않는다.)

P(A ∩ B) = P(A) * P(B)

P(A | B) = P(A)  B has no effect on A

P(B | A) = p(B)  A has no effect on B

if there is a 1% chance that you get jackpot from casino, and a 50% chance that your t-shirts green color, then what is the probability that You wear green t-shirt and you get jackpot from casino(assuming that t-shirt has no influence on jackpot)?

Since t-shirt has no effect on casino result, we take these events as indepent, and so the probability that both events will occur is 

P(Jackpot ∩ Green_shirt) = P(Jackpot) * P(Green_shirt)=(0.01)*(0.5)=0.005

##### calculating the intersection (when two events are dependent) 이벤트끼리 서로 영향을 끼치는 경우

![when two events are dependent](https://i.imgur.com/IoW0DIP.png)

P(A ∩ B) = P(A)*P(B | A)

                P(B | A) = P(A ∩ B) / P(B)

# 2. 베이즈 정리 (Bayes’ Theorem) 쉽게 이해하기

I can predict you have no girl friend, because i know probability of fat, youtube, no fashion, and these conditional probability given that when they don't have girl friend. You have 95% chance of no girl friend!

![대체이미지](https://i.imgur.com/h6hlFgH.png)

##### Bayes’ Theorem proof

![대체이미지](https://i.imgur.com/DPjQa5C.png)

"spam" and "free" are clearly dependent

Since we assume when we have spam email, there might be "free" in the text, and also when we haver "free" in the email, we suspect it is "spam"

##### 베이즈 정리 수식 유도

![대체이미지](https://i.imgur.com/bVRYOJv.png)

##### spam mail

![대체이미지](https://i.imgur.com/0N9MXXQ.png)

![대체이미지](https://i.imgur.com/syFgauq.png)

스팸메일일 확률

3 emails out of a total of 10 are spam message **P(spam) = 3/10**

fee라는 단어가 들어간 확률

4 emails out of those 10 contain the word "free" **P(free) = 4/10**

spam중에 free라는 단어가 들어간 확률

2 emails containing the word "free" have been marked as span **P(free | spam) = 2/3**

![대체이미지](https://i.imgur.com/FSQyw3K.png)




