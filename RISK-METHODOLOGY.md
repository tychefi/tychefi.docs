# 产品风险指数 / Product risk index

TycheFi 采用 1.0～5.0 的**内部产品风险指数**，支持一位小数。1 为较低风险端、5 为较高风险端，五段刻度用于展示产品方提供的指数，不是基于统计模型计算的等距风险量。当前 Flexible、Fixed 3M／6M／12M 均由 TycheFi 指定为 4.9，动态收益待评估。评级不是独立机构评级、不代表亏损概率、最大回撤或本金保障，不由净年化自动推导。

- 等级由 TycheFi 提供，维护于 `products/manifest.json` 的 `risk.level`。未提供时必须为 null，页面显示“待评估”，不默认成低风险。
- 策略与市场、流动性、托管与换汇、兑付与损失承担、合约与网络五个维度说明已知风险，不虚构各维度分数或历史风险统计。
- 更新评级时同时更新 `risk.updatedAt`，核对产品条款与风险因素，并同步发布前端。改变评级不改变已锁定的金融条款。
- 动态收益策略尚未披露完整细则，是否可评级应单独确认；不得因筹备状态自动赋予最低或最高等级。

TycheFi uses an **internal product risk index from 1.0 to 5.0**, with one decimal supported. One is the lower-risk end and five the higher-risk end. Five visual segments display the product provider's index; they do not represent equally spaced statistical risk amounts. TycheFi currently assigns 4.9 to Flexible and Fixed 3M/6M/12M; dynamic yield is not rated. They are not independent ratings, loss probabilities, drawdown estimates or principal protection, and are not derived automatically from APR.

- TycheFi supplies the level in `products/manifest.json`, under `risk.level`. Missing ratings remain null and render as “Not rated”, never as low risk.
- Five factors describe known exposure: liquidity, strategy and markets, custody and conversion, repayment and loss allocation, and contracts and networks. No invented factor scores or historical statistics are used.
- Update `risk.updatedAt`, review terms and factors, and publish the new frontend snapshot when changing a level. A rating change does not rewrite locked financial terms.
- Incomplete dynamic-strategy disclosures require a separate rating decision; planned status does not automatically imply the lowest or highest level.
