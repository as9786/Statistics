# 이진 결과 모형
- 최대 가능도 추정을 사용하기 위해서는 가능도 함수를 먼저 계산해야 함
- $\prod_{i=1}^{N}P(Y_i=y_i)$
- $P(Y_i=y_i)$는 $Y_i$에 대한 확률분포의 PDF
- 종속변수가 이진 값을 갖을 경우, Bernoulli distribution을 갖음
- Bermoulli Distribution CDF : $f(y;p)=p^y(1-p)^{1-y}\ for\ y\in{0,1}$
- Log-Likelihood : $l(p)=logL(p)=\sum_{i=1}^{n}\{{{y_ilogp+(1-y_i)log(1-p)\}$
- $p=P(Y_i=1)$
- p를 X의 함수로 표현
- p를 X의 함수로 표현할 때 어떠한 함수를 사용하는지에 따라 logit model or probit model로 구분
- p=P(y=1|x)=F(x'b)
- F는 x'b의 함수로 정의된 특정한 모수적 함수이며, 보통 누적분포함수(CDF)
- Logistic(Logit) : $F(\cdot)=\Lambda(\cdot)=\frac{1}{1+e^{-(b_0+b_1x_1)}}$
- Probit : F$(\cdot)=\phi(\cdot)$. $\phi$는 정규 분포의 누적분포함수
- Complementary log-log : Data가 불균형이 심할 때 사용

# 잠재 변수
- 잠재변수를 가정. $y_i^*$
- $y_i^*=x_ib+e_i$
- 실제 종속변수는 잠재변수에 의해서 결정된다고 가정

# Marginal effect

