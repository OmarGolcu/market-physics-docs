# Feature library documentation

Documentation for three Python libraries that turn OHLCV data into descriptive features:

| library | version | what it covers | page |
|---|---|---|---|
| **market_physics** | 0.1.3 | 147 physics-inspired estimators in 16 families + `energy` (mechanics, gravitation, electromagnetism, thermodynamics, information theory, chaos, fractals, random matrix theory) | [market_physics.html](https://omargolcu.github.io/market-physics-docs/market_physics.html) |
| **ta_classic** | 0.1.0 | 14 classic technical-analysis indicators under a hard contract (causal, measured tail-slice reach, deterministic flat-market answers) + the `reach` module | [ta_classic.html](https://omargolcu.github.io/market-physics-docs/ta_classic.html) |
| **price_action** | 0.3.0 | 38 non-repainting structural detectors — candles, two swing engines, market structure, FVG / order-block zones with a mitigation life-cycle, breakers, liquidity, patterns, levels, trendlines | [price_action.html](https://omargolcu.github.io/market-physics-docs/price_action.html) |

**Read the docs:** https://omargolcu.github.io/market-physics-docs/ (overview of all three, their shared contract, and how each function maps to the Black Hole indicator registry)

Every page follows one template: a physics / TA / price-action essay per family, then one article per function with its
signature, parameter table, returns, raises, a runnable example and a chart. Signatures, parameter tables and docstring
text are extracted directly from the source; charts and example values are produced by running the libraries on
deterministic synthetic data (not market data). Source: `the-market-physics` monorepo @ `37730ca`.

Changes since the previous (2026-07) page, which documented market_physics alone:

- market_physics: `momentum_energy` is now documented and counted (147 indicators); no function removed, no signature changed.
- price_action: now part of this site (previously a separate v0.1.0 page with 29 functions); 38 functions at 0.3.0,
  including the zigzag swing engine, FVG / order-block zone tables, mitigation events, breaker blocks, equal highs/lows,
  premium/discount and OTE. `detect_support_resistance` gained `tolerance_mode` / `atr_window` and `detect_trendlines`
  gained `method` / `touch_tolerance`.
- ta_classic: documented for the first time.
- Each article ends with an "In Black Hole" line generated from the registry (keys, category, `min_bars`, `output_range`,
  `unbounded_history`, `zero_snap`, variants), or the reason the function is not registered.

All outputs are descriptive features, **not trading signals**.
