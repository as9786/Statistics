# 검정
- 실제 모형(Unrestricted model)의 설명력과 귀무가설이 맞다는 가정 하의 모형(restricted model)의 설명력의 차이가 크면 클수록 귀무가설이 틀린 확률이 올라감
- 모형의 설명력은 log-likelihood 값과 비례

## Likelihood ratio test
- $H_0 : \psi = \psi_0, \ where\ \psi=(\theta_1, \dots, \theta_r)$
- 여러 개의 모수를 검정(한 개여도 됨)
- LPR statistic은 chi-square distribution을 가짐(자유도 : r)
- $X= 2(l(\hat \theta ; Y) - l(\hat \theta_0 ; Y)) ~ \X_r^2$
- X 값이 커질수록 귀무가설을 기각할 확률 증가
- Log-Likelihood 값은 음수
