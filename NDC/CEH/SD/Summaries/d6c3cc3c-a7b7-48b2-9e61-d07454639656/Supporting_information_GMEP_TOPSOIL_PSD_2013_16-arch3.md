# Glastir Monitoring & Evaluation Programme

## Overview and aims
- Welsh Government monitoring initiative (Glastir Monitoring and Evaluation Programme, GMEP) started in 2013 to assess effects of Glastir agri-environment schemes on environmental outcomes.
- Primary aim: gather evidence on soil quality and broader environmental indicators to evaluate scheme effectiveness and inform future policy decisions (climate, biodiversity, soil and water quality, woodland expansion).
- Also intended to quantify general soil quality status and trends, identifying impacts from drivers such as land use, climate, and pollution beyond Glastir interventions.

## Monitoring design and sampling framework
- Four-year rolling survey cycle (2013–2016) to maximise spatial coverage while tracking year-to-year changes.
- Two components:
  - Wider Wales Component: baseline estimates, national trends, national reporting for Glastir.
  - Targeted Component: focuses on Glastir priority areas.
- Integration across components achieved by using a common spatial unit of 1 km square.
- Sample frame: 300 x 1 km squares over the cycle.
  - Half random within strata defined by the Land Classification of Great Britain (to capture environmental heterogeneity).
  - Half targeted to Glastir priority areas.
- Exclusions: squares with >75% urban land or >90% sea.
- Within each square: soil samples collected from 5 predetermined, randomly dispersed locations when possible, using a 15 cm C-core; samples sent to laboratories (UK CEH, Bangor).

## Soil analysis and measurement methods
- Primary metric: soil particle size distribution (PSD), a key property affecting hydrology, pollutant transport, nutrient availability, erosion, soil biology, and productivity.
- Methods used:
  - Laser diffraction (Beckman Coulter LS13 320) to measure PSD quickly, with small soil amounts.
  - Traditional hydrometer method used for method comparison and benchmarking.
- Sample preparation:
  - Organic matter removed using a peroxide digestion (UK CEH Bangor standard procedure).
  - Samples prepared with Calgon (5%) and treated with a platform shaker before measurement.
- Instrument operation and QA:
  - Instrument warm-up, alignment, and run settings standardized.
  - Sand fraction captured with a 63 µm sieve for cross-checking results.
  - Use of reference soils and internal Bangor standards (BS1, BS3) for QA/QC; includs duplicates to test reproducibility.
- Data quality considerations:
  - LD measurements generally accurate and reproducible; discrepancies with hydrometer linked to methodological differences (e.g., clay-sized measurements) and high organic matter interfering with LD in some cases.
  - Adjusted PSD cut-offs based on validation: Sand 64.61–2000 µm, Silt 2.42–63.41 µm, Clay 0.04–2.41 µm.
  - Organic matter content (loss on ignition) can bias LD measurements; removal improves reliability but recalcitrant organics may persist.

## Data quality assurance and validation
- QA/QC protocols aligned with NERC Joint Codes of Practice; routine inclusion of standard soils; pre-run instrument calibration and rinsing; duplicate samples for reproducibility checks.
- Cross-method comparison:
  - PSD results from laser diffraction (LD) compared with hydrometer method using internal standards (BS1, BS3) and then plotted against “true values” from historic data or external labs.
  - Found LD to be accurate and, in many cases, more representative of the true clay size distribution than sedimentation-based methods.
- Inter-laboratory comparison:
  - PSD results for sandy, silty, and clayey soils compared against ADAS and BGS laboratories.
  - Demonstrated that LD-based measurements were reproducible and comparable with other UK laboratories.

## Data structure, metadata, and governance
- Metadata structure described for the dataset GMEP_TOPSOIL_PSD_2013_16.csv, including:
  - SQ_ID, PLOT_TYPE, PLOTNUM, PLOTYEAR, geographic coordinates, land classification, repetition indicators, batch, and PSD size-bin percentages (SAND, SILT, CLAY) and TOTAL.
- Data governance and openness:
  - Outputs are disseminated via reports, charts, and dashboards; underlying data are intended to be shared publicly where appropriate, aligning with governance standards and openness expectations.
- Integration and interoperability:
  - Adoption of a common spatial unit (1 km) and alignment with the Countryside Survey of Great Britain supports potential integration and comparability with GB-wide datasets in future analyses.

## Key findings and implications for monitoring frameworks
- Demonstrates a robust, multi-scale, ecosystem-based monitoring approach:
  - Combines baseline national estimates with targeted, scheme-specific monitoring.
  - Ensures data comparability across time and space through standardized sampling and measurement protocols.
- Validates the use of laser diffraction for PSD in soil monitoring:
  - Faster, smaller samples, broad size-range, and strong reproducibility when properly QA/QC’ed.
  - Important caveat: high organic matter can bias LD results; standardization of pre-treatment and cut-offs is critical.
- Highlights importance of data availability and governance:
  - Metadata transparency and data sharing enable independent verification and integration with other datasets.
- Provides a model for policy-relevant monitoring:
  - Links monitoring design to policy evaluation needs (baseline establishment, trend detection, evidence for policy adjustments).
  - Emphasizes alignment with existing national surveys to facilitate future data integration.

## Challenges and considerations for future monitoring work
- Data gaps and access: ensuring timely data availability and avoiding data silos between organisations.
- Metadata adequacy: maintaining comprehensive metadata to enable verification and re-use.
- Data transformation: harmonising data formats for cross-study analyses (e.g., PSD cut-offs and bin definitions).
- Communicating complex findings: presenting multi-metric, multi-scale results clearly to policymakers.
- Data governance: maintaining standards for data storage, sharing, and updating to support ongoing monitoring.

## Notable personnel and collaborations
- UK CEH staff and Bangor University involved in QA, soil processing, data management, and analysis.
- Field survey teams across multiple sites and personnel contributed to data collection and sample handling.
- Cross-lab collaboration with ADAS and BGS to validate methods and ensure comparability.