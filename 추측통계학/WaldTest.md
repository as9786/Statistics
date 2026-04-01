
- 제한이 없는 모형의 추정치 요구
- 가능도 함수의 값을 최대화함으로써 얻는 모수와 귀무가설 값 비교

## 가설 검정
- H0 : $\theta_k = \theta_{0k}$
- 귀무가설이 참이라면, $E(\hat \theta_k) = \theta_{0k}$
- Z-statistic 사용
- $Z=\frac{\hat \theta_k - \theta_{0k}}{\sqrt{\hat v_k}} ~N$
- $\hat v_k = Var(\hat \theta_k)$
- Wald statistic = $Z^2$
- $W = \frac{(\hat \theta_k - \theta_{0k})^2}{\sqrt{\hat v_k}} ~ X_1^2$
- 자유도가 1인 카이제곱 분포 따름 
- W 값이 크면 클수록 귀무가설을 기각할 확률 상승
- 따라서, 해당 분포에서 나왔다고 보기 어려울 정도로 큰 값들은 귀무가설(H₀)에 반대되는 증거를 제공한다

<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/f5dfb669-8083-4d7f-a705-dcbbf6ab257a" />

## 분산
- 특정 지점에서의 log-likelihood의 곡률에 의해 결정(최대값)
- 분산은 MLE의 이차 미분 값의 -역수
- Binomial dist parameter의 분산 : $Var[p] = p_0(1-p_0)/n$ 
