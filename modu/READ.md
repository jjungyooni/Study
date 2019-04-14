# 모두의 딥러닝



# lec 7-1
> 학습률 조절하는 방법, 데이터 선처리 방법, 오버피팅 방지하는 방법

### cost function 을 최소화 하기위해 사용했던 GD 에 learning rate 임의로 정해서 써왔는데, 이 값을 잘 정하려면?
1. 큰값으로 하면? -> 내려가는 스텝이 굉장히 크다면? => 학습이 제대로 안이뤄지고 (cost가 안줄고) 계속 반복을 하게 될 수도 있음 => overshooting
2. 굉장히 작은 값으로 하면? => 굉~~장히 오래걸려서 결과를 보기가 힘들어질 수도 있다. 

> 여러 값으로 테스트 해보는 수밖에 0.01 정도로 먼저 해보고 발산이 되는거같으면 좀더 작게, 너무 늦게 움직이면 크게 조절해야한다.

### 선처리 
* 데이터가 너무 차이가 있는 데이터는 학습할때 좀 힘들 수 있어서 걔들을 normalized data 로 범위를 좁혀준다 (평균과 분산값으로 standarization)
* 데이터가 중심에서 떨어져 있으면 zero-centered data 로 중앙으로 옮겨준다. 

### overfitting
> 너무 하나의 값에 맞춰져 있는것 방지법은?

1. more training data!
2. reduce the number of features
3. regularization 일반화 (weight 값을 너무 큰값으로 갖지 말자)


## 07-2 
> 모델이 얼마나 잘 만들어졌는지 확인하려면? -> training set 과 test set 분리

