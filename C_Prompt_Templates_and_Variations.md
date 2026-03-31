Table 1: Design summary of the four prompt variations used for robustness evaluation.

| Prompt Variant | Design Method (Specific Construction) |
| :--- | :--- |
| **`simplified`** | Appends "keep it simple and practical" instructions; removes redundant task constraint descriptions. |
| **`detailed`** | Injects strict execution constraints (e.g., API specifications, output type-safety, and reproducibility). |
| **`no_examples`** | Explicitly requires the model to infer solely from task requirements; removes all few-shot examples and templates. |
| **`improved`** | Incorporates machine learning engineering best practices (e.g., balancing AUC, runtime cost, and overfitting risks). |
