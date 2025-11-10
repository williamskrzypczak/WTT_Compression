# WaveRider WTT Compression – Quick Reference

© 2025 Bulldog Ventures Inc. All rights reserved.

## Overview
- Highlights breakout momentum following doji candles.
- Uses orange triangles for bullish breakouts and purple triangles for bearish breakouts.
- Includes optional per-bar alerts with dynamic ticker and price context.

## Default Settings
- Doji body threshold: 30% of candle range.
- Require close breakout: enabled.
- Breakout markers: tiny triangles.
- Alerts: enabled.

## Key Inputs
- `Doji Body Threshold`: Sensitivity for qualifying doji candles (0.0 – 0.5).
- `Require Close Breakout`: Require closing price to exceed the doji high/low.
- `Enable Alerts`: Toggle automatic alert firing.
- `Uptrend Color` / `Downtrend Color`: Customize breakout marker colors.

## Signal Logic
1. Detects doji when candle body ≤ threshold × range.
2. Waits one bar; confirms prior bar was doji.
3. Flags breakout when price closes (or trades, per setting) beyond doji range.
4. Plots triangles and emits alerts when enabled.

## Alert Messages
- Bullish: `"WaveRider WTT Compression: Bullish doji breakout on <ticker> at <price>"`
- Bearish: `"WaveRider WTT Compression: Bearish doji breakout on <ticker> at <price>"`

## Tips
- Lower the threshold for stricter doji detection; raise it to capture more setups.
- Disable `Require Close Breakout` for faster but more aggressive signals.
- Use TradingView’s `Once Per Bar` alert frequency to match the script’s behavior.

