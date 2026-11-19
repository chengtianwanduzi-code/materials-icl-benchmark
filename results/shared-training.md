# Shared training data

Within a property, the methods share the same public training pool and external evaluation cohort. The training-set mean is included as a reference. The no-example control uses the same evaluation queries.

Values are RMSE in the units shown. Scores are displayed as mean ± standard deviation where available. **Bold** indicates the lowest reported RMSE in each column within this table. A dash denotes an unavailable result or a comparison outside the scope of that model. Sample counts appear below each endpoint. n is the number of evaluation records and m is the number of distinct materials.

## Polymers

| Model | Glass transition (K)<br>n=59, m=58 | Melting temperature (K)<br>n=6, m=4 | Experimental density (g/cm³)<br>n=15, m=15 | Experimental refractive index<br>n=13, m=13 |
| --- | ---: | ---: | ---: | ---: |
| Training-set mean | 90.92 | 108.1 | 0.6793 | 0.2285 |
| Random forest | 46.09 ± 0.467 | **23.23 ± 0.866** | 0.6187 ± 0.000421 | 0.1797 ± 0.00102 |
| XGBoost | 50.46 ± 0 | 41.85 ± 0 | 0.5816 ± 0 | 0.1571 ± 0 |
| polyBERT | 40.5 ± 1.36 | 69.24 ± 14.2 | 0.5801 ± 0.0114 | 0.1318 ± 0.00524 |
| TransPolymer | 39.26 ± 1.94 | 65.69 ± 2.6 | 0.5585 ± 0.0184 | 0.1662 ± 0.00175 |
| MMPolymer | — | — | 0.5854 ± 0.0136 | 0.1642 ± 0.0827 |
| PerioGT | — | — | — | 3.926e+14 ± 6.38e+14 † |
| MolCLR | 49.03 ± 0.905 | 54.67 ± 26 | 0.5619 ± 0.0151 | 0.1657 ± 0.0338 |
| Uni-Mol | — | — | 0.5348 ± 0.0206 | 0.1269 ± 0.00797 |
| Sol (no-example control) | 31.37 ± 1.3 | 73.94 ± 3.96 | 0.162 ± 0.00837 | 0.03585 ± 0.00218 |
| Sol (full-context ICL) | **29.13 ± 2.26** | 62.86 ± 6.42 | 0.1532 ± 0.0131 | **0.0333 ± 0.000765** |
| Sol (retrieval ICL) | 29.46 ± 1.4 | 57.63 ± 4.42 | 0.1435 ± 0.00669 | 0.03824 ± 0.00166 |
| GPT-6 Luna (full-context ICL) | 36.93 ± 0.5 | 68.17 ± 10.7 | 0.298 ± 0.0602 | 0.05215 ± 0.00534 |
| DeepSeek V4 Pro (full-context ICL) | 48.08 ± 4.82 | 62.4 ± 27.4 | 0.177 ± 0.0303 | 0.07316 ± 0.00501 |
| GPT-5.2 (full-context ICL) | 48.52 ± 5.44 | 67.89 ± 11.5 | **0.1358 ± 0.0209** | 0.08012 ± 0.00992 |
| GPT-4.1 (full-context ICL) | 53.84 ± 3.09 | 51.15 ± 14.9 | 0.1635 ± 0.00775 | 0.1116 ± 0.0164 |

## Inorganic crystals

| Model | PBE band gap (eV)<br>n=9, m=9 | Bulk modulus (GPa)<br>n=7, m=7 | Shear modulus (GPa)<br>n=7, m=7 |
| --- | ---: | ---: | ---: |
| Training-set mean | 1.634 | 48.55 | 24.58 |
| Random forest | 1.735 ± 0.0479 | 51.6 ± 0.988 | 19.29 ± 1.15 |
| XGBoost | 1.256 ± 0 | 66.93 ± 0 | 20.96 ± 0 |
| CGCNN | 1.667 ± 0.223 | 52.45 ± 21.8 | 15.36 ± 0.95 |
| MEGNet | — | — | — |
| ALIGNN | — | 14.09 ± 9.84 | — |
| Matformer | — | — | — |
| DenseGNN | — | — | — |
| Sol (no-example control) | **0.02502 ± 0.0133** | 128.4 ± 18 | 78.71 ± 5.73 |
| Sol (full-context ICL) | 0.05304 ± 0.0305 | 331.5 ± 69.7 | 78.62 ± 6.12 |
| Sol (retrieval ICL) | 0.04021 ± 0.0388 | 149.3 ± 25 | 74.59 ± 11 |
| GPT-6 Luna (full-context ICL) | 1.035 ± 0.819 | **14.04 ± 2.85** | 18.73 ± 2.32 |
| DeepSeek V4 Pro (full-context ICL) | 1.074 ± 0.123 | 24.27 ± 4.58 | **14.95 ± 0.55** |
| GPT-5.2 (full-context ICL) | 2.086 ± 0.33 | 27.16 ± 3.67 | 18.3 ± 1.79 |
| GPT-4.1 (full-context ICL) | 1.558 ± 0.153 | 17.59 ± 3.73 | 15.16 ± 4.02 |

## Alloys

| Model | Yield strength (MPa)<br>n=137, m=39 | Ultimate tensile strength (MPa)<br>n=140, m=40 | Elongation (percentage points)<br>n=29, m=21 | Vickers hardness (HV)<br>n=41, m=24 |
| --- | ---: | ---: | ---: | ---: |
| Training-set mean | 554.8 | 661 | 18.46 | 242.2 |
| Random forest | 587.5 ± 6.65 | 659.8 ± 8.36 | 24.94 ± 0.673 | 217.7 ± 1.37 |
| XGBoost | 611.3 ± 0 | 739.6 ± 0 | 24.84 ± 4.35e-15 | 240.3 ± 0 |
| CrabNet | 681.3 ± 36.6 | 604.6 ± 28.3 | 30.83 ± 5.98 | 246.4 ± 3.78 |
| Roost | 806.5 ± 81.1 | 683.9 ± 149 | 33.38 ± 7.91 | 223.4 ± 23 |
| MODNet | 931.8 ± 55 | 947.4 ± 27.5 | 30.98 ± 7.45 | 217.8 ± 35.9 |
| ICL-FM | 582.7 ± 7.36 | 630.8 ± 2.44 | 24.15 ± 0.789 | 215.1 ± 1.71 |
| TabICL | 585.2 ± 12.7 | 631.2 ± 8.2 | 23.41 ± 0.349 | 207.2 ± 1.47 |
| Sol (no-example control) | 289.7 ± 8.21 | **373.1 ± 8.27** | 10.33 ± 0.45 | 193.1 ± 6.27 |
| Sol (full-context ICL) | **288.7 ± 6.76** | 379.6 ± 4.63 | **9.393 ± 0.157** | **173.5 ± 3.34** |
| Sol (retrieval ICL) | 306.9 ± 8.89 | 395.2 ± 6.15 | 9.639 ± 0.1 | 189.9 ± 7.88 |
| GPT-6 Luna (full-context ICL) | 490.4 ± 12.9 | 594.7 ± 8.24 | 20.33 ± 2.03 | 232.8 ± 7.24 |
| DeepSeek V4 Pro (full-context ICL) | 334.2 ± 9.73 | 416.4 ± 10.4 | 20.96 ± 3.67 | 183.7 ± 6.9 |
| GPT-5.2 (full-context ICL) | 407.4 ± 19.2 | 434.8 ± 19.7 | 24.27 ± 2.49 | 186.1 ± 4.96 |
| GPT-4.1 (full-context ICL) | 514 ± 10.3 | 867.1 ± 41.5 | 21.76 ± 1.74 | 265.4 ± 15.8 |

† The PerioGT refractive-index error is a numerical outlier in the evaluated configuration.
