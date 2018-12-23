# python 

- 과학 분야, 특히 기계학습과 데이터 과학 분야에서 널리 쓰이는 언어
- 파이썬 자체의 뛰어난 성능에 넘파이와 사이파이 같은 수치 계산과 통계 처리를 다루는 탁월한 라이브러리
- 여러 유명 딥러닝 프레임워크들이 파이썬용 API 제공

이 책에서 다루는 언어, 라이브러리
```
- 파이썬3
- 넘파이 (수학 알고리즘과 배열을 조작하기 위한)
- matplotlib (시각적으로 볼 수 있게 해주는)
```

=> 아나콘다 설치하면 다 포함하고 있다.
(https://www.anaconda.com/download/)



## numpy
- 배열로 산술 연산 수행이 가능
- 원소별 계산뿐 아니라 배열 * 스칼라 값 조합으로도 수행 가능 -> 브로드 캐스트 
- 다차원 배열로도 작성 가능
```python
import numpy as np   # 넘파이 가져오기

# 1차원 배열
x = np.array([1.0, 2.0, 3.0]) # 배열 생성하기
print(x) # [1. 2. 3.]
type(x) # <class 'numpy.ndarray'>

# N차원 배열
A = np.array([[1, 2],[3, 4]])
print(A) 
# [[1 2]
# [3 4]]
A.shape # 행렬 A 의 형상 (2, 2)
A.dtype # 행렬에 담긴 원소의 자료형 dtype('int64')

A[0] # 0행
A[0][1] # (0, 1) 위치의 원소

# for문으로도 접근 가능
for row in A:
    print(row)
#[1 2]
#[3 4]

A = A.flatten() # A를 1차원 배열로 변환(평탄화)
print(A) # [1 2 3 4]
A>2 # array([[False, False], [True, True]])
A[A>2] # array([3,4])
```


## matplotlib
- 시각화 라이브러리
- 그래프 및 이미지 시각화 가능
```python
import numpy as np
import matplotlib.pyplot as plt

# 데이터 준비
x = np.arange(0, 6, 0.1) # 0에서 6까지 0.1 간격으로 생성
y = np.sin(x)

# 그래프 그리기
plt.plot.(x, y)
plt.legend()
plt.show()
```

# 정리