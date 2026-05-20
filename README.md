# Stabilizing-Preference-Optimization-in-LLMs
Gradient-Gated DPO: Stabilizing Preference Optimization in Language Models

## Summary

### Problems
- Direct Preference Optimization (DPO) suffers from a "squeezing effect."
- Rejected-response gradients concentrate probability mass on high-confidence predictions and suppress alternative outputs.
- This pathology appears even in simple softmax models.
- It can cause systematic probability collapse during training.

### Contributions
- Introduces Gradient-Gated Preference Optimization (`Gate-DPO`).
- Stabilizes training by modulating rejected gradients based on the model’s probability geometry.
- Attenuates harmful updates when rejected responses target extremely low-probability outputs.
- Preserves standard preference optimization behavior for normal updates.
- Works without changing the underlying preference objective.
- Is complementary to existing methods such as extended SFT, IPO, and Cal-DPO.
- Empirically reduces squeezing and improves chosen-response likelihood across architectures and datasets.
- Mass-dynamics analysis reveals healthier optimization behavior, with better preferred responses and reduced suppression of the overall distribution.
- Shows that smaller gated models can outperform larger ungated models on chosen-response improvements.

> See the arXiv preprint version: https://arxiv.org/html/2605.02626v1
- Code will be made available for reproducibility.
