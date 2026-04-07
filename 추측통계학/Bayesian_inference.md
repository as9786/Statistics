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
- 
