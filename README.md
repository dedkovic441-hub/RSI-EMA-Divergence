# RSI-EMA-Divergence

A standalone browser dashboard for Binance USDⓈ-M Futures public market data.

## Strategy
- RSI (14), EMA 9 and EMA 21.
- Bullish divergence: price lower low while RSI forms a higher low.
- Bearish divergence: price higher high while RSI forms a lower high.
- Entry marker requires the corresponding EMA 9/21 crossover.
- Signals are evaluated using completed candles only.

## Run
Open `index.html` in a modern browser, or enable GitHub Pages for the repository (Settings → Pages → Deploy from a branch → main / root).

## Data and safety
Uses Binance public REST klines and public mark-price WebSocket. No API keys, account access, order placement, or live trading. Historical signal markers are not a fee-adjusted backtest or a guarantee of future results.

## Current limitations
- Pivot divergence requires three candles on each side of a pivot, so it is deliberately delayed.
- The initial release loads up to 500 recent candles and does not fetch older history.
- Backtest panel reports detected signals only; trade simulation, fees, slippage, position sizing, and performance metrics are not implemented yet.
