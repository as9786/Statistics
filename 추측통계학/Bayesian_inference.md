# 통계적 추론
- 우리가 관심있어 하는 수학적 모형 또는 확률 모형의 모수 값을 추론하는 방법

## Frequentist perspective
- 모수는 고정
- 점 추정 또는 구간 추정
- 최소 제곱법, 최대 가능도 추정 등

## Bayesian perspective
- 모수는 변수
- 전체적인 모수의 분포에 관심

# Bayesian inference
- 모수에 대한 사전 지식이 있다고 가정
- 해당 모형을 통해서 발생된 data가 존재
- 이 data를 사용해서 모수에 대한 믿음을 최신화 => 새로운 확률 분포 추정
- Prior(사전 지식) + data -> Posterior
- 사전 지식과 data를 위해서 basyes' rule 사용
- $P(\theta|D) = \frac{P(D|\theta)P(\theta)}{P(D)}$
- $\theta$ : 우리가 알고자하는 모수, D : Data(우리가 관찰한 표본), $P(D|\theta)$ : data의 확률=가능도, $P(\theta)$ : 사전확률분포(Prior), 사전믿음, 선행연구 또는 상식 선에서 결정, P(D) : 증거(evidence)
- $P(D)=\sum_{\theta^k}P(D|\theta^k)P(\theta^*)$ 또는 $P(D)=\int_{\theta^k} P(D|\theta^k)P(\theta^k) \text{d}\theta^k$

## 과정
- 문제에 대한 변수 혹은 data 결정
- 수학적 모형 결정
- 모수의 사전 분포 결정
- Bayesian inference를 통해 사후 분포 도출
- 사후 분포가 data를 잘 설명하는지 파악

# Bayes' rule
- 데이터를 보기 전 우리가 믿고 있던 정도(prior)가, 데이터를 본 이후 어떻게 바뀌는지(posteriors)를 연결하는 수학적 관계
- 모수값의 확률을 관찰한 data를 토대로 새롭게 최신화 하는 것
- 구름 낀 날씨일 확률을 예측하고자 할 때
  - 사전 믿음 : 평소 흐린 날씨일 확률 : p(cloudy)
  - Observed data
    - 비 : p(cloudy|rain)
    - Sunglasses : p(cloudy|sunglasses)
- $P(\theta|y)=\frac{P(y|\theta)P(\theta)}{P(y)}=\frac{P(y|\theta)P(\theta)}{\sum_{\theta} P(y,\theta)}=\frac{P(y|\theta)P(\theta)}{\sum_{\theta} P(y|\theta)P(\theta)}$
- $P(\theta|y)$ : 사후 분포, $P(y|\theta)$ : 가능도, $P(\theta)$ : 사전 분포, P(y) : 증거
- 사전 분포 : 모수에 대한 사전 믿음
- 증거 : 모든 가능한 파라미터를 고려했을 때, 전체적으로 데이터가 나타날 확률
- 사후 분포 : 목표
- 가능도와 사전 분포를 통해 사후 분포의 형태를 추측하는 것

# 어려움
- 증거를 구하는 것이 어려움
- 상대적으로 간단한 가능도 함수를 사용하고, 그에 켤레 사전 분포를 사용
- Variational approximation(변분 추론)
- Grid approximation
- Sampling simulation : MCMC(Metropolis Random Walk, Metropolis-Hastings, Gibbs sampling etc)
