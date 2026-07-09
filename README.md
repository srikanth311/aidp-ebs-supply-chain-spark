# AIDP EBS Supply Chain Demo — Spark Transformations

This repository contains the AIDP notebooks that transform the synthetic Oracle source into governed standard-catalog Silver and Gold tables.

It is intentionally separate from the ingestion repository:

- Ingestion repository: creates and loads the dedicated Oracle demo schema.
- Spark repository: reads that schema through an AIDP external catalog and writes curated Delta tables to an AIDP standard catalog.

## Outputs

```text
SUPPLY_PO_LINE_COMPARISON
SUPPLY_PO_PRICE_REVIEW_FEATURES
SUPPLY_PO_PRICE_REVIEW_OUTPUT
```

## Notebooks

```text
notebooks/
├── 01_external_and_standard_catalog_preflight.ipynb
├── 02_build_silver_supply_chain_tables.ipynb
├── 03_build_gold_price_review_output.ipynb
└── 04_validate_standard_catalog_outputs.ipynb
```

Run the notebooks in order from AIDP Workbench after creating the source external catalog and target standard catalog.

Default notebook configuration:

```text
SOURCE_CATALOG=aidp_sc_demo_source
SOURCE_SCHEMA=aidp_sc_demo
TARGET_CATALOG=aidp_sc_demo_standard
SILVER_SCHEMA=supply_chain_silver
GOLD_SCHEMA=supply_chain_gold
```

No Oracle wallet belongs in this repository. The notebooks read through the AIDP external catalog and write to the AIDP standard catalog.

Public ingestion repository URL: `https://github.com/srikanth311/aidp-ebs-supply-chain-ingestion`
