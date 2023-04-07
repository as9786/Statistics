# 포아송 분포

## 정의

- 정해진 시간 안에 어떤 사건이 일어날 횟수에 대한 기댓값을 $\lambda$라고 했을 때, 그 사건이 n회 일어날 확률은 아래와 같음

![image](https://user-images.githubusercontent.com/80622859/229729205-c2985345-a83d-486d-9655-1d57cb9c450d.png)

- e는 자연상수

## 이항분포

- 1시간 동안 창 밖을 봄
- 1000명이 있음. 10초에 1명 꼴로 사람이 넘어진다고 가정
- 10초에 0.1%의 확률로 사람이 한 명 넘어짐
- 3600초 동안 10초에 0.1%의 확률로 일어나는 사건이 독립적으로 360번 일어남
- 이런 경우 이항 분포를 이용해 1시간 동안 몇 명의 사람이 넘어지는지에 대한 확률에 대한 분포를 확인할 수 있음
- 총 시행 횟수 n과 성공확률 p인 경우의 이항분포 B(n,p)라고 했을 때 B(360,0.001)을 따르는 사건
- 평균적으로 360 x 0.001 = 0.36명이라는 결론을 얻을 수 있음
- 360번 중 k번 사건이 이어나갈 확률

![image](https://user-images.githubusercontent.com/80622859/229730263-415dca58-e345-446b-a08b-d2f656e83f1d.png)

- 360! 너무 큰 수!
- 이항분포에서 n이 너무 크고 p가 너무 작은 경우에 이항 분포의 확률분포를 근사적으로 계산하기 위해서는 극한값을 이용한 새로운 형태의 분포를 제시

## 포아송 분포 유도

- $\lambda = np, p = \frac{\lambda}{n}$

![image](https://user-images.githubusercontent.com/80622859/229731093-1e968579-ab0f-4a2f-b180-747f380ddfa6.png)

- n을 무한대로 극한을 취하면 아래와 같음

![image](https://user-images.githubusercontent.com/80622859/230542483-f53a503e-bc2d-4dc7-a73a-2ee554fd9a0e.png)

![image](https://user-images.githubusercontent.com/80622859/230542128-b15ca9cd-b713-443a-b82e-04422e5edf19.png)

![image](https://user-images.githubusercontent.com/80622859/230542506-970f0a59-41dc-419d-a524-2b119a1faed1.png)

- 수 많은 사건 중(n이 무한대일 때) 특정한 사건이 발생활 확률이 매우 적은 확률 변수가 갖는 분포

## 예제

- 총 2000건의 보험에 대해 청구할 확률이 0.0001
- 평균 = 2000 

### 1. 보험 청구가 한 번도 없을 확률

![image](https://user-images.githubusercontent.com/80622859/230542648-d3c99a3a-d7af-4ef8-a2e5-04d6c8485a26.png)

