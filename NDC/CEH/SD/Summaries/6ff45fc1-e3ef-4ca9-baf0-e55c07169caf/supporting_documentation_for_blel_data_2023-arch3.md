# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 2023

## Overview and scope
- Long-term monitoring dataset from Blelham Tarn, Cumbria, England, with fortnightly sampling throughout 2023 (Jan–Dec).
- Variables collected: surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3/L), pH, ammoniacal nitrogen (NH4N, µg N/L), total oxidised nitrogen (TON, µg N/L), soluble reactive phosphate (PO4P, µg P/L), total phosphorus (TOTP, µg P/L), dissolved reactive silicon (SIO2, µg/L), and phytoplankton chlorophyll a (TOCA, µg/L).
- Integrated water samples from 0–5 m; sampling primarily from a buoy at the deepest part of the lake; shore samples collected when buoy access was not possible (Flag 2).

## Sampling regime and data structure
- Sampling frequency: fortnightly during 2023 as part of ongoing monitoring.
- Data structure: CSV with columns including sdate (measurement date), variable (name of measurement), value (measurement value), sign(if<LOD) (indicator if below detection limit), and flag (sampling location indicator: 1 buoy, 2 shore).

## Measurement methods and calibration
- Surface temperature and dissolved oxygen:
  - Measured with a YSI ProODO handheld instrument.
  - DO saturation calculated from DO concentration; calibrations performed biweekly for DO % and daily for field measurements; target DO % 98–102% to pass.
- Secchi depth: measured by lowering a Secchi disk on a labeled rope.
- Alkalinity and pH: integrated water sample sealed to prevent atmospheric exchange; measured by Gran titration with a Radiometer electrode; electrode calibrated prior to each sampling.
- Total ammoniacal nitrogen (NH4N) and total oxidised nitrogen (TON):
  - Measured colorimetrically with a SEAL AQ2 analyzer after filtration.
  - NH4N method involves cycler reagents and indophenol blue reaction; UKAS-accredited; calibration and quality controls included.
  - TON method reduces nitrate to nitrite and uses colorimetric detection; UKAS-accredited; calibration and quality controls included.
- Total phosphorus (TP):
  - Digestion with potassium persulfate, followed by molybdenum blue colorimetric analysis; UV-Vis measurement; calibrations with standards and checks for precision/accuracy; blank corrections applied.
- Dissolved reactive silicon (SiO2) and soluble reactive phosphate (PO4P):
  - SiO2 measured colorimetrically using ammonium molybdate and ascorbic acid to form silicomolybenum blue; calibration and QC samples included.
  - PO4P measured colorimetrically (molybdenum blue) after filtration; calibration and blanks used for every lake sample.
- Phytoplankton chlorophyll a (TOCA):
  - Filtered sample extracted with boiling methanol; analyzed spectrophotometrically.

## Data quality, validation and limitations
- Data are raw and not yet quality controlled/calibrated; some QA performed:
  - Temperature, DO, Secchi, alkalinity, pH, PO4P, and TOCA data double-entered by different people and visually validated by a database manager.
- Missing data attributed to weather, equipment limitations, or staff shortages.
- Notes on data below detection limits indicated in the dataset via sign<LOD.
- Shore samples (Flag 2) used when buoy sampling was not possible, introducing potential comparability considerations with buoy samples.

## Data availability, metadata and governance
- Data are provided as CSV files for download; explicit metadata about data collection and processing is described within the document.
- Data governance elements include calibration schedules, QA steps performed, and documentation of methods; however, full public data sharing of all underlying datasets and complete metadata may require further governance steps to ensure transparency and reproducibility.

## Funding and references
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme.
- Data validation supported by NERC through the UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
- Method references include Mackereth et al. (1978), Mortimer (1981), and Talling (1974).

## Implications for monitoring framework development
- Demonstrates a structured, long-term, multi-parameter lake monitoring approach with:
  - Clear definition of sampling locations, integrated depth, and frequency.
  - Comprehensive measurement methods with calibration and QA protocols.
  - Well-documented data structure, units, and flags for detection limits and sampling site.
- Highlights practical challenges relevant to monitoring governance:
  - Use of raw data pending quality control; need for standardized, timely QC processes to enable policy-relevant use.
  - Importance of metadata completeness and accessibility to support data reuse and comparability across datasets.
  - Real-world data gaps due to weather, equipment, or staffing, emphasizing the value of robust data governance and transparent reporting.
- Provides a concrete example for setting data standards, metadata requirements, and QA procedures to inform future monitoring frameworks and decision-making.