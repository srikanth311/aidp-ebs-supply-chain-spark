# AIDP EBS Supply Chain Demo — Spark Transformations

This repository will contain the AIDP notebooks and validation code that transform the synthetic Oracle source into governed standard-catalog Silver and Gold tables.

It is intentionally separate from the ingestion repository:

- Ingestion repository: creates and loads the dedicated Oracle demo schema.
- Spark repository: reads that schema through an AIDP external catalog and writes curated Delta tables to an AIDP standard catalog.

## Planned outputs

```text
SUPPLY_PO_LINE_COMPARISON
SUPPLY_PO_PRICE_REVIEW_FEATURES
SUPPLY_PO_PRICE_REVIEW_OUTPUT
```

## Planned notebooks

```text
notebooks/
├── 01_external_catalog_preflight.ipynb
├── 02_build_silver_po_line_comparison.ipynb
├── 03_build_gold_price_review_output.ipynb
└── 04_validate_standard_catalog_outputs.ipynb
```

The notebooks will be created after the ingestion repository and CSV contract are finalized.

No Oracle wallet belongs in this repository. AIDP catalog, schema, and cluster identifiers will be supplied through notebook parameters or an untracked local configuration file.

Public ingestion repository URL: `<PUBLIC_INGESTION_REPOSITORY_URL>`
