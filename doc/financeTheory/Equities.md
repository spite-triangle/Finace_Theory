# Equity

# 基本概念

**Equity (股权)** ： 公司的所有权，即普通股 `Common Stock`。**可以说计算公司的股权，就能计算这个公司的价值**

**Dividends (股息/股利)** ：普通股能获取的利益，通常的中小型发展公司不会支付股息（但不是永远不给，永远不给，那只有傻子才投资），因为穷，得把钱留着干其他事
- `Cash Dividends` 现金股利
- `Stock Dividends` 股票股利

普通股的关键点有
- 拥有普通股的人是「剩余索取者`Residual Claimant`」，公司收益首先偿还「债券持有人 `bondholder`」，剩余利益才会分给普通股持有人（若公司收益好，持股人能得到更多的利益）
- `Limited Liability` 有限责任，**持股人可能会失去投入公司的一切，而不是所拥有的一切**
- `Voting Rights` 出售公司控制权，获取投资资金
- `Ease Shortsales` 限制卖空

股票市场有两种，两种市场运行规则完全不同
- `Primary Market` 一级市场: 公司首次发行股票的市场，需要学习其他的课程
    - `Venture Capital` 风险投资
    - `Initial Pubilc Offering` 面向公众发行股票，例如上市`Going Pubilc` 
    - `Seasoned Equity Offering`
- `Secondary Market` 二级市场: 二手市场

# 价值计算

## Dividends Discounted Model

> [!note]
> 通用模型

$$
\begin{aligned}
    P_t &= V_t(D_{t+1},D_{t+2},\dotsm) \\
        &= \frac{E_t[D_{t+1}]}{(1 + r_{t+1})} + \frac{E_t[D_{t+2}]}{(1 + r_{t+2})^2} + \dotsm \\
        &= \sum_{k=1}^\infty  \frac{E_t[D_{t+k}]}{(1 + r_{t+k})^k} 
\end{aligned}
$$

- $P_t$ : 在 $t$ 时刻的价格
- $D_t$ : 在 $t$ 时刻的 `Cash Dividends` 现金股利
- $E_t[\ ]$ : 股息的预测操作，因为 $D_t$ 不像债券的息票是固定的，会随时间变化
- $r_t$ : 在 $t$ 时刻股票的风险回报贴现率 `Risk-adjusted discount rate`。**风险越高的一年，对应的 $r_t$ 也应当越大，股票的价格也就越小**

## Discounted Cashflow Model

为了对上面的模型进行简化，提出两个假设
- 每年获取的现金股利都一样
    $$
        E_t[D_{t+k}] = D
    $$
- 风险回报贴现值不随时间变化
    $$
        r_{t+k} = r
    $$

代入模型得到 `Discounted Cashflow Model`

$$
P_t = \sum_{k=1}^\infty \frac{D}{(1 + r)^k} = \frac{D}{r}
$$


## Gordon Growth Model

在 `Discounted Cashflow Model` 基础上，假设股息的增长率为 $g$，得到了 `Gordon Growth Model`

$$
P_t = \sum_{k=1}^\infty \frac{D(1+g)^{k-1}}{(1 + r)^k} = \frac{D}{r - g}, \ \  r > g
$$

再将该公式进行变形

$$
r = \frac{D}{P_t} + g, \ \  r > g
$$

可以看出贴现率由两个部分组成：**股息占总价值的比列、公司在未来的增长率**。上述公式中 $D$ 得在下一个期限才会支付，描述的是 $[t,t+1]$ 期间的股息会在 $t+1$时刻支付，但是现实是我们无法知道当前的下一期能有多少股息（这是未来的事），那么只能用最近的股息 $D_0$ 去预测未来下一期的股息

$$
r = \frac{D_0(1 + g)}{P_t} + g, \ \  r > g
$$

> [!note]
> 该公式只能用于股票处于「稳定态」时，计算贴现率。当出现人为干涉时，便不再适用，例如股东强制调整 $D$，这是只能使用 `Dividends Discounted Model`

