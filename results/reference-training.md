# Training data from prior studies

Each column compares methods using a training pool drawn from a public reference dataset. Evaluation uses the same external materials as the shared-training comparison. The tables reflect the configurations evaluated in this study. The Sol row reports the ICL setting evaluated for each data source. ★ marks the lowest RMSE among the evaluated peer baselines in the corresponding column.

Values are RMSE in the units shown. Scores are displayed as mean ± standard deviation where available. **Bold** indicates the lowest reported RMSE in each column within this table. A dash denotes an unavailable result or a comparison outside the scope of that model. Sample counts appear below each endpoint. n is the number of evaluation records and m is the number of distinct materials.

## Polymers

| Model | Glass transition (K)<br>n=59, m=58 | Melting temperature (K)<br>n=6, m=4 | Experimental density (g/cm³)<br>n=15, m=15 | Experimental refractive index<br>n=13, m=13 |
| --- | ---: | ---: | ---: | ---: |
| Sol (ICL) | 29.95 ± 2.39 | 56.43 ± 2.08 | **0.1664 ± 0.0287** | **0.03384 ± 0.00237** |
| GPT-6 Luna (full-context ICL) | 39.05 ± 2.33 | 61.18 ± 3.23 | 0.4398 ± 0.0207 | 0.04694 ± 0.00902 |
| DeepSeek V4 Pro (full-context ICL) | 44.07 ± 5.25 | 70.08 ± 24.3 | 0.175 ± 0.0435 | 0.07285 ± 0.00956 |
| GPT-5.2 (full-context ICL) | 41.78 ± 2.56 | 55.26 ± 12.2 | 0.1835 ± 0.0157 | 0.0556 ± 0.0128 |
| GPT-4.1 (full-context ICL) | 57.37 ± 11.4 | **43.17 ± 13.9** | 0.272 ± 0.0678 | 0.09211 ± 0.0109 |
| Random forest (PolyBench26) | 37.36 ± 2.98 | — | — | — |
| Chemprop (PolyBench26) | **27.32 ± 2.52** ★ | — | — | — |
| PolyGraphMT | — | 83.2 ± 8.98 ★ | 0.4475 ± 0.0356 ★ | — |
| Ridge (RefractiveIndexGPT) | — | — | — | 0.143 ± 0.0209 ★ |

## Inorganic crystals

| Model | PBE band gap (eV)<br>n=9, m=9 | Bulk modulus (GPa)<br>n=7, m=7 | Shear modulus (GPa)<br>n=7, m=7 |
| --- | ---: | ---: | ---: |
| Sol (ICL) | **0.2207 ± 0.0413** | 177.6 ± 32.5 | 87.55 ± 5.58 |
| GPT-6 Luna (full-context ICL) | 1.905 ± 0.398 | 20.03 ± 5.7 | 18.79 ± 3.83 |
| DeepSeek V4 Pro (full-context ICL) | 1.55 ± 0.808 | 17.32 ± 1.05 | 19.25 ± 4.31 |
| GPT-5.2 (full-context ICL) | — | 25.38 ± 1.19 | 21.57 ± 2.43 |
| GPT-4.1 (full-context ICL) | — | **17.16 ± 2.55** | 17.77 ± 4.82 |
| MODNet | — | 19.39 ± 4.08 ★ | **16.94 ± 2.58** ★ |
| XGBoost (band-gap reference) | 1.028 ± 0.0837 ★ | — | — |

## Alloys

| Model | Yield strength (MPa)<br>n=137, m=39 | Ultimate tensile strength (MPa)<br>n=140, m=40 | Elongation (percentage points)<br>n=29, m=21 | Vickers hardness (HV)<br>n=41, m=24 |
| --- | ---: | ---: | ---: | ---: |
| Sol (ICL) | **312.2 ± 4.77** | **375.5 ± 8.47** | **10.62 ± 0.376** | 184 ± 1.04 |
| GPT-6 Luna (full-context ICL) | 367.5 ± 17.6 | 634.9 ± 54.3 | 12.64 ± 1.81 | 183.1 ± 11 |
| DeepSeek V4 Pro (full-context ICL) | 365.5 ± 18.3 | 420 ± 21.4 | 13.04 ± 0.446 | 153 ± 16.2 |
| GPT-5.2 (full-context ICL) | 350.1 ± 14.3 | 436.8 ± 12.1 | 12.29 ± 0.797 | **148.9 ± 17.6** |
| GPT-4.1 (full-context ICL) | 380.6 ± 20.1 | 740.6 ± 11.3 | 12.65 ± 3.13 | 274.1 ± 82.5 |
| MODNet | 821.6 ± 107 ★ | — | — | — |
| XGBoost (alloy reference) | — | 502 ± 37.7 ★ | 24.47 ± 0.164 ★ | — |
| GBDT (hardness reference) | — | — | — | 207.4 ± 5.91 ★ |

## Public training-data references

| Endpoints | Reference |
| --- | --- |
| Glass transition | [Polymer Benchmark 2026](https://github.com/rlearsch/PolymerBenchmark2026) |
| Melting temperature and experimental density | [PolyGraphMT](https://github.com/sobinalosious/PolyGraphMT) |
| Experimental refractive index | [RefractiveIndexGPT](https://github.com/KanHatakeyama/RefractiveIndexGPT) |
| PBE band gap, elastic moduli and yield strength | [Matbench](https://github.com/materialsproject/matbench) · [MP Gap reference](https://github.com/samuel-cmd79/matbench-mp-gap-representation-audit) |
| Ultimate tensile strength and elongation | [Alloy study in *Materials*](https://pmc.ncbi.nlm.nih.gov/articles/PMC12842681/) |
| Vickers hardness | [Alloy hardness study](https://www.nature.com/articles/s41524-025-01560-2) |
