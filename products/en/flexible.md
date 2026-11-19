# Tyche Flexible

## Health and risk indices

Current reference configuration: **health index 4.9 / 5**, corresponding to **risk index 0.1 / 5**. Both use a 0–5 internal scale: risk index = 5 − health index. Higher health expresses lower risk on this scale. The app reads the actual independent configuration from `tyche.vault`; on-chain values govern.

TycheFi supplies these indices. They are not independent ratings, loss probabilities, drawdown estimates or principal protection, and are not inferred from APR. The five explanatory factors are liquidity, strategy and markets, custody and conversion, repayment and loss allocation, and contracts and networks. See the [health and risk index approach](https://github.com/tychefi/tychefi.docs/blob/main/HEALTH-AND-RISK.md).

## Overview

Subscribe with USDT to a Vault managed by the TycheFi team. There is no fixed lock-up and no token: principal and income belong to each deposit's original account. Full-deposit redemption can be requested anytime. The product is available on FLON Testnet using test assets only; the on-chain subscription switch determines availability.

## This product’s trading expertise and partnership

According to the TycheFi team, this product’s strategy is executed by a team led by a **world-class arbitrage trader with 20 years of experience**. The team conducts long-running cross-market arbitrage between futures exchanges worldwide. The trader has worked with the team for **five years**. The team reports that the strategy's historical annualized returns have consistently remained at **10%–11%**.

This is team-provided strategy background and historical performance information, not this Vault's user net APR. Gross APR, management fees and user net APR follow the on-chain terms locked on subscription. Past performance does not indicate future returns.

## Returns and fees

The current reference for new deposits is **7% gross APR**, less an annual fee of **2% of principal**, giving **5% net APR**. The fee is not 2% of profits. Each confirmed deposit locks its on-chain rate and version; later changes do not rewrite existing deposits.

`Cumulative net interest = principal × locked net APR × actual accrual days / 365`

Principal uses USDT's 6 decimals. For each deposit, cumulative net interest is rounded down to 2 decimals, then scheduled and paid amounts are subtracted. Fractions carry forward rather than being discarded monthly.

## Subscription, accrual and payments

1. Subscribe to `tyche.vault` with the designated USDT. Pending principal remains in the contract and earns nothing.
2. The team must activate it within **168 hours** of confirmation. Accrual begins on its actual UTC+8 start day.
3. Interest eligibility requires **one calendar month**. If the corresponding day does not exist in the next month, use month-end. Interest is recorded before eligibility and settled once eligible.
4. Monthly cutoff is 00:00 on the 1st, with payment by 18:00 on the 3rd. The first payment is due by 18:00 the day after eligibility.

Flexible accrual uses calendar days: include the start day and exclude the confirmed redemption-request day. All times are UTC+8.

## Lock-up and redemption

There is no maturity. Request redemption of the **entire deposit** anytime; this is not instant liquidity. Accrual stops on confirmation. Expected payment is 7–14 days, with a firm deadline of **336 hours** from on-chain confirmation and no additional grace period.

Before one calendar month, redemption earns no interest and returns principal in full, without a separate management fee deducted from principal. After eligibility, unpaid net interest is settled without paying previous interest twice. Payments go to the original account. Deposits cannot be transferred or partially redeemed.

## Overdue activation refunds

After 168 hours without activation, activation closes. Request a full interest-free refund, due within **24 hours** of confirmation, using the pending principal retained in the contract.

## Use of funds and responsibility

`tyche.vault` receives funds. After activation, authorized treasury roles may withdraw investable principal to the team's account, convert it to fiat for futures arbitrage strategies, then return USDT for interest and redemptions. Pending principal, investable principal, interest and redemption cash have separate ledgers; other products' cash is protected.

The Tyche team is responsible for fixed-income principal and the specified net returns, including covering principal losses and interest shortfalls. Performance depends on its ability to fund repayment. This does not mean principal always remains in the contract or that strategies are risk-free.

## Main risks

Risks include markets, margin, execution, counterparties, off-chain custody, conversion and returning liquidity, as well as contracts, wallets and networks. Redemptions require sufficient USDT from the team; shortages do not extend payment deadlines.

## Using the product

Check the on-chain net APR, fee and exit terms in Vault details before subscribing. Portfolio shows each deposit and offers redemption or overdue refunds. For help, join [TycheFi Telegram](https://t.me/tychefi).
