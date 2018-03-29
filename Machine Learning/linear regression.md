# 0. 정리 강의 url

https://www.youtube.com/watch?v=MwadQ74iE-k


# 1. linear regression (선형회귀) 이해하기

![대체이미지](https://i.imgur.com/a7G9gs1.png)

classification : kNN, Decision Tree, SVM

학습된 class로만 답이 분류되어 나옴

regression : 입력값에 관한 출력값 예측

linear regression predicts output by fitting a linear equation (y = ax + b) to observed data

linear regression는 y = ax + b와 같은 1차 방정식의 형태를 가지고 있습니다.

![대체이미지](https://i.imgur.com/6P2FMQ6.png)

왼쪽과 오른쪽 선 중 무엇이 더 예측을 잘 하게 될까요?

왼쪽?일까요?

##### Error - difference between prediction and real value

![대체이미지](https://i.imgur.com/qm2wavo.png)

예측을 더 잘하다고 평가되는 기준은 더 작은 에러를 가지고 있는가입니다.

##### Square Error - (difference between prediction and real value)^2

넓이 즉, 제곱을 하는 이유는 에러가 클 수 록 더욱 차이를 크게하여서 예측 모델 사이의 구분을 더 잘하기 위해서입니다.

![대체이미지](https://i.imgur.com/svGfjsZ.png)

how to fine least mean square? Gradient Decent!

Cost Function = Mean Square Error 를 최저로 만드는 것을 목표로 합니다.

![대체이미지](https://i.imgur.com/opOk5h9.png)

기존의 θ값에서 learning rate와 mean square error의 값을 뺀 것들 반복하여서 mean square error의 값을 0에 가깝게 합니다.

##### how to decide learning rate?

We must set the learning rate to an appropriate value since learning rate determines how fast or slow we will move toward the optimal θ

If learning rate is very large, we may skip the optimal solution. If learning rate is too small, finding optimal solution will take huge steps.

learning rate를 적절하게 조정해줘야합니다.