# Python Algo Trading Strategy: 472% Return (Flow Effects)

**Source:** https://x.com/quantscience_/status/1881390825067725076
**Author:** @quantscience_ (Quant Science)
**Saved:** 2025-01-25

## Strategy Overview

This strategy takes advantage of **"flow effects"** - how certain points in time influence the value of an asset.

Uses a simple temporal shift to determine when trades should exit relative to their entry for monthly boundary conditions.

## The Core Concept

The signals for when to go short, when to cover shorts, when to go long, and when to close longs are all linked to recurring monthly cycles.

This periodic "flow" of signals—month-in, month-out—creates a systematic pattern.

## Implementation (Python)

### 1. Load Libraries and Data

```python
# Import required libraries
# Ingest price data on TLT (Treasury Bond ETF)
```

### 2. Generate Signals

Set up an empty data frame to track the long/short signals.

**Short Entry Signals:**
- Each new month's 1st day
- Each new month's 5th day

**Long Entry Signals:**
- 7 days before end of each month
- 1 day before end of each month

### 3. Run Trade PnL

Use `vbt.Portfolio.from_signals()` to calculate performance.

Use `pf.stats()` to return the portfolio stats summary tear sheet.

## Results

- **Total Return:** 472%
- Uses VectorBT for backtesting
- Applied to TLT (Treasury Bond ETF)

## Key Takeaways

1. Simple calendar-based signals can be powerful
2. Monthly flow effects exist in bonds
3. VectorBT is great for quick backtesting
4. Strategy exploits end-of-month rebalancing flows

## Caution

- Note: Stats showed "Worst Trade 1000%" which needs investigation
- Always validate with out-of-sample data
- Past performance doesn't guarantee future results

## Resources

- Full thread: https://x.com/quantscience_/status/1881390825067725076
- ThreadReader unroll available

## Tags
#python #algorithmic-trading #strategy #backtesting #vectorbt #flow-effects #bonds #tlt
