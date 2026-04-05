# TurboQuant Visualized

Visual walkthrough of [TurboQuant: Online Vector Quantization with Near-optimal Distortion Rate](https://arxiv.org/abs/2504.19874)

## Run

```bash
pip install numpy matplotlib scipy
python 01_rotation_trick.py
python 02_scalar_quantization.py
python 03_mse_bias_problem.py
python 04_two_stage_fix.py
python 05_distortion_vs_lower_bound.py
python 06_kv_cache_explainer.py
```

## The story in 6 plots

| Script | What it shows |
|---|---|
| `01_rotation_trick.py` | Random rotation makes any vector's coordinates Gaussian and independent |
| `02_scalar_quantization.py` | How 1D k-means (Lloyd-Max) quantizes each coordinate |
| `03_mse_bias_problem.py` | MSE-optimal quantizers are BIASED for inner products |
| `04_two_stage_fix.py` | The fix: (b-1) bits MSE + 1 bit QJL on residual → unbiased |
| `05_distortion_vs_lower_bound.py` | TurboQuant is within ~2.7x of the information-theoretic limit |
| `06_kv_cache_explainer.py` | Why this matters: KV cache memory in transformers |
