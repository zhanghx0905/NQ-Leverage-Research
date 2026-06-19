# Data Directory

The data folder is split by file role:

- `input/`: canonical source inputs used by the analysis scripts.
- `interim/`: reproducible audit tables produced from inputs and reused by downstream scripts.
- `output/`: final CSV and JSON outputs produced by the reports.

## Input Files

- `input/nq1_continuous_badj_nonbadj.csv`
  - Cleaned TradingView NQ1 continuous futures input.
  - Contains only `date`, B-ADJ OHLC, and non-B-ADJ OHLC.
  - B-ADJ close deltas are used for continuous futures point PnL.
  - Non-B-ADJ close is used for actual NQ price, notional exposure, and leverage sizing.
- `input/nq1_continuous_badj_nonbadj_notes.json`
  - Cleaning notes for the NQ input, including removed derived columns and provenance counts.
- `input/raw_TQQQ.csv`
  - TQQQ adjusted-close history.
- `input/raw_BIL.csv`
  - BIL adjusted-close history, used as the short-bill cash-yield proxy.

## Interim Files

- `interim/tqqq_mnq_badj_daily_model.csv`
  - Audit table produced by `final_tqqq_mnq_badj_analysis.py`.
  - Used by `final_rebalance_badj_analysis.py`.

## Output Files

- `output/tqqq_mnq_badj_nav_paths.csv`
- `output/tqqq_mnq_badj_daily_returns.csv`
- `output/tqqq_mnq_badj_summary.csv`
- `output/tqqq_mnq_badj_yearly_returns.csv`
- `output/tqqq_mnq_badj_source_notes.json`
- `output/tqqq_mnq_rebalance_nav_paths.csv`
- `output/tqqq_mnq_rebalance_nav_paths_no_cash.csv`
- `output/tqqq_mnq_rebalance_detail_70pct_bil.csv`
- `output/tqqq_mnq_rebalance_summary_70pct_bil.csv`
- `output/tqqq_mnq_rebalance_summary_no_cash.csv`
- `output/tqqq_mnq_rebalance_source_notes.json`

Old Yahoo `NQ=F`, Investing raw main-continuous, and unadjusted front-contract simulation artifacts should not be reintroduced for long-horizon MNQ return simulation.
