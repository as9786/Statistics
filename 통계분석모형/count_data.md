# Cound data
- 비선형 -> 최대 가능도 추정
- 어떠한 사건이 특정한 시간 동안 발생하는 횟수
- 음수일 수 없음 
- 하루동안 발생하는 범죄 수
- Poisson distribution -> 평균 = 분산
- 조건부 확률이 아닌 조건부 기대값에 초점
- Poisson distribution : 정해진 시간 안에 발생하는 사건의 수를 값으로 갖는 분포
- 음이항 분포 -> 매 시행에서 성공률이 p인 bernouill experiment를 r번 성공할 때까지 독립적으로 반복 시행한 횟수에 대한 분포

# Poisson regression
- $P(Y=y)=f(y)=e^{-\mu}\frac{\mu^y}{y!},y=0,1,2,...,\mu > 0$
- $E(Y)=Var(Y)=\mu$

## 한계
- 분산이 평균보다 클 수 있음

# 음이항 회귀(Negative Binomial regression, NB)
- $v \sim Gamma(1,\alpha)$
  - 평균 : 1, 분산 : $\alpha$
- y는 Possion-Gamma mixture distribution을 가짐. NB distribution은 $NB(\mu, \alpha)$로 표시
- $Pr(Y=y|\mu, \alpha)=\frac{\Gamma(\alpha^{-1} +y)}{\Gamma(\alpha^{-1})\Gamma(y+1)}(\frac{\alpha^{-1}}{\alpha^{-1}+\mu})^{\alpha^{-1}}(\frac{\mu}{\mu+\alpha^{-1}})^y$
- Poisson model보다 더 일반적(음이항 분포는 확장판)
- Poisson distribution에서는 평균=분산
- 그러나 real data에서는 분산 > 평균인 경우 존재(과산포)
- 음이항 분포는 위 과산포를 반영
- $Var(x) = \mu + \alpha \mu^2$
  - $\alpha=0$ : Poisson distribution
  - $\alpha > 0$ : 과산포 반영

