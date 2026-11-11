# Buyback Arbitrage Math & 3-Scenario Modeling

This guide defines the mathematical formulas, scenario parameters, and tender/exit execution plans for every buyback deep dive.

---

## 1. The Retail Arbitrage Mechanics

### Step 1: Capital & Share Sizing
Under SEBI Regulation 6, an investor qualifies for the **15% Small Shareholder Retail Quota** only if their total market holding in that company on the Record Date does not exceed ₹2,00,000:

$$N = \left\lfloor \frac{2,00,000}{\text{Purchase Price } (P_{\text{buy}})} \right\rfloor$$

$$\text{Total Capital Outlay } (C) = N \times P_{\text{buy}}$$

### Step 2: Tender & Acceptance Distribution
When the tender window opens, the investor **tenders all $N$ shares**:

- **Accepted Shares ($A$)**:
  $$A = \text{round}(N \times \text{AR})$$
  *(where $\text{AR}$ is the Estimated Acceptance Ratio, e.g. 40% = 0.40)*
- **Unaccepted Shares Returned ($U$)**:
  $$U = N - A$$

### Step 3: Gross Arbitrage Return
Accepted shares are bought back by the company at the fixed **Buyback Price ($P_{\text{bb}}$)**:
$$\text{Gain on Accepted Shares} = A \times (P_{\text{bb}} - P_{\text{buy}})$$

Unaccepted shares are credited back to the Demat account and valued or sold at the **Post-Buyback Market Price ($P_{\text{post}}$)**:
$$\text{P&L on Unaccepted Shares} = U \times (P_{\text{post}} - P_{\text{buy}})$$

$$\text{Gross Profit } (\Pi) = \left[ A \times (P_{\text{bb}} - P_{\text{buy}}) \right] + \left[ U \times (P_{\text{post}} - P_{\text{buy}}) \right]$$

---

## 2. The 3 Standard Post-Buyback Price Scenarios

Because the post-buyback market price ($P_{\text{post}}$) cannot be known in advance, every analysis must calculate outcomes across these three standardized market scenarios:

### Scenario A: Bull Case (Full Price Recovery)
- **Assumption**: $P_{\text{post}} = P_{\text{buy}}$
- The stock price holds steady or recovers back to the pre-buyback purchase price after the record date.
- **Result**: Zero loss on unaccepted shares. Total profit equals the full premium on accepted shares.

### Scenario B: Base Case (Routine 5%–8% Post-Record Date Dip)
- **Assumption**: $P_{\text{post}} = P_{\text{buy}} \times (1 - 0.06)$  *(6% price adjustment)*
- Historically, once the eligibility record date passes, stocks experience a mild 5% to 8% dip as short-term record-date traders exit.
- **Result**: The premium gain on accepted shares easily cushions the small mark-to-market dip on unaccepted shares, yielding a positive net return.

### Scenario C: Bear Case (12%–15% Market Correction)
- **Assumption**: $P_{\text{post}} = P_{\text{buy}} \times (1 - 0.14)$  *(14% market correction)*
- Broader market downturn or negative earnings announcement causes the unaccepted shares to decline sharply.
- **Result**: Tests the safety margin of the deal to see if the buyback premium still protects capital.

---

## 3. Break-Even Acceptance Ratio ($AR_{\text{be}}$)

The break-even acceptance ratio tells the investor the **absolute minimum percentage of shares** that must be accepted for the trade to break even (Gross Profit = 0) at a given post-buyback price $P_{\text{post}}$:

$$AR_{\text{be}} = \frac{P_{\text{buy}} - P_{\text{post}}}{P_{\text{bb}} - P_{\text{post}}} \times 100$$

*Example*: If $P_{\text{buy}} = ₹300$, $P_{\text{bb}} = ₹400$, and the stock drops 10% to $P_{\text{post}} = ₹270$:
$$AR_{\text{be}} = \frac{300 - 270}{400 - 270} = \frac{30}{130} \approx 23.08\%$$
If the estimated acceptance ratio is 45%, this trade has a significant safety cushion ($45\% > 23\%$).

---

## 4. Post-Buyback Execution Plan for Unaccepted Shares

Every deep dive must prescribe an explicit post-settlement action plan:

1. **Strategy 1: Immediate Arbitrage Liquidation (Recommended for Pure Arbitrageurs)**
   - Sell all unaccepted shares ($U$) in the open market on the day they are credited back to Demat.
   - Realizes the cash profit immediately and frees capital for the next corporate action.

2. **Strategy 2: Tender-and-Hold (For Quality Fundamental Businesses)**
   - If the company has high ROE (>18%), zero debt, and positive EPS accretion from the extinguished shares, hold the unaccepted shares for long-term compounding.
   - Set an explicit **Trailing Stop-Loss**: Exit unaccepted shares if the price closes below the 200-day moving average or 10% below $P_{\text{buy}}$.

