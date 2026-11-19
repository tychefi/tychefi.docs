# 健康与风险指数 / Health and risk indices

## 中文

两项指数均为 0～5 范围，**风险指数 = 5 − 健康指数**。健康越高，所表达的风险越低；风险越高，所表达的风险越高。此前的 4.9 指健康，不是风险。

当前四个固收产品（Flexible、Fixed 3M／6M／12M）的健康参考配置均为 **4.9**，对应风险 **0.1**。动态收益待评估。两项指数是 TycheFi 提供的内部口径，不是独立评级、亏损概率、最大回撤预测或本金保证；不能按净年化收益反推指数。

- 链上配置：`tyche.vault::healthcfg`。管理权限通过 `sethealth(product,rated,health_x100)` 设置健康，风险由合约派生，不能独立输入。
- 精度：0～500 的整数代表百分之一单位。490 → 健康 4.90、风险 0.10；允许已评级健康为 0，此时风险为 5。
- 未评估：`rated=false` 或缺少／读取失败／无效配置时，两项都显示“待评估”。未评估的零占位不是真实风险值，不能显示为零风险。
- 数据来源：应用只使用验证过的链上值，`assessment.reference` 只提供文档参考，不作为运行时回退。更新指数不改变利率、锁期或兑付义务。
- 五个维度：流动性、策略与市场、托管与换汇、兑付与损失承担、合约与网络，说明已知风险，不虚构维度分数。

健康 4.9 的正面颜色不代表风险消失。阅读各产品的策略、团队、资金流和退出安排后，再判断其是否符合自己的要求。

## English

Both indices range from 0 to 5. **Risk index = 5 − health index.** Higher health expresses lower risk on this internal scale. The previously supplied 4.9 means health, not risk.

Current reference configurations for Flexible and Fixed 3M/6M/12M are **health 4.9**, **risk 0.1**. Dynamic yield is not rated. TycheFi supplies this internal assessment; it is not an independent rating, loss probability, drawdown prediction or principal guarantee, and cannot be inferred from net APR.

- Configuration: `tyche.vault::healthcfg`. The administrator sets health through `sethealth(product,rated,health_x100)`; the contract derives risk rather than accepting it independently.
- Precision: integers 0–500 represent hundredths. 490 means health 4.90 and risk 0.10. Rated health of zero is valid and implies risk of five.
- Unrated: false rated status, missing or failed reads, or invalid configuration displays both indices as “Not rated”. Unrated zero placeholders do not mean zero risk.
- Source: the app uses validated on-chain values only. `assessment.reference` is documentation context, never a runtime fallback. Assessments do not alter rates, lock-up or repayment obligations.
- Five factors explain liquidity, strategy and markets, custody and conversion, repayment and loss allocation, and contracts and networks. No invented factor scores are used.

A positive color for health 4.9 does not remove risk. Read each product's strategy, team, funds and exit terms.
