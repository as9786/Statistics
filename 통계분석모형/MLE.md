# 선형 모형의 한계
- 특정한 값들만을 갖는 종속 변수(제한적 종속변수)를 잘 설명하지 못함
- 명목변수(이진 분류 등), 서열변수(리커드 척도 등), fractional values(%), frequency of events(하루에 발생한 교통사고 건 수 등)
- 비선형 모형 사용 필요
- OLS 추정식은 비선형 모형에 부적합
- 목적함수가 볼록하지 않음. 게산이 어려움. 편향이 발생

# 최대 가능도 추정
- 모형의 모수를 추정하는 방식. 가능도를 최대화
- 가정 : 종속 변수는 특정 확률 분포를 따른다
- 가능도 : 우리가 가지고 있는 데이터의 확률
- 가능도는 확률 분포로 표현 가능
- 가능도는 우리가 추정하고 싶은 모수
- 왜냐하면 가능도는 확률 분포를 결정해줌

## Binomial distribution(이항 분포)
- Bernoulli distribution
- $p_x(x) = \begin{pmatrix}n\\x\end{pmatrix}p^x(1-p)^{n-x}$ p->모수, n : # of Bermoulli trials, x = # of success

## Bernoulli distribution
- A random variable that takes value 1 in case of success and 0 in case of failure
- PDF : $f(x;p)=p^x(1-p)^{1-x}\ for\ x \in {0,1}$
- E[X] = p, V[X] = p(1-p)

## 속성

### 일치성(Consistency) 
- $\lim_{x \rightarrow a} \hat \theta_k = \theta_k$
- $E(\hat \theta_k) = \theta_k$ => Bias x

### Approximate normality
- $\theta$는 표본이 커질수록 정규 분포에 근사

# 가능도 최대화
- 두 가지 방법
  - Newton-Raphson algorithm -> 단일 모형
  - EM(Expectation-Maximization) algorithm -> 혼합 모형
 - 기계 학습에서는 경사하강법 사용

## Newton-Raphson algorithm
- 근을 찾는 방법
- 순차적으로 x의 값을 최산화
- 임의 x 값에 대한 접선을 구하고, 그 접선의 x 절편을 다음 x 값으로 사용

# Regularity conditions
- Y는 독립항등분포(iid)
- 서로 다른 모수 값은 서로 다른 분포를 가짐
- 모수를 보면 모형이 결정
- 동일한 정의역을 가짐 


