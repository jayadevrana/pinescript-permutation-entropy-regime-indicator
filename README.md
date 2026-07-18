# Pinescript Permutation Entropy Regime Indicator

Pine Script v6 indicator that classifies market regime using Bandt-Pompe permutation entropy: adaptive Structure Rank, drift bias, five regimes, bar coloring and dashboard.

## Features

- Computes permutation entropy (Bandt-Pompe ordinal patterns, embedding dimension 3, delay 1) over a configurable window of recent closes to measure how ordered vs. random-walk price action is.
- Converts entropy into a Predictability score, then percentile-ranks it into an adaptive **Structure Rank** so the regime cutoffs self-tune per instrument and timeframe.
- Adds a **drift-bias** term (net share of up vs. down closes) to split structured regimes into directional Up, Down, or Range.
- Classifies price into five regimes: Structured Up, Structured Down, Structured Range, Neutral, and Random / Chop.
- Optional regime-colored price bars and pane background shading for instant visual context.
- On-chart dashboard reporting Regime, Structure Rank, Predictability, normalized entropy, drift bias, bars-in-regime, and window/dimension.
- Five built-in `alertcondition`s for regime entries and regime changes, evaluated on confirmed bars only.
- Fully user-configurable window, smoothing, rank lookback, structured/chop levels, drift threshold, colors, and dashboard position.

## Stack

- Pine Script v6 (TradingView) — single indicator script (`permutation_entropy_regime.pine`).

## Getting started

1. Open the [TradingView](https://www.tradingview.com/) Pine Editor.
2. Create a new indicator and paste the contents of `permutation_entropy_regime.pine`.
3. Click **Add to chart**. The indicator plots in a separate pane with the Structure Rank line, level guides, dashboard, and optional bar coloring.
4. Tune the inputs (Entropy Window, Structured/Chop levels, Drift Bias Threshold) to suit your market and timeframe, and wire up alerts from the built-in alert conditions if desired.

## Notes

Trading automation is infrastructure, not financial advice. No profit guarantees. Test in dry-run/paper before live.

## Author

Built by [Jayadev Rana](https://jayadevrana.in) — @bluealgocapital · [YouTube](https://www.youtube.com/@jayadevrana3657) · [GitHub](https://github.com/jayadevrana)
