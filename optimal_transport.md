# Optimal transport
- 하나의 확률 분포를 다른 확률 분포로 옮기는데 필요한 비용 계산 문제
- 두 확률 간의 거리 측정
- Transport plan : 두 분포 사이의 거리를 구하고, 각 점을 다른 점으로 어떻게 옮길지 정의. $\gamma(x,y)$
- Cost function : 위치 x에서 위치 y로 물질을 옮길 때 드는 비용. c(x,y) 

## 두 확률 분포 간의 거리를 측정하는 방법
- 확률 변수 X, Y가 분포 P,Q를 갖고, 확률밀도함수를 각각 p,q라고 함

### 1. Kullback-Leibler Divergence(KLD)
- 두 확률 분포 P와 Q 간의 차이를 측정하는 비대칭적인 방법
- P가 Q로부터 얼마나 다른지에 대한 상대적인 entropy 차이
- $D_{KL}(P||Q) = \int P(x)log(\frac{P(x)}{Q(x)})dx$

### 2. Jensen-Shannon Divergence(JSD)
- KLD의 대칭적인 방법. 두 분포의 평균을 기반으로 차이 측정
- P와 Q가 완전히 일치하면 JSD = 0. 최대값은 1
- $D_{JS}(P||Q) = \frac{1}{2}(D_{KL}(P||M) + D_{KL}(Q||M)), \ M=\frac{1}{2}(P+Q)$

### 3. Wasserstein distance
- 확률 분포를 옮기는데 드는 최소 비용 측정
- 연속 변수 또는 영상과 같은 공간적 분포에서 사용 가능
- $min_{\gamma \prod(P,Q)} \int c(x,y)d \gamma (x,y)$

### 4. Total Variation Distance(TVD)
- 두 확률 분포 간의 최대 차이 측정
- 두 분포가 얼마나 겹치는지 판단. 일치하면 0
- $d_{TV} (P,Q) = \frac{1}{2} \int |P(x)-Q(x)|dx$

### 5. Hellinger distance
- 두 분포 간 유사도 측정. 대칭
- $H(P,Q)=\frac{1}{\sqrt{2}}(\int (\sqrt{P(x)} - \sqrt{Q(x)})^2dx)^{1/2}$

