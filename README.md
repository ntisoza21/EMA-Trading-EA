# EMA Trading EA Collection

A compact set of MetaTrader 5 Expert Advisors built around EMA trend logic, with optional RSI confirmation, partial profit exits, and risk-based lot sizing.

This project is intended as a starting point for strategy development and testing in MetaEditor. It is not financial advice and should only be used on a demo account before any live trading.

## Project purpose

The collection includes multiple EA variants that share the same core idea:

- EMA 5, 20, 50, 200 trend detection
- Buy and sell entries based on trend alignment
- Profit-taking logic
- Re-entry behavior when a valid signal remains active
- Optional RSI confirmation
- Partial close logic
- Risk-based position sizing

## Included EA files

- `EMA_Trend_ReEntry_EA.mq5`  
  Basic EMA strategy with re-entry logic and profit close.

- `EMA_RSI_EA.mq5`  
  EMA trend strategy with RSI confirmation filter.

- `EMA_Partial_Close_EA.mq5`  
  EMA strategy with partial close logic.

- `EMA_Risk_Based_Lot_EA.mq5`  
  EMA strategy using risk-based lot sizing.

## Recommended workflow

1. Open MetaEditor in MetaTrader 5.
2. Create a new Expert Advisor project.
3. Paste the EA code into the main `.mq5` file.
4. Compile the file.
5. Attach it to a chart in MetaTrader 5.
6. Test the EA in Strategy Tester or run it on a demo account.

## Suggested setup

- Symbol: major forex pair or liquid market
- Timeframe: M5, M15, or H1 for testing
- Account type: demo account for initial validation
- Spread and slippage: account for realistic execution

## Important notes

- Do not use the EA blindly on a live account.
- Always optimize and test under realistic conditions.
- Consider broker spread, execution speed, and slippage before using in production.
- The code is intentionally simple and educational, meant to serve as a base strategy template.

## Installation and download

You can download this repository as a ZIP archive from GitHub:

- https://github.com/ntisoza21/EMA-Trading-EA

Then:

1. Click `Code`
2. Select `Download ZIP`
3. Extract the files
4. Open the `.mq5` files in MetaEditor

## Example EA logic summary

The core logic typically does this:

- Checks EMA alignment (fast > mid > slow > trend for long entries)
- Uses the opposite alignment for short entries
- Uses RSI as a confirmation filter when enabled
- Closes profitable positions when target is reached
- Reopens a new order if the market still meets the signal
- Optionally closes only part of a position to lock profits
- Calculates the lot size from account balance and risk percentage

## Disclaimer

Trading involves financial risk. This project is for research, learning, and strategy testing only. There are no guarantees of profit, and past performance does not imply future results.

## License

This repository is provided as-is for educational and research use.

## Contact

This repo is maintained under the GitHub account:

- ntisoza21
