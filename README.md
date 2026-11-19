# TycheFi 产品文档

本仓库维护面向用户的产品说明，Vault 详情页与站内产品文档读取同一份内容。中英文分别存放，入口由 `products/manifest.json` 定义。

| 产品 | 中文 | English |
| --- | --- | --- |
| Tyche Flexible | [灵活固收](products/zh-CN/flexible.md) | [Flexible income](products/en/flexible.md) |
| Tyche Fixed 3M | [3 个月](products/zh-CN/fixed-3m.md) | [3 months](products/en/fixed-3m.md) |
| Tyche Fixed 6M | [6 个月](products/zh-CN/fixed-6m.md) | [6 months](products/en/fixed-6m.md) |
| Tyche Fixed 12M | [12 个月](products/zh-CN/fixed-12m.md) | [12 months](products/en/fixed-12m.md) |
| Tyche Strategies | [动态收益](products/zh-CN/dynamic.md) | [Dynamic yield](products/en/dynamic.md) |

## 维护与发布

1. 同时修改对应产品的中英文文件，更新 manifest 的 `updatedAt`。金额、计息、派息、转让及退出规则必须与已确认 PRD 一致；未开放或待定的安排明确标注。
2. 文档报价是注明口径的参考配置；应用的实际利率、版本、期次日期、额度与开关仍由链上读取。调整文案不改变合约条款。
3. 提交并推送本仓库。在 `tychefi.webui` 执行 `pnpm docs:sync --repo ../tychefi.docs --revision <完整提交 SHA>`，导入该提交的中英文快照、路径及版本信息。
4. 运行 WebUI 测试和构建，再发布前端。页面提供指向对应文档提交的源码链接，便于核对。

应用构建使用固定提交快照，无需用户浏览器实时访问 GitHub；GitHub 中的未发布编辑不会自动改写线上产品说明。

合约、权限、完整 PRD 及测试链部署证据继续存放于 [tyche.contracts/docs](https://github.com/tychefi/tyche.contracts/tree/main/docs)，不在本仓库重复维护实现说明。

## 风险指数

各产品的 `risk` 字段维护内部指数（1.0～5.0，支持一位小数，未评估为 null）、提供方、更新时间和五个风险维度。前端以刻度和文字同时展示，详情可展开具体因素；定义见 [风险分级方法 / Rating approach](RISK-METHODOLOGY.md)。评级不表示亏损概率，也不按收益率自动生成。

## 产品级策略团队

专业理财团队、策略执行方、合作经历及历史表现只能在对应产品中披露，不能上升为全平台或某一产品类别的统一介绍。当前四个固收产品已分别确认适用同一段套利团队背景，并各自在中英文文件中维护；新产品不得自动继承。TycheFi 的平台管理与固收兑付责任，和专业团队的策略执行职责分别说明。

Professional strategy teams, execution arrangements, partnership history and historical performance are disclosed per product, without platform-wide or category-wide inheritance. The same arbitrage background has been explicitly confirmed for the four current fixed-income products and is maintained in each product's bilingual files. A new product must disclose its own arrangements. TycheFi's platform management and repayment obligations are distinct from strategy execution.
