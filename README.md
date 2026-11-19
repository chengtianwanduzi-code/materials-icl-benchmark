# In-Context Learning for Materials Property Prediction

**Research preview · 20 November 2026 · Manuscript in preparation**

We study how well general-purpose language models predict quantitative properties of polymers, inorganic crystals, and alloys when given labeled examples at inference time. The evaluation compares in-context learning (ICL) with conventional machine learning, materials-specific models, and tabular foundation models.

## Preliminary results

These tables use the same external evaluation records for every model within a property. The cohort includes **463 records across 143 distinct materials and 43 sources**, covering 11 properties. It was curated to separate the evaluation materials and reference values from earlier public records and to keep evaluation material identities out of the study's training pools. The polymer and alloy endpoints use reported measurements. The crystal endpoints use computational reference values.

| Comparison | Description | Results |
| --- | --- | --- |
| Shared training data | Methods use the same public training pool for each property. | [RMSE table](results/shared-training.md) |
| Training data from prior studies | Methods use a common pool drawn from the corresponding public reference dataset for each property. | [RMSE table](results/reference-training.md) |

Performance varies by endpoint. In the shared-training table, full-context Sol reaches 29.13 K RMSE on glass transition temperature and GPT-5.2 reaches 0.1358 g/cm³ on experimental density. Random forest reaches 23.23 K on melting temperature, the lowest error reported for that endpoint in the shared-training table.

The results describe this evaluation cohort. Some endpoints have few distinct materials, including four for melting temperature and nine for band gap. Seven of the nine band-gap reference values are zero. The tables distinguish evaluation records from distinct materials so that repeated measurements or processing conditions are visible in the sample counts.
