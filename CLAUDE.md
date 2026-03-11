- Add the least code possible to address a request. 
- Avoid code complexity and bloat at every opportunity. 
- Before making significant code changes, ask clarifying questions.
- Make documentation as succinct as possible. Avoid adding code blocks: just link to the relevant file instead.

P.8. Forward Volatility from the SOFR Cap Market
Strip forward volatilities from the SOFR cap market over 2022–2025 and test whether the forward vol curve predicts future realized rate volatility — a Fama–Bliss analog for the volatility term structure. The cap stripping exercise from homework covers a single date; this project extends that to a daily time series spanning the full Fed policy cycle (aggressive hiking, pause, easing). You will build a forward vol panel across tenors, run predictive regressions of realized vol on lagged forward vol, characterize the resulting volatility term premium, and assess whether it can be harvested through a systematic carry strategy. The project pays particular attention to the distinction between normal and Black vol conventions, overlapping-observation issues in regression inference, and regime dependence of the vol premium.

Data provided: Daily SOFR cap flat vols for multiple maturities (2022–2025); SOFR swap rates; daily SOFR rate for realized vol computation; a processed validation file for cross-checking the bootstrap.

Methods: Forward vol bootstrap from flat cap vols, predictive regressions (Fama–Bliss style), volatility term premium estimation, split-sample stability tests, carry strategy design with regime analysis.