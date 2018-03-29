# 0. 강의 url

https://youtu.be/9TR54u08IGU

# 1. kmean 클러스터링(k-평균 클러스터링)

##### k-mean steps

1. prepare data 데이터가 필요
2. decide how many clusters you need 얼마나 많은 cluster를 만들지 결정
3. choose inital center of cluster (centroid) cluster의 중심 설정
- randomly select centroid
- manuallu assign centroid
- kmean++
4. assign data point to nearest cluster 주어진 데이터가 어떤  cluster 중심에 가까운지 지정
5. move centroid to the center of its cluster 모든 데이터를 cluster 지정해주고 cluster의 중심을 데이터들의 중간에 있는 지점으로 옮겨줌
6. repeat step 4 and step 5 스텝 4와 5를 반복합니다. (cluster가 변하지 않을때까지)
    until there is no assigned cluster change

![prepare data](https://i.imgur.com/2qNQPoe.png)

![choose inital center of cluster](https://i.imgur.com/B6X22zb.png)

k=3으로 지정하고  cluster의 중심을 정해줍니다.

![assign data point to nearest cluster](https://i.imgur.com/BgmfaZW.png)

주어진 데이터를 어떤 cluster 중심에 가까운지 지정해줍니다.

![move centroid to the center of its cluster](https://i.imgur.com/4Y7Dko2.png)

모든 데이터를 cluster의 지정이 되었으면 cluster의 중심을 데이터 중간 있는 지점으로 옮겨줍니다.

![assign data point to nearest cluster](https://i.imgur.com/1mZocua.png)

변경된 cluster를 중심으로 데이터를 다시 지정합니다. (4의 데이터만 c3로 변경됨)

![move centroid to the center of its cluster](https://i.imgur.com/ajmaOOv.png)

변경된 데이터의 중심을 cluster의 중심으로 변경해줍니다.

![k-mean clustering is done](https://i.imgur.com/KKW63LR.png)

더 이상 cluster를 바꿔지지 않으니 k-mean clustering은 끝나게 됩니다.

##### how to init centroid?

1. randomly choose 랜덤으로 지정
2. manually assign init centroid 바로 직접 지정
3. k-mean++

![manually assign init centroid](https://i.imgur.com/5UxgEXa.png)

![manually assign init centroid](https://i.imgur.com/9gDDGZr.png)

위와 같이 정해진 데이터가 정확한 값을 가지고 잇다면 수동으로 cluster centroid를 지정합니다.

예) 위와같이 지역의 위도,경도로 지정할때

##### k-mean++ init centroid

![k-mean++ init centroid](https://i.imgur.com/whRV2Rq.png)

1. select first data point as first centroid 첫번째 데이터를 첫번째 centroid를 지정합니다.
2. select farthest data point from first centroid as second centroid 두번째 centorid는 첫번째 centroid에서 가장 먼 데이터의 위치로 지정합니다.
3. select farthest data point from centroids as next centroid 마지막 centorid는 현재 있는 centorid에서 공통적으로 먼 데이터의 위치로 지정합니다.