# Risk and Return


# 定义

概念符号

- `Return` 回报 ： $R_{it} = \frac{D_{it} + P_{it} - P_{it-1}}{P_{it-1}}$
- `Expected Return` 期望回报：$E[R_{it}]$ 
- `Net Risk-free Rate` 净无风险利率： $r_f$
- `Excess Return` 超额回报： $R_{it} - r_f$
- `Risk Premium`  风险溢价: $E[R_{it}] - r_f$

统计学符号

- `mean` : $\mu_i =\mathsf E[R_{it}]$
- `variance` : $\sigma_i^2=\mathsf E[(R_{it}-\mu_i)^2]$
- `standard deviation` : $\sigma_i=\sqrt{\sigma_i^2}$
- `Sample Estimators` 将上述统计结果的历史值都纳入统计

    $$
    \begin{aligned}
    \hat{\mu}_i &=\frac{1}{T}\sum\limits_{t=1}^TR_{it}\\
    \hat{\sigma}_i^2&=\frac{1}{T-1}\sum\limits_{t=1}^T(R_{it}-\hat{\mu}_i)^2\\
    \hat{\sigma}_i&=\sqrt{\hat{\sigma}_i^2}
    \end{aligned}
    $$

相关性
- `Covariance`

    $$
    \text{Cov}[R_{it},R_{jt}] = \text{E}[(R_{it}-\mu_i)(R_{jt}-\mu_j)]
    $$

- `Correlation`

    $$
    \mathsf{Corr}[R_{it},R_{jt}]~=~\frac{\mathsf{E}[(R_{it}-\mu_{i})(R_{jt}-\mu_{j})]}{\sigma_{i}\sigma_{j}}
    $$

# 有效市场

股票价格在有效市场 (`Efficient Market`) 中的特点
- 价格随机、不可预测
- 价格能实时且准确跟随行情变化
- 投资者不能从风险调整中获取收益

# 公理

> [!note]
> 风险越大，收益越大
