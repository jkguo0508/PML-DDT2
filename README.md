## Reproducibility: Full Implementation Configurations

The thresholds follow the **linear schedule** of Eqs. (12)–(13): starting from $(\tau_{\text{upper}}^{\text{init}}, \tau_{\text{lower}}^{\text{init}})$, they are updated every epoch by a fixed step until epoch $T_{\text{max}}$, reaching $(\tau_{\text{upper}}^{\text{final}}, \tau_{\text{lower}}^{\text{final}})$.



### PASCAL VOC


| Noise rate | $\tau_{\text{upper}}^{\text{init}}$ | $\tau_{\text{lower}}^{\text{init}}$ | Threshold update epochs | ASL ($\gamma^-$) |
| :---: | :---: | :---: | :---: | :---: |
| 0.1 | 0.9 | 0.0 | 60 | 5
| 0.2 | 0.9 | 0.0 | 60 | 5
| 0.4 | 0.9 | 0.0 | 60 | 4
| 0.6 | 0.9 | 0.0 | 60 | 3
| 0.8 | 0.95 | 0.0 | 60 | 2

### MS-COCO

| Noise rate | $\tau_{\text{upper}}^{\text{init}}$ | $\tau_{\text{lower}}^{\text{init}}$ | Threshold update epochs | ASL ($\gamma^-$) |
| :---: | :---: | :---: | :---: | :---: |
| 0.1 | 0.8 | 0.0 | 30 | 5
| 0.2 | 0.8 | 0.0 | 30 | 5
| 0.4 | 0.8 | 0.0 | 30 | 4
| 0.6 | 0.8 | 0.0 | 30 | 3
| 0.8 | 0.85 | 0.0 | 30 | 2

### NUS-WIDE


| Noise rate | $\tau_{\text{upper}}^{\text{init}}$ | $\tau_{\text{lower}}^{\text{init}}$ | Threshold update epochs | ASL ($\gamma^-$) |
| :---: | :---: | :---: | :---: | :---: |
| 0.1 | 0.8 | 0.0 | 30 | 5
| 0.2 | 0.8 | 0.0 | 30 | 5
| 0.4 | 0.8 | 0.0 | 30 | 4
| 0.6 | 0.8 | 0.0 | 30 | 3
| 0.8 | 0.85 | 0.0 | 30 | 2
