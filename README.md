# crypto futures: how perpetual contracts, leverage, fees, and risk management work on OKX

Searching for **crypto futures** usually means you want more than a definition. You probably want to understand how futures work, whether perpetual contracts expire, how much leverage is sensible, what fees to expect, and how to open a trade without discovering the important details after the position is already losing money.

This guide covers those practical questions and uses OKX as the working example. It explains the difference between spot and futures, how long and short positions work, how funding and liquidation affect the trade, how OKX futures fees are structured, and what to check before using the provided invitation link.

The link below is an OKX affiliate link associated with the code **CASH20**, advertised with a **20% rebate**. The exact rebate and eligibility should be confirmed on the registration or rewards screen because referral benefits can vary by account, region, product, and campaign.

[👉 Check the OKX futures offer and confirm the available rebate](https://okx.com/join/CASH20)

## What are crypto futures?

Crypto futures are derivative contracts that track the price of a cryptocurrency. You trade exposure to an asset such as Bitcoin or Ethereum without necessarily buying and holding the underlying coin in a spot wallet.

A futures position can be:

- **Long**, if you expect the contract price to rise.
- **Short**, if you expect the contract price to fall.
- **Leveraged**, meaning the position has a larger notional value than the margin deposited.
- **Settled in crypto or stablecoins**, depending on the contract type.

This creates more flexibility than ordinary spot trading, but it also introduces additional costs and risks. A spot trader can buy BTC and hold it through a downturn. A leveraged futures trader may have the position liquidated before the market has a chance to recover.

That difference is the whole story in miniature.

On OKX, futures products include perpetual futures and expiry futures. Perpetual futures do not have a fixed expiry date. Instead, a funding mechanism helps keep the perpetual contract price close to the underlying spot market. Expiry futures settle on a specified future date and use a defined settlement process.

## Crypto futures versus spot trading

The easiest way to understand futures is to compare them with buying cryptocurrency directly.

| Feature | Spot trading | Crypto futures |
| --- | --- | --- |
| What you trade | The underlying crypto asset | A derivative contract tracking the asset |
| Direction | Usually profits when price rises | Can profit from rising or falling prices |
| Leverage | Usually unavailable or limited | Available, subject to contract and account limits |
| Expiry | No expiry | Perpetual or fixed expiry |
| Main costs | Trading fee, withdrawal fee, spread | Trading fee, funding, spread, liquidation-related costs |
| Liquidation | Usually no forced liquidation if fully paid | Possible when margin falls below requirements |
| Ownership | You may hold the actual asset | You hold contractual exposure rather than the asset itself |
| Best suited to | Investing, holding, transfers | Hedging, short-term trading, directional strategies |

Suppose Bitcoin is trading at $60,000 and you buy $1,000 of BTC on the spot market. A 10% price decline produces an unrealized loss of roughly $100, excluding fees.

Now suppose you use $1,000 as margin for a $5,000 futures position. The same 10% move against the position represents a $500 loss before fees and funding. The price move has not changed, but the position has five times the exposure.

Leverage does not make the market more predictable. It simply makes the result arrive faster.

## How perpetual futures work

Perpetual futures resemble traditional futures contracts, but they do not have a fixed expiration date. You can keep a position open while the account maintains enough margin and the contract remains available.

Because there is no expiry date forcing the contract to converge at settlement, perpetual futures use **funding payments**. Funding is transferred between long and short traders according to the current funding rate.

When the funding rate is positive, longs generally pay shorts. When it is negative, shorts generally pay longs. The exact payment depends on the contract, position size, funding rate, and settlement schedule.

The funding rate is separate from the trading fee. You can pay a trading fee when your order is filled and later pay or receive funding while the position remains open.

OKX displays the current funding rate, the side expected to pay at the next settlement, the countdown to settlement, and the applicable funding interval on the futures trading interface. The interval varies by contract. OKX gives BTCUSDT perpetual as an example of an eight-hour funding interval and notes that some other contracts use different intervals.

That matters for trades held overnight or for several days. A position that looks profitable based only on entry and exit prices may produce a smaller result after repeated funding payments.

## Margin, leverage, and position size

Futures traders usually think about three related numbers:

1. **Margin**: the collateral assigned to the position.
2. **Leverage**: the relationship between position value and margin.
3. **Notional value**: the total value of the futures position.

A simple example:

- Margin: $500
- Leverage: 5x
- Position value: approximately $2,500

If the underlying asset rises by 4% and the position is long, the gross profit is approximately $100 before fees and funding. That is a 20% return on the $500 margin, again before costs.

If the asset falls by 4%, the gross loss is approximately $100. The same leverage that magnified the gain magnifies the loss.

The actual liquidation level is not determined by a simple “price moved against me by 20%” formula. It depends on the contract, maintenance margin, leverage, account mode, fees, mark price, other open positions, and whether the position uses isolated or cross margin.

### Isolated margin

With isolated margin, a specific amount of collateral is assigned to the position. A loss on that position does not automatically use the entire available trading balance in the same way cross margin can.

Isolated margin is easier to reason about when you want to cap the collateral assigned to one trade. It does not eliminate risk, and the position can still be liquidated.

### Cross margin

With cross margin, available account funds may support the position. This can delay liquidation in some situations, but it also means more of the account may be exposed if the market moves against the trade.

OKX explains that isolated margin uses designated funds, while cross margin can use the broader account balance depending on the account mode. Its Unified Account system includes single-currency, multi-currency, and portfolio margin modes, each with different collateral and risk behavior.

For someone learning crypto futures, isolated margin and modest leverage are generally easier to understand than a cross-margin setup involving several positions. The important point is not which mode sounds more advanced. It is whether you know exactly which assets can be used to support a losing trade.

## What are maker and taker fees?

Crypto futures fees are usually divided into **maker** and **taker** fees.

A taker order executes immediately against existing orders in the order book. Market orders usually fall into this category.

A maker order adds liquidity to the order book and is not filled immediately. A limit order can receive maker pricing if it rests on the book rather than matching immediately.

OKX’s published example for a regular futures user shows a **0.0200% maker fee** and a **0.0500% taker fee** for both listed futures groups. The fee is charged on the executed notional value, not simply on the margin deposited.

For example, if a USDT-margined futures order has a notional value of $10,000:

- At a 0.0200% maker fee, the trading fee is about **$2**.
- At a 0.0500% taker fee, the trading fee is about **$5**.

Opening and closing are charged separately when each order is executed. A round trip can therefore involve an opening fee and a closing fee, plus any applicable funding.

OKX’s formula for USDT- and USDC-margined futures is based on the fee rate multiplied by the number of contracts, contract multiplier, contract size, and fill price. Crypto-margined contracts use a different settlement calculation.

A limit order is not automatically a maker order. If it executes immediately, it may be treated as a taker order. Always check the fee preview and execution details rather than assuming the order type alone determines the final fee.

## OKX crypto futures fee tiers

OKX does not present futures as a set of monthly subscription plans. Instead, its futures fee schedule uses account tiers based on asset balances and/or 30-day trading volume.

The current published futures schedule lists a regular tier and VIP 1 through VIP 9. The table below includes the full set of futures fee tiers shown on the official schedule. The qualification thresholds are displayed as alternatives, using account assets or 30-day trading volume. Fees and product availability can vary by jurisdiction and may be reviewed by OKX over time.

| Tier | Qualification shown by OKX | Maker fee | Taker fee | 24-hour crypto withdrawal limit shown | Futures access |
| --- | ---: | ---: | ---: | ---: | --- |
| Regular user | Under $100,000 assets or under $10 million 30-day volume | 0.0200% | 0.0500% | $10 million | [ View OKX futures access](https://okx.com/join/CASH20) |
| VIP 1 | At least $100,000 assets or at least $10 million 30-day volume | 0.0180% | 0.0400% | $20 million | [ View VIP 1 conditions](https://okx.com/join/CASH20) |
| VIP 2 | At least $250,000 assets or at least $50 million 30-day volume | 0.0130% | 0.0350% | $24 million | [ View VIP 2 conditions](https://okx.com/join/CASH20) |
| VIP 3 | At least $500,000 assets or at least $100 million 30-day volume | 0.0100% | 0.0280% | $32 million | [ View VIP 3 conditions](https://okx.com/join/CASH20) |
| VIP 4 | At least $2 million assets or at least $200 million 30-day volume | 0.0080% | 0.0270% | $40 million | [ View VIP 4 conditions](https://okx.com/join/CASH20) |
| VIP 5 | At least $5 million assets or at least $600 million 30-day volume | 0.0050% | 0.0260% | $48 million | [ View VIP 5 conditions](https://okx.com/join/CASH20) |
| VIP 6 | At least $10 million assets or at least $1 billion 30-day volume | 0.0000% | 0.0250% | $60 million | [ View VIP 6 conditions](https://okx.com/join/CASH20) |
| VIP 7 | No asset threshold shown or at least $1.5 billion 30-day volume | -0.0020% | 0.0200% | $72 million | [ View VIP 7 conditions](https://okx.com/join/CASH20) |
| VIP 8 | No asset threshold shown or at least $2 billion 30-day volume | -0.0050% | 0.0200% | $80 million | [ View VIP 8 conditions](https://okx.com/join/CASH20) |
| VIP 9 | No asset threshold shown or at least $20 billion 30-day volume | -0.0050% for Group 1; -0.0100% for Group 2 | 0.0150% for Group 1; 0.0200% for Group 2 | $80 million | [ View VIP 9 conditions](https://okx.com/join/CASH20) |

A negative maker fee means the published tier may provide a rebate for eligible maker volume. It does not mean every order earns money, and it does not remove spread, slippage, funding, liquidation, or market risk.

For most individual traders, the practical comparison is between the regular tier and the first few VIP levels. The highest tiers require very large balances or trading volumes that are far beyond what a typical beginner should pursue simply to reduce fees.

## What does the 20% OKX rebate mean?

The provided OKX link uses the invitation code **CASH20** and is advertised with a 20% rebate. OKX’s affiliate documentation states that invitee rebate rates can range from 0% to 20%, while the specific rate assigned to an account can be checked inside the app’s rewards area.

That distinction matters. A referral link may be valid while the final rebate depends on:

- Whether the account is new or already linked to another referrer.
- The country or region associated with the account.
- The product being traded.
- Whether the user is joining through the correct registration flow.
- Current campaign terms.
- Whether the rebate is displayed and assigned after registration.

The safest process is:

1. Open the affiliate link before creating the account.
2. Confirm that the invitation code or referral relationship appears.
3. Complete the required identity verification, if applicable.
4. Check the rewards or referral section for the assigned rebate.
5. Confirm the trading fee preview before placing a futures order.

Do not assume that a referral rebate makes a leveraged position profitable. A discount reduces one cost. It does not protect against a price move, funding payment, spread, slippage, or liquidation.

## How to place a crypto futures trade on OKX

The exact interface can change, but OKX’s published process follows a straightforward sequence.

### 1. Select the futures market

Open the futures section and choose a contract such as a BTCUSDT perpetual. Check the contract name carefully. BTCUSDT perpetual, BTCUSD perpetual, and dated BTC futures can have different settlement currencies, contract sizes, funding behavior, and risk parameters.

### 2. Transfer funds to the trading account

Funds may need to be transferred from the funding account to the trading account before a futures order can be placed. Select the asset and amount, then verify that the balance is assigned to the correct account.

### 3. Choose the margin currency and contract type

USDT-margined contracts use USDT as collateral or settlement currency for the relevant position. Crypto-margined contracts use the underlying cryptocurrency or another contract-specific asset.

The margin asset changes the way profit, loss, and fees appear in the account. It also changes the risk of holding collateral whose own market price is moving.

### 4. Choose isolated or cross margin

Select the margin mode before entering the trade. If the position is intended to have a clearly defined collateral allocation, isolated margin may be easier to monitor. Cross margin requires a more complete understanding of how account balances interact with open positions.

### 5. Set leverage

Choose leverage conservatively. The highest available leverage is not a target. It is simply a maximum permitted setting for a particular product and account.

A lower leverage setting gives the position more room before liquidation, although position size still matters. Someone can create a risky trade with low leverage by making the position too large relative to the account.

### 6. Select an order type and size

Enter the price, quantity, and order type. Review the estimated margin, liquidation price, trading fee, and other displayed details.

A market order may execute quickly but can incur taker fees and slippage. A limit order may improve price control, but it may not fill. During rapid price movement, an order that appears close to the market can also become immediately executable and be treated as a taker.

### 7. Open and monitor the position

Choose Buy/Long if you expect the contract price to rise, or Sell/Short if you expect it to fall. After execution, monitor:

- Entry price
- Mark price
- Liquidation price
- Unrealized profit or loss
- Funding rate and next settlement time
- Margin ratio
- Position size
- Remaining account balance

The mark price is especially important because liquidation is not necessarily based only on the last traded price. The relevant calculation depends on the platform’s contract and risk rules.

### 8. Close the position deliberately

A position can be closed fully or partially. Before confirming the close, check whether the order will execute as a maker or taker and what fee applies.

OKX notes that a market close-all action may incur the higher taker fee, while a limit order can be cheaper if it rests on the order book and receives maker treatment.

## Liquidation: the risk new traders underestimate

Liquidation occurs when the position no longer has enough margin to satisfy the required maintenance level. The exchange can forcibly close the position, potentially when the market is moving quickly and available liquidity is changing.

OKX’s risk disclosure describes perpetual futures as complex leveraged instruments. It warns that leverage can magnify gains and losses, and that a position may be automatically closed when margin falls below the required maintenance level. It also warns that forced liquidation can occur rapidly during volatile markets.

A stop-loss can reduce the chance of reaching liquidation, but it is not a guarantee of a specific exit price. In a fast market, the order may fill at a worse price than expected. A stop-loss also does not replace sensible position sizing.

Before opening a trade, decide:

- How much account equity can be exposed.
- Where the trade thesis is invalidated.
- Whether the stop distance is realistic for the market.
- How funding affects the expected return.
- Whether the position can survive normal volatility.
- What happens if the order cannot be closed immediately.

If the answer depends on the market moving perfectly, the position is probably too large.

## A practical risk checklist for crypto futures

Use this checklist before placing a first or unfamiliar futures trade:

1. **Confirm the contract.** Check whether it is perpetual or expiry, USDT-margined or crypto-margined, and whether the contract is available in your jurisdiction.
2. **Check the contract specifications.** Review contract size, tick size, minimum order size, leverage limit, funding interval, and settlement rules.
3. **Use a position size based on acceptable loss.** Start with the loss you can tolerate, then work backward to the position size.
4. **Prefer isolated margin while learning.** This can make the collateral assigned to a position easier to track.
5. **Avoid maximum leverage.** High leverage compresses the distance to liquidation.
6. **Account for both sides of the trade.** Include the opening fee, closing fee, spread, slippage, and possible funding.
7. **Watch the mark price and margin ratio.** The last traded price alone does not tell you how close the position is to liquidation.
8. **Do not average down automatically.** Adding to a losing leveraged position can increase liquidation risk quickly.
9. **Keep spare funds separate.** Do not leave more collateral in a cross-margin account than you are willing to expose.
10. **Verify local availability and rules.** OKX states that not all futures pairs and features are available in every jurisdiction.

## Is OKX suitable for crypto futures beginners?

OKX provides the core tools needed to study and trade futures: perpetual and expiry contracts, different margin modes, leverage controls, maker and taker pricing, funding data, order types, and account modes.

That does not make futures a beginner-friendly product by default. The interface may be straightforward, but the underlying instrument remains leveraged and can be liquidated. A new trader should first understand the contract, funding, margin, fees, and exit process before focusing on strategies or high leverage.

The platform is a more reasonable fit when you:

- Want to trade both long and short.
- Understand that futures do not represent ordinary ownership of the underlying asset.
- Can calculate position value and margin.
- Are comfortable checking funding before holding a position.
- Have a written loss limit.
- Can verify that futures are available in your region.

It is a poor fit if you are looking for a guaranteed way to multiply a small account quickly. No referral code, fee discount, or exchange interface changes that basic fact.

## Final take

Crypto futures offer tools that spot trading does not: short exposure, leverage, perpetual contracts, and the ability to hedge an existing position. They also add funding, liquidation, margin requirements, and more ways for a small mistake to become an expensive one.

On OKX, the regular futures fee shown in the current schedule is 0.0200% for makers and 0.0500% for takers, with lower rates available at higher VIP tiers. The provided **CASH20** link may assign a rebate of up to 20%, but the final benefit should be confirmed during registration and inside the account’s rewards section.

Use the affiliate link only after checking the displayed terms, then verify the contract details before trading. The sensible first objective is not to maximize leverage. It is to understand exactly how much one position can lose, what it costs to hold, and how you will close it before the market makes that decision for you.

[👉 Open the OKX invitation link and review the available futures rebate](https://okx.com/join/CASH20)
