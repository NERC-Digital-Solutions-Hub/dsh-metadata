# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water, UK, 2023. Feuchtmayr, H., Dodd, B.A., Guyatt, H., Hunt, A.G., Le Quesne, K., Mackay, E.B., McShane, G., Moorhouse, H., Rankin, G., Rhodes, G., Thackeray, S.J. (2025)

## Overview
- Long-term, fortnightly monitoring dataset from Esthwaite Tarn, Cumbria, England.
- 2023 data cover surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, and several nutrients and phytoplankton chlorophyll a (TOCA).
- Data are provided as raw measurements, with some prior data entry validation; raw data not yet fully quality controlled or calibrated.

## Data Content and Variables
- Variables and units included:
  - TEMP: temperature in degrees Celsius
  - OXYG: oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - pH: pH units
  - NH4N: total ammoniacal nitrogen in µg N per litre
  - TON: total oxidised nitrogen in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon as SiO2 in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre
- Water integrated from 0 to 5 m; occasional shore samples when buoy access is not possible.
- Data reported for 2023 only.
- Special fields:
  - sign(if<LOD): indicates values below detection limit with a "<" sign
  - flag: 1 = sample collected at buoy location; 2 = shore-based sample

## Sampling Regime and Collection Methods
- Fortnightly sampling as part of an ongoing monitoring program.
- Measurements collected from a boat at a marked buoy; when buoy access failed, samples taken from shore.
- All measurements reflect a single integrated water sample from 0–5 m depth.

## Data Quality Control and Validation
- Data are raw and have not yet undergone full quality control and calibration.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people and visually validated by a database manager (graphs reviewed).
- Missing data attributed to weather, equipment limitations, or staff limitations.
- UKAS-accredited methods referenced for specific measurements (NH4N, TON); other parameters described with standard methods and calibration notes.

## Data Structure and Metadata
- Data are provided as a comma-separated values (CSV) file.
- Columns include:
  - sdate: date of measurement
  - variable and description: name and qualitative description of the variable
  - value: measured value
  - sign(if<LOD): indicator for below-detection-limit values
  - flag: sampling location indicator (1 buoy, 2 shore)
- Each variable has clearly defined units and measurement methods described in the accompanying Methods section.

## Analytical Methods and Instrumentation
- Temperature and dissolved oxygen:
  - Measured with a YSI ProODO handheld instrument; DO % calibration daily; routine biweekly/bi-monthly calibrations for % DO.
- Secchi depth:
  - Measured with a Secchi disk on a labeled rope.
- Alkalinity and pH:
  - Integrated water sample sealed to prevent atmospheric exchange; Gran titration with a radiometer electrode; electrode calibrated prior to sampling.
- Nitrogen species (NH4N, TON):
  - Measured colorimetrically with SEAL AQ2 discrete analyzer after filtration; standard calibration with quality checks; UKAS accredited methods.
- Phosphorus (TP) and silicate (SIO2):
  - TP: digestion with potassium persulfate followed by molybdenum blue colorimetric analysis; absorbance at 880 nm with UV-Vis spectrophotometer; blanks and reference materials used for accuracy.
  - SIO2: colorimetric silicon method with ammonium molybdate and ascorbic acid; absorbance at 880 nm; QA/QC samples included.
- Phytoplankton chlorophyll a (TOCA):
  - Filtration, methanol extraction, and spectrophotometric analysis following established protocols.

## Provenance and Funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.
- Data validation supported by NERC through UKCEH National Capability NE/Y006208/1.

## Data Availability and Governance Notes
- Data are provided for download as CSV; 2023 dataset described in detail with accompanying methodological notes.
- As a Data Steward, note the need for:
  - Completing comprehensive quality control and calibration before public sharing.
  - Maintaining metadata richness (method details, calibrations, detection limits, uncertainty).
  - Clear versioning and documentation of updates, given the raw status and ongoing long-term monitoring context.
  - Tracking data provenance, including sampling date, location flag (buoy vs shore), and any deviations from standard procedures.

## References
- Methodological references for chemical analyses and historical context:
  - Mackereth et al. (1978)
  - Mortimer (1981)
  - Talling (1974)