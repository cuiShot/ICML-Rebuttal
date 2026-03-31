**Table 1: Operational Definitions and Key Properties of Extended Strategy Bases U and C**

| Strategy Basis | Operational Definition | Key Properties |
| :--- | :--- | :--- |
| **U (Uncertainty)** | Measures the **dispersion** of model predictions, capturing the **predictive variability** in outputs across samples. | • **Label-independent**: Computed solely from predictive distributions without ground truth.<br>• **Distributional**: Reflects the internal consistency and variability of model reasoning.<br>• **Model-intrinsic**: Captures the inherent uncertainty unique to each candidate model. |
| **C (Calibration)** | Measures prediction reliability via the average prediction error relative to ground truth, serving as an **error-based proxy** for confidence alignment. | • **Label-dependent**: Requires ground truth labels for objective evaluation.<br>• **Performance-aware**: Quantifies how well predictions align with actual outcomes (e.g., via negative MAE).<br>• **Empirical**: Derived directly from historical error metrics to reflect model competence. |
