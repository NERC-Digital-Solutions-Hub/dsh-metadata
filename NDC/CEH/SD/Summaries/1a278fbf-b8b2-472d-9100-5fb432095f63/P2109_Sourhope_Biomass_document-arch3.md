# SOURHOPE FIELD DATA HANDBOOK 2003

## Background and Aims
- NERC Soil Biodiversity Thematic Programme established in 1999, centered on a large field experiment at Sourhope (Macaulay Land Use Research Institute, now James Hutton Institute) in the Scottish Borders.
- Primary aims: understand soil biota biodiversity and the functional roles of soil organisms in key ecological processes.
- 24 projects funded to study soil structure, soil processes (e.g., carbon and nitrogen cycles), and roles of micro-, meso-, and macro-fauna and flora (bacteria, nematodes, protozoa, fungi, Collembola, Acari, Tipulid/Bidionid/Scarabeid larvae, Enchytraeidae, Megradili, Mollusca, Coleoptera).

## Data Collected
- Above-ground biomass (vegetation biomass) measurements:
  - Collected on five occasions across 1999–2002 growing seasons from 50 x 50 cm cells within each main plot sub-plot.
  - Grass cuttings dried at 80°C and weighed; biomass values calculated.
  - July 1999 included mineral nutrient analysis for blocks and main plots (lab work by Macaulay Land Use Research Institute, Aberdeen).
- Mineral nutrient analyses (baseline 1999):
  - Vegetation nutrient content (N, Ca, K, Mg, P, Al) measured from vegetation samples.
  - Associated metadata on sample IDs, dates, treatments, blocks, main plots, and methods.
  - Detection limits provided for each nutrient (e.g., N, Ca, K, Mg, P, Al).
- Data structure described to facilitate reuse and interpretation (see below).

## Key Findings
- Biomass results showed a consistent ranking of biomass across treatments with peak production in July/August.
- Noted substantial biomass increase in 2001, likely due to staff changes and a switch from manual cutting to mechanical shears.
- Normalization suggestion: normalize all treatment measures against C1 in each year to assess ongoing effects of nitrogen and lime.
- Statistical analysis: ANOVA on ln-transformed biomass indicated significant differences between improved (N and/or lime) versus non-improved plots, a significant interaction between treatment and year, and no significant block effects (F = 0.76, df = 4,115, p > 0.05).

## Data Structure and Files
- Two CSV files provided:
  - Biomass values, 1999-2001: P2109_VEG_BIOMASS_1999_2002.csv
    - Key fields: MEASID, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, MEAS_DATE, BIOMASS (g per 50 x 50 cm cell).
  - Mineral nutrient analysis, 1999: P2109_BASELINE_99_VEG_MIN_ANAL.csv
    - Key fields include VEG_ID, CUT_DATE, TREATMENT, BLOCK, MAIN_PLOT, NITROGEN, CALCIUM, POTASSIUM, MAGNESIUM, PHOSPHORUS, ALUMINIUM (with detection limits and methods).
- Metadata and field descriptions reference Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003).

## Quality Assurance and Limitations
- Verification steps: numeric range checks, formatting checks, and logical integrity checks; internal MLURI QA procedures for laboratory analyses.
- Data are subject to QA procedures, but NERC cannot warrant accuracy or determine fitness for a given use; no liability for misuse or resulting losses or damages.
- Public sharing of underlying data and metadata can be a barrier; maintaining up-to-date metadata and data governance is emphasized.

## Access, Governance, and Use
- Data referenced as supporting information via the EIDC catalogue (SOURHOPE FIELD DATA HANDBOOK 2003).
- Emphasizes data quality, openness, and governance standards at the data source to facilitate reuse for monitoring, evaluation, and informing future decisions.

## Reference
- Scott, R.; Bell, J.; Kenny, C.; Jeffers, J.; Buckland, S.; Burt-Smith, G. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Available as Supporting Information via EIDC catalogue record.