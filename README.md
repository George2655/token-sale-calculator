# Token Unlock Calculator

A browser-based tool for exploring how token unlocks change circulating supply and estimating hypothetical selling scenarios.

**[Open the calculator →](https://george2655.github.io/token-unlock-calculator/)**

## Features

- Calculate circulating supply growth after an unlock
- Estimate the value of unlocked tokens at a chosen price
- See the new circulating supply and its share of total supply
- Calculate tokens unlocked per day
- Model a hypothetical share of unlocked tokens being sold
- Compare hypothetical daily selling value with average daily trading volume
- View a circulating supply projection chart
- Switch between light and dark themes, with your preference saved locally
- Use a responsive layout on desktop and mobile
- Validate inputs, including supply limits and zero-denominator cases

## How to use

1. Enter total supply, current circulating supply and the number of tokens being unlocked.
2. Set the token price and unlock duration in days.
3. Enter the hypothetical percentage of unlocked tokens sold and average daily trading volume in USD.
4. Click **Calculate scenario** to update the results and chart.

Use the same token unit for all supply fields. For a single cliff unlock, set the duration to **1 day**.

## Example

With the default inputs:

| Input | Value |
| --- | ---: |
| Total supply | 1,000,000,000 tokens |
| Current circulating supply | 150,000,000 tokens |
| Upcoming unlock | 30,000,000 tokens |
| Token price | $0.05 |
| Unlock duration | 30 days |
| Share of unlocked tokens sold | 25% |
| Average daily trading volume | $500,000 |

The calculator returns:

| Result | Value |
| --- | ---: |
| Circulating supply growth | +20% |
| Total unlock value | $1,500,000 |
| New circulating supply | 180,000,000 tokens |
| New circulation / total supply | 18% |
| Tokens unlocked per day | 1,000,000 |
| Hypothetical total selling value | $375,000 |
| Hypothetical daily selling value | $12,500 |
| Daily selling / daily trading volume | 2.5% |
| Market cap after unlock at the fixed price | $9,000,000 |

## Calculation model

```text
New circulating supply = Current circulating supply + Unlocked tokens
Supply growth (%) = Unlocked tokens / Current circulating supply × 100
Unlock value = Unlocked tokens × Token price
Daily unlocked tokens = Unlocked tokens / Duration in days
Hypothetical selling value = Unlock value × Share sold (%) / 100
Daily selling value = Hypothetical selling value / Duration in days
Daily selling / volume (%) = Daily selling value / Daily trading volume × 100
Market cap after unlock = New circulating supply × Token price
```

Supply growth is shown as **N/A** when current circulating supply is zero. The daily selling / volume ratio is shown as **N/A** when daily trading volume is zero.

## Assumptions and limitations

- All unlocked tokens are assumed to enter circulation.
- Unlocks and hypothetical selling are spread evenly across the selected period.
- Token price and daily trading volume remain fixed in the model.
- Inputs are entered manually; the tool does not fetch live market data.
- Trading volume is not order-book liquidity. The selling / volume ratio does not predict price impact or a future token price.

This tool is for scenario exploration and educational use, not financial advice.

## Tech stack

- HTML
- CSS
- Vanilla JavaScript
- SVG chart
- GitHub Pages

## Run locally

Download or clone this repository and open `index.html` in your browser. No build step or dependencies are required.

## Feedback

Found a bug or have an idea for a useful feature? Open an issue in this repository with the details.
