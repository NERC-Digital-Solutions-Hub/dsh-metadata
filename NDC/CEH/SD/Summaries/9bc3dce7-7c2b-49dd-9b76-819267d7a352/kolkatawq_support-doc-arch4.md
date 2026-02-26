# Kolkata Water Quality Dataset (KolkataWQ)

## Overview
- A dataset of urban surface water quality in Kolkata, India, combining field sensor measurements and laboratory analyses.
- Collected across three field surveys: June 2018, March 2019, and December 2019.
- Includes geographic coordinates for all sample locations and details on the development and testing of a prototype in-situ fluorimeter to identify waters with high bacterial load.

## What the dataset contains
- Three CSV files:
  - 1_KolkataWQ_Jun2018.csv (20 columns)
  - 2_KolkataWQ_Mar2019.csv (37 columns)
  - 3_KolkataWQ_Dec2019.csv (33 columns)
- Parameters and measurements fall into:
  - In-field physicochemical parameters (e.g., electrical conductivity, pH, dissolved oxygen, temperature)
  - Laboratory nutrient analyses (ammonium, phosphate, nitrite, nitrate, dissolved organic carbon)
  - Microbiological analyses (Escherichia coli, coliforms, total bacterial cells)
  - Fluorescence and absorbance measurements from prototype fluorimeters (Peak T, Peak C, chlorophyll-a, CDOM, tryptophan, turbidity, absorbance at 280 nm)
- Data quality notes include: missing values marked as NA; excitation-emission matrix data (Aqualog) discarded due to sample integrity concerns; some field logs captured as single values due to logging issues.

## Sampling and field collection
- Field sites located primarily within Kolkata urban area, spanning three watercourse types: Hooghly River (Ganga), East Kolkata Wetlands, and open sewage canals; includes samples outside Kolkata (marine and groundwater references RS1_DHG and RS1_NLH) and controls (municipal water supply and deionised water).
- Approximately 40 sampling events across two years; most sites sampled once, with some revisits for seasonal/diurnal comparisons.
- Collection method:
  - Samples collected ~1 m from bank/boat side using a 2 L bucket; field time, date, and GPS location recorded.
  - In-field subsamples used for physicochemical measurements; additional subsamples filtered for laboratory analysis within 24 hours.

## Measurements, instruments, and methods
- In-field physicochemical measurements (files 1–3):
  - DO, conductivity, pH, temperature; different equipment across surveys (e.g., HQ10 DO meters, Accumet conductivity meters, Ultrameter 6Pfc).
- Nutrient analyses (laboratory, within 24 h of collection):
  - Ammonia, ammonium, phosphate, nitrate, nitrite; performed using Palintest photometer and CEH lab analyses; major dissolved nutrients and DOC measured via ion chromatography and thermal oxidation (Bowes et al. 2020 methods).
- Microbiological analyses (laboratory, within 6–24 h):
  - E. coli, total coliforms, other coliforms; membrane filtration and MLGA methods; flow cytometry for total bacterial cells after glutaraldehyde fixation and SYBR Green I staining.
- Prototype fluorimeter data (in-field sensors):
  - 2018: three single-channel Chelsea sensors (Peak C, Peak T, turbidity).
  - 2019: five-channel VLux TPro sensor (multi-parameter outputs: chlorophyll-a, tryptophan, CDOM, absorbance, turbidity, plus individual channels and corrected values).
  - Data collection specifics:
    - Depth: up to 30 cm; data logged every second; averaged to 1-minute intervals (n = 60) for analysis.
    - 2019: Raspberry Pi data logger (TR1) with Python GUI; 2019 Dec: Hawk data logger; some single readings occurred due to logging issues.
- Data alignment and details:
  - File 1 provides 20 columns with mapping for field and lab analyses, including field-logged and lab-measured values.
  - File 2 provides 37 columns, with extended metadata for the 2019 March survey (including total bacterial cells and chlorophyll fluorescence parameters).
  - File 3 provides 33 columns for December 2019 with advanced field measurements (DO_s, TDS, ORP, etc.) and extended fluorescence/nutrient columns.

## Data structure and metadata
- Each file contains sample-level metadata (Date, Time, Sample_ID, Latitude, Longitude) and instrument-specific measurement columns.
- Fluorescence and turbidity measurements are aligned to the corresponding sensor outputs (e.g., Peak T, Peak C, CDOM, Tryp, Chlorophyll-a) with standard units and data collection notes (average over 60 readings, single readings where applicable).
- Laboratory analyses specify the measurement method and turnaround (within 24 hours for nutrients; within 6 hours for microbial indicators).

## Data quality, limitations, and caveats
- Aqualog-derived excitation-emission data were discarded due to sample integrity concerns (age, storage, transport).
- Some field data logged manually resulted in single values rather than 60-minute averages (file 3 specifics).
- Missing values are explicitly labeled as NA; overall data completeness varies by parameter and survey.
- The dataset references and relies on established methods (e.g., Bowes et al. 2020) for nutrient and microbial analyses, and QC standards were used for chemical analyses.

## Data governance and reuse potential
- Provides a structured, multi-parameter, multi-survey view of urban water quality in Kolkata, suitable for:
  - Data-driven assessment of sensor-based monitoring versus lab analyses.
  - Cross-site comparisons of water quality across river, wetlands, and canal systems.
  - Evaluation and calibration of prototype fluorimeters for detecting bacterial contamination events.
- Metadata-rich files support discoverability and cross-referencing with methodological literature (Bowes et al. 2020).

## References
- Bowes, M.J. et al., 2020. Nutrient and microbial water quality of the upper Ganga River, India: identification of pollution sources. Environmental Monitoring and Assessment. https://doi.org/10.1007/s10661-020-08456-2