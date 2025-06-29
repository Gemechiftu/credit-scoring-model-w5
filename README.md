# credit-scoring-model-w5
Credit Scoring Business Understanding
1. Basel II Accord and Model Interpretability
The Basel II Accord emphasizes risk-sensitive capital requirements, encouraging financial institutions to measure and manage credit risk more precisely. This creates a strong business and regulatory need for interpretable, transparent, and well-documented models. Regulators and internal auditors must understand how credit decisions are made, especially when models affect loan approvals, capital allocation, or reserve buffers. Thus, while performance is important, model interpretability and auditability are essential for compliance, trust, and fairness.

2. Proxy Variables and Business Risk
In many credit datasets, especially from external sources like eCommerce platforms, we lack a direct label indicating whether a customer defaulted on credit payments. As a result, we must define a proxy variable (e.g., delayed payments, high refund rate, or basket abandonment) to approximate credit default behavior.

While this helps build a working model, using proxies introduces potential business risks:

Label noise: The proxy may not perfectly represent actual defaults, leading to misclassifications.

Bias: Systematic errors in the proxy could unfairly disadvantage certain customer segments.

Regulatory scrutiny: If the proxy is too weakly related to true risk, decisions may not hold up to audits.

Hence, careful selection and validation of the proxy is critical to ensure sound, ethical predictions.

3. Interpretable vs. Complex Models: Trade-offs
Model Type	Pros	Cons
Logistic Regression + WoE	✅ High interpretability
✅ Easy to audit
✅ Simple to explain to stakeholders	❌ May underperform with complex data patterns
Gradient Boosting (e.g. XGBoost)	✅ High predictive performance
✅ Captures nonlinear relationships	❌ Difficult to interpret
❌ Harder to justify regulatory decisions

In regulated financial environments, simplicity and interpretability often outweigh small gains in accuracy. While complex models can improve performance, they increase the risk of model opacity, bias, and non-compliance. Many institutions start with interpretable models, then gradually layer complexity with caution, often using hybrid approaches like explainable AI (XAI) tools (e.g., SHAP) to interpret black-box models.
