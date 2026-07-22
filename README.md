## Reproducibility: Full Implementation Configurations

### Common settings (all experiments)

- Optimizer: Adam, learning rate = 1e-4, weight decay = 1e-4  <!-- 请确认优化器 -->
- Random seed(s): **[FILL IN, e.g., 1 / {1, 42, 2026}]**
- Threshold update schedule: after the warm-up stage, the upper threshold is
  linearly annealed from its initial value τ_up toward 0.5 with a per-epoch step
  η₁ = (τ_up − 0.5) / N₁, and the lower threshold is linearly annealed from
  τ_low toward 0.5 with step η₂ = (0.5 − τ_low) / N₂, where N₁ / N₂ are the
  threshold-update epochs listed below.
- Fuzzy-mean (soft-label mean) constraint: margin = 0.5, regularization
  coefficient = 0.1.
- ASL parameters are reported as (γ⁻, γ⁺, γ_clip, s); γ⁻ is the negative
  focusing parameter.  <!-- 请按你代码里的实际含义核对后两个数 -->

### PASCAL VOC

| Noise rate | Warm-up (epochs) | Init τ_up | Init τ_low | Threshold update epochs (N₁ / N₂) | ASL (γ⁻, γ⁺, γ_clip, s) | Fuzzy-mean margin | Total epochs |
|---|---|---|---|---|---|---|---|
| 0.1 | TBD | TBD | TBD | TBD | TBD | 0.5 | TBD |
| 0.2 | 5 | 0.9 | 0.0 | 60 / 60 | (5, 2, 1, 30) | 0.5 | 60 |
| 0.4 | 5 | 0.9 | 0.0 | 60 / 60 | (4, 1, 1, 20) | 0.5 | 80 (best at 60) |
| 0.6 | TBD | TBD | TBD | TBD | TBD | 0.5 | TBD |
| 0.8 | 5 | 0.95 | 0.0 | 60 / 60 | (2, 1, 1, 20) | 0.5 | 80 (best at 60) |

### MS-COCO

| Noise rate | Warm-up (epochs) | Init τ_up | Init τ_low | Threshold update epochs (N₁ / N₂) | ASL (γ⁻, γ⁺, γ_clip, s) | Fuzzy-mean margin | Total epochs |
|---|---|---|---|---|---|---|---|
| 0.1 | TBD | TBD | TBD | TBD | TBD | 0.5 | TBD |
| 0.2 | 30 (stop epoch) | 0.8 | 0.05 | 40 / 35 | (5, 2, 1.5) | 0.5 or 0.7 | 80 |
| 0.4 | 9 | 0.8 | 0.0 | 30 / 30 | (4, 1, 1, 20) | 0.5 | 60 |
| 0.6 | 8 | 0.8 | 0.0 | 30 / 30 | (3, 1, 1, 20) | 0.5 | 60 |
| 0.8 | 8 | 0.85 | 0.0 | 30 / 30 | (2, 1, 1, 20) | 0.5 | 60 |

### NUS-WIDE

| Noise rate | Warm-up (epochs) | Init τ_up | Init τ_low | Threshold update epochs (N₁ / N₂) | ASL (γ⁻, γ⁺, γ_clip, s) | Fuzzy-mean margin | Total epochs |
|---|---|---|---|---|---|---|---|
| 0.1 | TBD | TBD | TBD | TBD | TBD | 0.5 | TBD |
| 0.2 | 9 | 0.8 | 0.0 | 35 / 35 | (5, 2, 1.5, 30) | 0.5 | 60 |
| 0.4 | 9 | 0.8 | 0.0 | 30 / 30 | (4.5, 1, 1, 30) | 0.5 | 60 |
| 0.6 | 8 | 0.8 | 0.0 | 30 / 30 | (3, 1, 1, 20) | 0.5 | 60 |
| 0.8 | 8 | 0.85 | 0.0 | 30 / 30 | (2, 1, 1, 20) | 0.5 | 60 |
