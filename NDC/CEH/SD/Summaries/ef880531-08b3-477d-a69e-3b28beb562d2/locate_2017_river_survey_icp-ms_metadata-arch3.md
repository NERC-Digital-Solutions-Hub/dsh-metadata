# Summary

- LOCATE is a multidisciplinary NERC project involving major UK institutions to understand carbon flow from land to the ocean. Part 2 provides ICP-MS results for river water, complementing Part 1 which covers river water parameters (e.g., temperature, salinity, nutrients, organic carbon, isotopes) and estuary data. Part 2 focuses on major and trace elements across 41 rivers in England, Scotland, and Wales, sampled monthly in 2017 (plus a trial in November 2016); sampling sites were standardized to support data integration.

- Dataset scope and design
  - Geographic coverage: 41 rivers across Great Britain; sampling intended to reflect different land-use types representative of GB.
  - Temporal coverage: monthly samples in 2017 (most sites in all months; Dorset Stour excluded from some months and sampled from April 2017); November 2016 included as a trial period.
  - Dataset content: results of ICP-MS analyses for major and trace elements in river water; companion dataset for estuaries and Part 1 river water parameters exists with DOIs and is accessible via the British Oceanographic Data Centre (BODC).

- Sampling regime and field methods
  - Sampling regime: fixed site per river; most months undertaken within 2–3 days per month; coordination led by BGS.
  - In-field procedures:
    - Field filtering of samples (except particulate organic carbon) and preparation of bottles; samples kept in the dark in coolers or freezers.
    - Salinity, electrical conductivity (SEC), and temperature measured in the field; if a probe was unavailable, samples were sealed for later analysis.
    - Mid-channel sampling at shallow depths (0–30 cm) or representative mid-river locations; depth and site conditions recorded.
    - Field data forms captured weather and river conditions; photos were taken upstream and downstream (not submitted to EIDC but available).
    - Contamination controls included gloves and standardized rinsing of vessels.
  - Sample types and handling:
    - ICP-MS samples: 60 mL bottles with 0.45 μm filtered river water.
    - Isotope samples: 0.45 μm filtered and stored in 20 mL glass vials.
    - Transport and storage: samples kept cold (cool box or freezer) and returned to participating labs; acidified to 1% HNO3 for ICP-MS analysis; blanks prepared via acidified MQ water.
  - Post-collection handling:
    - Samples sent to BGS Keyworth for analysis; QAQC and calibration steps implemented to guarantee traceability and data quality.

- Analytical methods and QA/QC
  - Instrumentation: Agilent 8900 ICP-QQQ ICP-MS.
  - Method: Ag_2.3.21 Determination of major and trace elements in aqueous samples using ICP-MS.
  - Measurement units: mg/L or μg/L; 0.45 μm filtered water used for analysis; after receipt, samples acidified further to 0.5% v/v HCl.
  - Data format: results stored in a 61-column CSV file with fields including River, Month, LIMS sample number, and concentrations for a wide panel of elements (e.g., Ca, Mg, Na, K, P, S, Si, Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, V, Cr, Co, Ni, Cu, Zn, Ga, As, Se, Rb, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, La, Pr, Nd, Sm, Eu, Gd, Tb, Dy, Ho, Er, Yb, Tm, Lu, Hf, Ta, W, Tl, Pb, Bi, Th, U).
  - Detection limits: two DLs per element in each column (Batch DL and Method DL). If a value is below DL, it is reported as < DL.
  - Quality assurance:
    - UKAS accreditation: BGS laboratory (ISO/IEC 17025:2017, UKAS lab number 1816).
    - QC protocol: QC runs every 20 samples; calibration blocks included per run; use of certified multi-element and single-element standards for calibration and validation.
  - Data integrity and traceability: detailed metadata accompany results, including LIMS sample numbers, river identity, month, and element-specific detection limits, enabling auditability and reproducibility.

- Data governance, accessibility, and integration
  - Data management: results are organized in a structured CSV with explicit metadata fields (e.g., LIMS code, River, Month, element concentrations, DLs).
  - Data sharing: Part 1 data and related estuary datasets have DOIs and are associated with BODC; outputs are intended to be disseminated to stakeholders and the public under appropriate data governance.
  - Integration with other datasets: Part 2 data is designed to complement Part 1 river water parameters and the estuary dataset, enabling cross-domain analyses of carbon and geochemical fluxes from land to sea.

- Implications for monitoring frameworks
  - Demonstrates a rigorous, end-to-end data lifecycle for environmental monitoring: robust field protocols, standardized laboratory analyses with accredited QA/QC, and comprehensive metadata to support transparency, replication, and policy evaluation.
  - Provides a model for data interoperability across related components (river water chemistry, estuary chemistry, carbon parameters), useful for evaluating environmental health and informing decision-making.
  - Highlights the value of clear data governance, publication-ready data formats, and explicit handling of detection limits to ensure data is usable for policy analysis and future decision-making.