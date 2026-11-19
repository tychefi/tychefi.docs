# Tyche Strategies

## Health and risk indices

**Not rated**. Placeholder values do not mean zero risk or a health rating. Both use a 0–5 internal scale: risk index = 5 − health index. Higher health expresses lower risk on this scale. The app reads the actual independent configuration from `tyche.vault`; on-chain values govern.

TycheFi supplies these indices. They are not independent ratings, loss probabilities, drawdown estimates or principal protection, and are not inferred from APR. The five explanatory factors are liquidity, strategy and markets, custody and conversion, repayment and loss allocation, and contracts and networks. See the [health and risk index approach](https://github.com/tychefi/tychefi.docs/blob/main/HEALTH-AND-RISK.md).

## Availability

Dynamic yield Vaults are **in preparation: subscriptions, share issuance, trading and redemption are not open**. This page describes the agreed product form, not a live strategy, portfolio, fee schedule or return. No verifiable target APR, performance history or fixed lock-up is currently offered.

## Difference from fixed income

Gains, losses and fees change the share NAV. Holders bear volatility and principal drawdowns. Fixed-income APRs, its 2% management fee and Tyche's fixed-income shortfall obligations do not apply to this product.

## Shares and subscriptions

Each dynamic Vault is planned to issue one fungible token, with shares calculated at settlement NAV rather than a fixed 1 USDT = 1 share.

`Shares issued = net subscription amount used for issuance / settlement NAV per share`

A subscription funds the Vault and creates shares. Secondary trading pays another holder for existing shares. Redemption returns shares for settlement at redemption NAV and applicable fees. These are separate cash flows.

## Lock-up, liquidity and fees

Strategy, eligible assets, valuation sources and frequency, management and performance fees, lock-up, subscription/redemption windows, queues and payment deadlines must be disclosed before launch. **These terms are currently undecided.** A token does not imply instant redemption or a guaranteed buyer.

Quantity-based trading and partial fills are planned. Market prices may differ from NAV. Market, custody and liquidity terms depend on launch disclosures; no trading entry point is currently provided.

## Management and risks

Only the TycheFi team provides Vaults; third parties cannot create them. Returns must be explained through disclosed strategies, not replaced by unannounced rewards.

Risks include strategy losses, valuation uncertainty, markets and liquidity, execution, counterparties, custody, contracts and networks. Read the final product terms before launch. For help, join [TycheFi Telegram](https://t.me/tychefi).
