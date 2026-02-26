# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere South Basin, UK, 2023

## Overview
- Part of an ongoing fortnightly monitoring dataset for the Windermere South Basin (Cumbria, England) during 2023.
- Data cover surface temperature, surface oxygen saturation, Secchi depth, water chemistry, and phytoplankton chlorophyll a.
- Data available to download as raw measurements; not yet quality controlled.

## Data Collected (variables and units)
- Surface temperature (TEMP) in degrees Celsius.
- Surface oxygen saturation (OXYG) in % air-saturation.
- Secchi depth (SECC) in metres.
- Alkalinity (ALKA) in micrograms per litre as CaCO3.
- pH (unitless).
- Total ammoniacal nitrogen (NH4N) in micrograms N per litre.
- Total oxidised nitrogen (TON) in micrograms N per litre.
- Soluble reactive phosphate (PO4P) in micrograms P per litre.
- Total phosphorus (TOTP) in micrograms P per litre.
- Dissolved reactive silicon (SIO2) in micrograms SiO2 per litre.
- Phytoplankton chlorophyll a (TOCA) in micrograms per litre.
- Samples are integrated from 0 to 7 m; data are from January to December 2023.
- Values below detection limit are marked with a < sign in the Sign(if<LOD) column.

## Data Structure and Format
- Data provided as a comma-separated values (CSV) file.
- Columns include:
  - sdate: Date of measurement.
  - Variable, Description: Name and description of each measured parameter.
  - Value, Description: Measured value for each variable.
  - Sign(if<LOD), Description: Indicates if a value is below the detection limit.

## Methods (measurement techniques and instruments)
- Temperature and dissolved oxygen:
  - Instrument: YSI ProODO handheld (Xylem Analytics UK).
  - DO reported in mg/L; saturation calculated based on Mortimer (1981).
  - Calibration: daily DO% calibration; biweekly calibration in water-saturated air; bimonthly calibration in air-saturated water.
- Secchi depth:
  - Measured by lowering a Secchi disk on a marked rope.
- Alkalinity and pH:
  - Integrated water sample sealed to prevent atmospheric exchange.
  - Alkalinity and pH measured by Gran titration with a combination electrode (Radiometer GK2401C; Radiometer PHM64); electrode calibrated before each sampling occasion.
- NH4N (ammonium nitrogen):
  - Method: Colourimetric using SEAL AQ2 discrete analyser after filtration (Whatman GF/C).
  - Reagents and conditions produce a blue-green indophenol-like colour; measured at 670 nm.
  - Calibration: automatic dilution from a 2.0 mg/L NH3-N stock; control standards (1.0 mg/L) every 10 samples; UKAS-accredited.
- TON (total oxidised nitrogen):
  - Method: Colourimetric using SEAL AQ2 discrete analyser after filtration.
  - Nitrate reduced to nitrite (hydrazine, alkaline) and colour-coupled reaction measured at 546 nm.
  - Calibration: 0–2.0 mg/L N; control standards every 10 samples; UKAS-accredited.
- Total phosphorus (TP):
  - Digestion: Potassium persulphate digestion under heat/pressure; followed by molybdenum blue colorimetric analysis.
  - Measurement: Absorbance at 880 nm (UV-150-02).
  - Calibration: 0–0.2 mg/L P; blanks and standards used; data blank corrected.
- Dissolved reactive silicon (SIO2):
  - Method: Colorimetric with ammonium molybdate to form silicomolybenum blue; measured at 880 nm.
  - Range: 0–5 mg/L SiO2; QC samples at 2.0 mg/L and 4.0 mg/L every ~20 samples.
- Phytoplankton chlorophyll a (TOCA):
  - Filter known volume through GF/C; pigments extracted with boiling methanol (Talling 1974 method); analysed spectrophotometrically.
- Soluble reactive phosphate (PO4P):
  - Measured colorimetrically (molybdenum blue) after filtration (GF/C); calibration and blanks used.

## Quality Control and Data Validation
- Raw data are not yet quality controlled or calibrated.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered by different people and validated by a database manager; visual checks (line graphs) performed.
- Missing data attributed to weather, equipment limitations, or staff shortage.

## Coverage, Limitations, and Data Use
- Data reflect measurements from a single deepest-water buoy location in the Windermere South Basin.
- Sampling is fortnightly across 2023; data represent a snapshot of surface conditions and linked chemical/biological parameters.
- Users should note the lack of full QC at the time of download; planned data validation and calibration are implied.

## Data Access and Documentation
- Data come with a structured metadata description of each parameter, units, and detection-limit conventions.
- Documentation includes explicit methodological details for replicability and comparison with other sites or years.

## Funding and References
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme.
- Data validation supported by NERC through the UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
- Key references for methods:
  - Mackereth et al. (1978) Water Analysis methods.
  - Mortimer (1981) Oxygen content of air-saturated waters.
  - Talling (1974) In standing waters methods for primary production.