# 0. 정리 강의

https://www.inflearn.com/course/%EB%A8%B8%EC%8B%A0%EB%9F%AC%EB%8B%9D%EC%9D%B4%EB%A1%A0-%ED%8C%8C%EC%9D%B4%EC%8D%AC%EC%8B%A4%EC%8A%B5/

# 1. kNN 최근접 이웃 알고리즘

![kNN](https://i.imgur.com/ESvhfB6.png)

키스의 수가 많으면 로맨틱 영화, 킥의 수가 많으면 액션 영화라고 분류한다고 가정합니다.

k는 최근접 점을 몇개 할지 정하는 수입니다.
k는 홀수여야합니다
짝수이면 답을 할 수 가 없기 때문입니다.

보편적으로 k는 작고 홀수로 사용됩니다.(ex) k=3)

![knn2](https://i.imgur.com/vC6SCj9.png)

위와 같이 최근접 점 3개 중에서 액션영화가 2개 로맨스영화가 1개라면
빨간색 점(새로운 데이터)은 액션영화가 되게 되는 것입니다.

그렇다면 최근접 점은 프로그램상에서는 어떻게 구할까요?
피타고라스의 정리를 사용하여서 구할 수 있습니다.

distance^2 = a^2 + b^2