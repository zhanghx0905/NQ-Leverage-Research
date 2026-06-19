# Data Directory

Use `final/` for current analysis outputs.

Key files:

- `final/nq1_integrated_badj_nonbadj_closed_only.csv`: combined TradingView NQ1 data. B-ADJ columns are used for continuous point PnL; non-B-ADJ columns are used for actual price and notional.
- `final/tqqq_mnq_badj_daily_model.csv`: audit table used in the final TQQQ vs MNQ path analysis.
- `final/tqqq_mnq_badj_nav_paths.csv`: final normalized NAV paths.
- `final/tqqq_mnq_badj_summary.csv`: final summary statistics.
- `final/tqqq_mnq_badj_yearly_returns.csv`: final calendar-year returns.
- `final/tqqq_mnq_rebalance_summary_70pct_bil.csv`: daily/weekly/monthly rebalance comparison with 70% BIL cash sleeve.
- `final/tqqq_mnq_rebalance_summary_no_cash.csv`: daily/weekly/monthly rebalance comparison without cash yield.
- `final/tqqq_mnq_rebalance_nav_paths.csv`: NAV paths for TQQQ and MNQ rebalance rules.
- `final/tqqq_mnq_rebalance_detail_70pct_bil.csv`: rebalance-day flags, fractional MNQ contracts, and leverage drift detail.

Old Yahoo/Investing/main-continuous simulation artifacts were removed. The remaining files are the current B-ADJ based analysis inputs and outputs.
