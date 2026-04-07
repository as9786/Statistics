# Ordered response model

- 종속 변수가 순위 정보를 가짐
- Ordinal variable(서열 변수). 만족도, 평점 등
- 비선형모형 <- 최대 가능도 추정
- 가능도를 먼저 계산해야 함
- $\prod_{i=1}^{N}P(Y_i=y_i)$
- 확률 분포를 어떻게 구하느냐에 따라서 ordered logit and ordered probit model로 구분
- Ordered logit -> e|x ~ Standard logistic distribution
- Ordered probit -> e|x ~ Standard normal distribution
- Cut points를 통해 구간을 나눔
- 3개를 분류 시 2개의 cut points 필요
- $P(Y=0|X) = P(y^* \leq \alpha_1)$
- $y^*=xb+e$ 이 식을 위에 대입
- $P(xb+e \leq \alpha_1) = P(e \leq \alpha_1 - xb)$
- $P(Y=1) P(\alpha_1 < y^* \leq \alpha_2)=P(\alpha_1 - xb < e \leq alpha_2 - xb)$
- $P(y=J|x)=P(y^*>\alpha_j|x)=1-\Gamma(\alpha_j-xb)$
- $f(y_i) = \prod_{j=1}^j p_{ij}^{y_{ij}}$

