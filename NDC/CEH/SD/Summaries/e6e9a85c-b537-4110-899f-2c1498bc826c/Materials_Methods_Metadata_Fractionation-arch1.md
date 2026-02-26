# Materials and methods, and metadata for Phosphorus, carbon and nitrogen concentrations in UK soil mineral fractions, 2013-2014. Data taken from 'An investigation of the distribution of phosphorus between free and mineral associated soil organic matter, using density fractionation', Adams et al 2018, Plant & Soil

## Overview
- Datasets describing phosphorus (P), carbon (C) and nitrogen (N) concentrations in UK soil mineral fractions from 2013–2014, aligned with Adams et al. 2018 Plant & Soil.
- Focus on density-based soil fractionation to separate light and heavy organic matter, producing fractions such as light fraction (LF), heavy fraction (HF), and occluded/light components (OLF, NLF).
- Measurements include total and fractionated concentrations of organic carbon (OC), total nitrogen (TN), total phosphorus (TP), inorganic phosphorus (IP), and organic phosphorus (OP), across multiple vegetation types and catchments.
- Supplement contains extensive metadata and detailed column definitions for six tables (S1–S6) to enable data discovery, interpretation, and reuse.

## Methods (fractionation and analysis)
- One density fractionation per soil sample using 25 g subsamples in 400 mL bottles with 250 mL sodium polytungstate (NaPT) at density 1.6 g cm-3.
- Separation of non-light fraction (NLF) material; removal of NLF using pipettes or mesh bags; re-centrifugation to repeat until all NLF accounted for.
- Rinsing: samples rinsed with deionised water; conductivity monitored; complete removal of NaPT assumed when conductivity < 50 μS cm-1 (calcareous soils < 200 μS cm-1 acceptable due to carbonate dissolution).
- OLF extraction via sonication; disruption checked microscopically; OLF combined with NLF; LF rinsed and dried.
- HF treatment: remaining material subjected to repeated centrifugation and rinsing until conductivity < 50–200 μS cm-1; HF dried and ground.
- Carbonate removal: samples with potential inorganic carbonate (bulk pH > 5.5) treated with 0.1 M HCl; CO2 release observed microscopically until complete.
- Analyses:
  - Total organic carbon (TOC) and total nitrogen (TN) in milled sub-samples by Vario EL elemental analyser.
  - Total phosphorus (TP) by ignition-extraction method (Olsen & Sommers 1982 approach).
  - Inorganic phosphorus (IP) by extracting 0.5 g soil with 25 mL 0.5 M sulfuric acid, followed by molybdate analysis; organic P (OP) computed as TP − IP.
- Replication: all analyses replicated four-fold.
- Bulk analyses (for comparison) used the same C and N methods and IP, but TP analyzed by aqua regia microwave digestion (as per Toberman et al. 2016).
- Quality and provenance: methods and measurements documented; data and methods cross-referenced to published sources.

## Data structure and content (Tables S1–S6)
- Table S1. Sample information
  - Sample ID, vegetation type (e.g., b = broadleaf), depth (shallow s or deep d), catchment (e.g., C = Conwy), date, database ID, and other location metadata.
- Table S2. Recovery of soil mass in density fractionation
  - Details per sample: date of collection, geographic coordinates, MAP (mean annual precipitation), MAT (mean annual temperature), land use, starting mass, bulk mass, fraction masses (LF, HF), and related recovery metrics (e.g., %LF, %HF).
  - Additional descriptive fields: soil type, pH, bulk density, organic C, and other attributes linked to each sample.
- Table S3. OC & TN concentration data
  - Content by fraction: OC bulk, OC LF, OC HF; TN bulk, TN LF, TN HF; units in percent (%).
- Table S4. TP, IP & OP concentration data
  - Fractional content: bulk TP, bulk IP, bulk OP; LF TP, LF IP, LF OP; HF TP, HF IP, HF OP; units in mg g−1.
- Table S5. Recoveries of OC & TN
  - Recoveries for bulk OC/TN and for combined LF+HF OC/TN; recovery percentages and related notes.
- Table S6. Recoveries of TP, IP & OP
  - Recoveries for bulk TP/IP/OP and LF+HF TP/IP/OP; recovery percentages and related notes.
- Column header explanations (extensive) included for Tables S2–S6, detailing variable definitions such as date, latitude, longitude, MAP, MAT, depth, land use, sample mass metrics, fraction masses, pH, bulk density, OC/TN/TP/IP/OP values by fraction, and recovery calculations.
- Units
  - OC and TN: percent (%, by mass).
  - TP, IP, OP: mg g−1 (and related fractions: LF, HF, bulk).
  - Additional metadata: dates, coordinates, depths, and concentration-recovery metrics.

## Data quality, interpretation, and use
- Replication and detailed methodology support reproducibility and cross-study comparisons.
- Fractionation method relies on a defined density cut-off (1.6 g cm−3) and careful handling of NLF/OLF/HF to minimize artefacts.
- Carbonate-rich (calcareous) soils require careful interpretation due to the dissolution step and conductivity thresholds.
- Data are provided with extensive metadata and table-specific definitions, enabling local-scale analysis across vegetation types, catchments, and sampling depths.
- Provenance and references
  - Primary data and methods: Adams et al. 2018, Plant & Soil (data source for distribution of phosphorus between free and mineral-associated soil organic matter).
  - Supporting methodologies and context: Cerli et al. 2012; Olsen & Sommers 1982; Schrumpf et al. 2013.
  - Bulk soil context: Toberman et al. 2016 (LTLS soil survey, England, Scotland, Wales, 2013–2014).