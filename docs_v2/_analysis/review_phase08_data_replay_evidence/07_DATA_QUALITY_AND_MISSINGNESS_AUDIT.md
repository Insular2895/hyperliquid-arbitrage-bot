# Data Quality and Missingness Audit

RAW is immutable. Re-normalization creates a new schema/dataset version. Drops/gaps remain explicit and cannot become zero, healthy or N/A. Unknown payload may be retained for future normalization. Actual, Replay, Counterfactual, Shadow, Simulated, MicroLive actual and Live actual provenance stays separate. No lookahead applies even when files are preloaded.
