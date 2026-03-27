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
- $p_x(x) = \begin{pmatrix}n\\x\end{pmatrix}p^x(1-p)^{n-x}$. p->모수, n : # of Bermoulli trials, x = # of success

## Bernoulli distribution
- A random variable that takes value 1 in case of success and 0 in case of failure
- PDF : $f(x;p)=p^x(1-p)^{1-x}\ for\ x \in {0,1}$
- E[X] = p, V[X] = p(1-p)



