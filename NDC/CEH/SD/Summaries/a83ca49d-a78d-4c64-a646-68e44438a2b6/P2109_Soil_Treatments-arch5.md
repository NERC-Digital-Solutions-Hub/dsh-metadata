# NERC Soil Biodiversity Thematic Programme (Sourhope Field Data)

- Context: The NERC Soil Biodiversity Thematic Programme (established 1999) studied soil biota and their functional roles through 24 projects at the Sourhope field site, focusing on soil structure, processes (carbon and nitrogen cycles), and the roles of micro-, meso-, and macro-fauna and flora.
- Purpose and scope: Aimed to understand soil biodiversity and its ecological processes, with data generated from field measurements and treatments that can be used as explanatory variables in conjunction with other datasets from the site.

## Dataset overview

- Dataset name: P2109_VIEW_SOIL_TREATMENTS.csv
- Time coverage: Treatments applied 1999–2001, with additional data included for 2001–2004.
- Purpose: Describes range of site and plot-level treatments and can be used alongside other experimental datasets as explanatory variables.
- Documentation reference: Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003); available as Supporting Information via the EIDC catalogue.

## Dataset schema (key fields)

- TREATMENT_DATE: Date treatment was applied to soil.
- BLOCK: Block number (1–5).
- MAIN_PLOT: Main plot identifier (A–F).
- SUB_PLOT: Sub-plot identifier.
- CELL_X: Cell grid number X.
- CELL_Y: Cell grid number Y.
- TREATMENT_TYPE: Type of treatment applied.
- DOSAGE: Details of dosage.

## Treatments and experimental design

- Site-level treatment: Vegetation cutting (multiple cuts per year with specific date ranges, including note of a mower downtime in some years).
- Plot-level treatments (six categories):
  1) Control 1 – No treatment
  2) Control 2 – No treatment
  3) Nitrogen – NH4NO3 fertilizer; annual rate 24 g m-2; split into two doses per year; applied in spring and late spring/summer across 4 years (1999–2002)
  4) Lime – CaCO3; annual rate 600 g m-2; single annual dose in spring across 4 years
  5) Nitrogen and Lime – combination of Nitrogen and Lime treatments
  6) Insecticide – Dursban 4 OPA; application pattern varies by year; annual rate 7.5 L ha-1; applied after mowing when weather permitted; multiple applications per year

- Year-by-year application windows (highlights):
  - Nitrogen: Spring and late spring windows vary by year (1999–2002)
  - Lime: Spring applications each year (1999–2002)
  - Insecticide: Multiple applications per year with specific dates per year (1999–2002)

## Data access, provenance and documentation

- Availability: Data intended for dissemination alongside other site datasets; available through the EIDC catalogue (Supporting Information).
- Provenance references: Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003)
- Metadata: Dataset description includes field definitions and treatment details to support interoperability with other Sourhope datasets.

## Data quality, governance and usage notes

- Quality assurance: Data are subject to QA procedures, but NERC does not warrant the accuracy of data supplied, nor accepts liability for their use.
- Metadata and standards: Metadata exists for key fields; linkage to published handbook recommended for full context.
- Potential limitations for users: Incomplete or evolving user needs; potential challenges integrating across multiple systems/formats; long transfer times for large datasets; some data may require consultation with data custodians to confirm details (e.g., dates, treatment specifics).
- Data updating: Dataset includes multiple years; governance should specify how updates are incorporated and communicated.

## Data stewardship considerations and challenges (relevant to governance)

- Ensure complete, consistent metadata aligned with the cited Scotts et al. documentation.
- Capture data provenance, including treatment administration details and field conditions.
- Manage data availability and sharing limitations (embargoes, proprietary aspects, disclosure risks).
- Plan for interoperability across多年 datasets and formats; provide clear identifiers for blocks, plots, and cell coordinates.
- Document data quality checks and any known data cautions to end users.
- Maintain an auditable pathway for updates and ensure dataset can be discovered via relevant portals/catalogues (e.g., EIDC).

## Legal and liability notes

- Disclaimer: NERC cannot warrant the accuracy of any data or determine fitness for a user’s intended use; no liability for loss, damage, or injury arising from use of these data.