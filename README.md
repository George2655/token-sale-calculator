# Token Sale Calculator

A simple Web3 calculator for estimating token sale allocation, token price, ROI, TGE unlock value and target FDVs.

Live demo:  
https://george2655.github.io/token-sale-calculator/

## Features

- Estimate allocation after oversubscription
- Calculate token sale price from FDV and total supply
- Calculate expected token price at target FDV
- Estimate tokens received
- Calculate unlocked and locked tokens at TGE
- Estimate position value and profit
- Calculate TGE value and locked value
- Show break-even, 2x and 3x FDV targets

## Example

If:

- Investment: $1,000
- Oversubscription: 2x
- Sale FDV: $40M
- Expected FDV: $100M
- Total Supply: 1B tokens
- TGE Unlock: 25%

The calculator estimates:

- Allocation: $500
- Sale Token Price: $0.04
- Tokens Received: 12,500
- Expected Multiple: 2.5x
- Position Value: $1,250
- TGE Value: $312.50

## Tech Stack

- HTML
- CSS
- JavaScript
- GitHub Pages

## How It Works

The calculator uses the token sale FDV and total token supply to estimate the token price at the sale.

It then compares the sale FDV with the expected FDV to calculate the potential multiple and future position value.

Oversubscription is used to estimate the actual allocation received in a public sale.

## Run Locally

Download or clone the repository:

```bash
git clone https://github.com/George2655/token-sale-calculator.git
