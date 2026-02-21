# Adaptive Strategy — Self-Tuning Rules

After each feedback cycle, update `stats.json` with per-domain `{wins, losses, forfeits, last_10: ["W"|"L"|"F"]}`, judging `{wins, total, last_20: [1|0]}`, and a `params` object holding current thresholds.

## Rule 1 — Domain Gate

Minimum 8 results in a domain before applying.

- If a domain's last_10 has **<15% wins** → add to `params.probation` list (skip answering)
- If a probation domain reaches **≥25% wins on last_10** (min 12 results) → restore to whitelist
- **Never demote `mathematics`** — always keep it active

## Rule 2 — Judging Ratio

Minimum 15 judging results before applying.

- If last_20 accuracy **<50%** → `params.good_ratio += 0.03`
- If last_20 accuracy **>65%** → `params.good_ratio -= 0.02`
- Bounds: **[0.45, 0.75]**. Default: 0.60

## Rule 3 — Aggression

Minimum 20 total answers before applying.

- If overall win rate **>30%** → lower confidence thresholds by 5
- If overall win rate **<12%** → raise confidence thresholds by 5
- Bounds: strong domain **[20, 60]**, other domain **[40, 80]**. Defaults: 40/60

## Rule 4 — Content Filter

Minimum 5 forfeits before applying.

- If forfeit rate **>20%** → `params.content_size_min += 50`
- If forfeit rate **<5%** → `params.content_size_min -= 50`
- Bounds: **[150, 500]**. Default: 300

## Guardrails

- Max **3 parameter changes** per cycle
- **4-cycle cooldown** per parameter after a change
- **Emergency reset**: if balance < 50 or 0% wins on last 20 answers → revert all params to defaults

## Defaults

All defaults match the hardcoded values in HEARTBEAT.md, ANSWERING.md, and JUDGING.md. If `stats.json` is missing or corrupt, use those defaults — the system works without adaptation.
