# 0. 정리 강의 url

https://youtu.be/n0p0120Gxqk

# 1. 의사결정트리(Decision Tree)

![Decision Tree](https://i.imgur.com/wcRuv1X.png)

타이타닉호 탑승객의 생존여부 결정트리
('sibsp'는 탑승한 배우자와 자녀의 수를 의미)
숫자는 각각 생존 확률과 탑승객이 해당 사항에 해당될 확률

순서

1. Define Problem, Collect training data

2. Extract Data, Bulid a tree

3. Deploy machine

4. Test with test data

의사결정트리를 구성할 때에는 Highest information gain에 해당하는 것을 트리로 구성해갑니다.

information gain (base entropy - new entropy)

# 2. ID3 Algorithm (Entropy and Infomation Gain)

img  | cartoon  | winter | number of preson>1 | Winter family photo
---  | -------- | ------ | ------------------ | ------------------
img1 | No       | Yes    | Yes                | Yes
img2 | No       | Yes    | No                 | No
img3 | Yes      | No     | Yes                | No
img4 | Yes      | Yes    | Yes                | No
img5 | No       | Yes    | No                 | No
img6 | No       | No     | Yes                | No
img7 | Yes      | No     | Yes                | No
img8 | Yes      | Yes    | No                 | No


Total 8 photos

1 photo winter family photo

7 photo Not winter family photo

= Entropy([1+,7-])

= -(1/8) * log(1/8)-(7/8) * log(7/8)

= 0.543
----------------------
Entropy = - p(+) * log(p(+)) - p(-) * log(p(-))

Inoformation Gain(winter family photo, cartoon)

= E (winter family photo) - E (winter fmaily photo, cartoon)

= 0.543 - (4/8 * E[0+,4-]) + 4/8 * E([1+,3-])

= 0.138
-------------------------

Inoformation Gain(winter family photo, winter)

= E (winter family photo) - E (winter fmaily photo, cartoon)

= 0.543 - (5/8 * E[1+,4-]) + 3/8 * E([0+,3-])

= 0.093
-------------------------

Inoformation Gain(winter family photo, number of preson>1)

= E (winter family photo) - E (winter fmaily photo, cartoon)

= 0.543 - (5/8 * E[1+,4-]) + 3/8 * E([0+,3-])

= 0.093

첫번째 속성은 Information Gain이 가장 높은 cartoon으로 지정됩니다.