# Markov Chain Monte Carlo
- Bayes' rule을 이용해서 사후분포의 형태 파악
- 직접 계산하는 것이 아니라, 사후 분포로부터 많은 수의 모수 값들을 표본 추출하여 해당 분포의 형태 추정(Monte Carlo simulation)
- 증거를 계산하는 것이 어렵지만 MCMC는 계산 안해도 됨

## Metropolis algorithm
- The simplest MCMC
- 확률 분포에서 표본을 뽑는 방법
- 복잡한 분포에서 표본 추출이 어려울 떄 사용
- 원하는 분포를 따르는 표본을 받아들일지 말지 결정
- 임의의 모수 값에서 시작
- 그 값을 기준으로 근처의 새로운 값들을 제안
- 모수 값이 평균인 정규분포 사용
- 추출한 값의 확률이 기존 값의 확률보다 더 크면 수용
- 그렇지 않으면 확률적으로 수용
- $p_{accept}=min(\frac{p(\theta_{proposed})}{p(\theta_{current})},1)$
- u~Uniform(0,1)
- $r=\frac{\pi(x')}{\pi(x)}$
- if u < r -> 이동
- 새로운 상태가 더 확률이 높으면 무조건 이동 

