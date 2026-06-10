# Privacy & data provenance

**This repository contains synthetic data only.**

Every number produced by this prototype is generated from a parametric model
with hand-chosen, illustrative defaults (`MarketParams` in
`courier_elasticity.py`, `CohortParams` in `cohort_decay.py`). There is no real
courier data, no merchant data, no Uber data, and no data from any other company
anywhere in this repo or its outputs.

## What is *not* here

- No proprietary datasets, exports, or query results from any employer or client.
- No personally identifiable information (PII) of any kind — no courier names,
  merchant names, account IDs, locations, or earnings.
- No internal metric definitions, thresholds, or model parameters from any real
  marketplace.
- No secrets, credentials, API keys, or tokens.

## What the model *is*

The curve **shapes** are grounded in patterns Jeff observed publicly describing
his own 2019 Uber product-analyst take-home (a $5/hr peak-window incentive with
Cochran sample-sizing and a free-rider tracking metric) and the qualitative
cohort-decay pattern in the driver-signup-to-first-trip exercise. The *shapes*
are real; the *numbers* are invented to make those shapes legible.

To use this against your own marketplace, you fit `baseline_util`, `max_util`,
and `half_saturation` to your courier-acceptance logs and set `fleet_size` to
your active-courier count — all of which stays on your side. This repo is the
method, not the data.

See the source note for the grounding:
<https://jeffpinto.com/notes/uber-market-launch/>
