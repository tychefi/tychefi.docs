# Tyche Fixed · 3M

## Overview

A **3-month lock-up**, with fundraising, a common accrual start and a common maturity for each series. Each series has its own fungible share token. **1 USDT of principal = 1 share token**, both with 6 decimals.

This is a FLON Testnet product using test assets only. Subscription requires both switches to be open, an eligible fundraising window and remaining capacity. A displayed quote does not make every series available.

## Returns and fees

The current template is **8% gross APR**, an annual management fee of **2% of principal**, and **6% monthly-mode net APR**. Daily mode receives 70% of net interest, equivalent to **4.2% net APR**. The fee is based on principal, not profits.

Series rates are configurable before fundraising. Gross APR is capped at 10%, the fee is 2%, and monthly net APR is capped at 8%. The series terms confirmed on subscription govern; later template changes cannot rewrite a series after fundraising starts.

## Fundraising and accrual start

Fundraising principal remains in the contract, earns nothing and cannot be withdrawn for investment. Valid subscriptions atomically mint shares 1:1. Shares cannot transfer during fundraising. Success is confirmed at the close only if the minimum raise is met; at least 24 hours separate the close and accrual start.

Accrual starts at UTC+8 midnight. Maturity is the corresponding day 3 calendar months later, or month-end if needed. Refer to the actual series dates.

If fundraising fails or the manager cancels before success, returning shares starts a **24-hour** deadline for a full interest-free refund. Successful fundraising cannot be cancelled; only then can principal become investable.

## Per-second interest and payments

`Net interest = principal × locked net APR × actual seconds held / (365 × 86400)`

Intervals include the start and exclude the end. Daily-mode intervals receive 70%. Exact entitlement accumulates per account and series; when payable, cumulative amounts are rounded down to **2 USDT decimals**, less amounts already scheduled or paid. Remainders carry forward.

| Mode | Entitlement | Payment deadline (UTC+8) |
| --- | --- | --- |
| Monthly | Full net interest; reference APR 6% | Previous month's interest on the 1st–7th, by 23:59:59 on the 7th |
| Daily | 70% of net interest; reference APR 4.2% | By 23:59:59 the day after the accrual interval |

Choose a mode on subscription. Later changes take effect at 00:00 on the next month's 1st; the current month retains its old mode. No token swap is needed and past daily discounts are not refunded. Further subscriptions to the same series retain the account's current mode.

## Liquidity during lock-up

Lock-up prevents principal repayment by the Vault before maturity; it does not prohibit all token transfers. Ordinary transfers open at the common accrual start and stop at maturity. Quantity-based transfers are supported.

Pre-transfer accrued interest stays with the seller. The buyer accrues from receipt using their own settings; a first-time holder defaults to monthly mode. Future principal redemption rights follow the token. Historical paid interest is not paid again.

Direct transfers are supported; platform order matching and market escrow are not open. Early exit needs a buyer, with no guaranteed price or liquidity. The flexible product's 14-day early-redemption route does not apply.

## Maturity, continued holding and repayment

Accrual stops at maturity. Tokens may still be held, retaining the principal claim; unpaid accrued income remains with its registered account. **There is no automatic renewal or additional accrual.** Ordinary transfers stop; tokens may only be returned for repayment.

Return shares to the Vault to request repayment, including partial quantities. Shares booked before maturity are locked and continue earning until maturity; they can no longer transfer.

- Book before maturity: principal and unpaid final interest arrive by 18:00 the following day after maturity.
- Return after maturity: payment is due within 24 hours of confirmation.
- Earlier deadlines for separately recorded monthly or daily interest remain unchanged.

Payment and the corresponding token burn are atomic: insufficient cash cannot burn shares without paying.

## Funds, responsibility and risks

Authorized roles may withdraw successfully raised investable principal to the Tyche team's account, convert it to fiat for futures arbitrage, then return USDT for payments. Each series segregates fundraising principal, investable principal, interest and redemption cash. Tyche is responsible for the specified principal and net interest shortfalls, subject to its actual funding and ability to perform.

Risks include markets, margin, execution, counterparties, off-chain custody, conversion, returning liquidity, contracts, wallets and networks. Shares do not guarantee an immediate buyer or prove all principal remains on-chain. For help, join [TycheFi Telegram](https://t.me/tychefi).
