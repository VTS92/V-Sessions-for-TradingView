# V-Sessions — Multi-Session Volume Mapping Engine

**Pine Script v6 | TradingView | Public Release 2026 — Open Source**

Multi-session analysis engine covering London, New York, NYSE, overnight US, Tokyo, TSE, Sydney and custom sessions, with session-specific volume profiles, POC/LVN analysis and anchored VWAP functionality.

Built and used daily in live trading. Part of the V-Suite — works best combined with the [V-Profile Matrix](https://github.com/VTS92/V-Profile-Matrix-for-TradingView) and the [V-Cumulative Delta](https://github.com/VTS92/V-Cumulative-Delta-for-TradingView).

---

## What it does

V-Sessions maps up to 8 configurable global trading sessions (London, New York, NYSE RTH, New York overnight/ETH, Tokyo, TSE RTH, Sydney and one fully custom session) directly on the chart, so you can see at a glance which region drove the current price action.

For each active session, the engine independently tracks:

- **Session Box** — a bounded visual range marking the session's high/low and duration on the chart
- **Session POC** — the price level with the highest traded volume within that specific session
- **Session LVN Zones** — low-liquidity price gaps formed during the session, flagged as likely fast-move areas, with automatic mitigation tracking once price revisits them
- **Anchored VWAP & Deviation Bands** — optional VWAP with up to 3 configurable standard-deviation bands, calculated independently of the session boxes
- **Day-of-week labelling** — automatically tags the start of each new trading day on intraday charts

Because every session is tracked as an independent state, the indicator can display multiple overlapping or sequential sessions on the same chart without mixing their data — useful for comparing how the Tokyo session's value area behaves against the following London session, for example.

---

## Screenshots
![V-Sessions Detail](Screenshot_1.png)
![V-Sessions Overview](Screenshot_2.png) 

---

## Source Code

The full Pine Script v6 source is included in this repository: [`V-Sessions.pine`](V-Sessions.pine). Licensed under [MIT](LICENSE) — free to use, modify and redistribute.

---

## How to use

1. Open TradingView and go to **Pine Editor**
2. Paste the contents of `V-Sessions.pine`
3. Click **Add to chart**
4. Enable/disable individual sessions and configure their time windows under **Session Configuration**
5. Toggle POC, LVN, VWAP and Bands from the **Session Tools & Configurations** group

---

## Part of the V-Suite

- **[V-Profile Matrix](https://github.com/VTS92/V-Profile-Matrix-for-TradingView)** — session-anchored volume profile with ATR-filtered Fair Value Gap detection and Power Score
- **[V-Cumulative Delta](https://github.com/VTS92/V-Cumulative-Delta-for-TradingView)** — cumulative volume delta with order-flow regime detection and VWAP divergence
- **[V-Profile Delta Range](https://github.com/VTS92/V-Profile-Delta-Range-for-TradingView)** — rolling delta profile with institutional Z-score cluster detection

**How they fit together:** V-Sessions tells you *when* each market was active and how volume was distributed within it. V-Profile Matrix tells you *where* volume is concentrated and rates the strength of each imbalance. V-Cumulative Delta tells you *who* is in control of the order flow right now.

---

## Author

**Vito Santarsiero** — Trading Platform Operations Specialist | CISI IOC Candidate | London, UK

[LinkedIn](https://linkedin.com/in/vito-santarsiero) · [V-Profile Matrix](https://github.com/VTS92/V-Profile-Matrix-for-TradingView) · [V-Cumulative Delta](https://github.com/VTS92/V-Cumulative-Delta-for-TradingView)

## License

MIT — see [LICENSE](LICENSE).
