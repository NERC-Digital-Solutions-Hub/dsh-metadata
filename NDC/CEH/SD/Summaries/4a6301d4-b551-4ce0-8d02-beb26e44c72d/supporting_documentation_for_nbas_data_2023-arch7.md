# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere North Basin, UK, 2023.

## Overview
- Fortnightly monitoring dataset from Windermere North Basin, Cumbria, England, covering January to December 2023.
- Variables collected: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammoniacal nitrogen (NH4N), total oxidised nitrogen (TON), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Data provided for download as CSV with date-stamped measurements and accompanying metadata (detection limits and sampling location flags).

## Variables and units
- TEMP: degrees Celsius
- OXYG: % air-saturation
- SECC: metres
- ALKA: µg CaCO3 per litre
- pH: (no unit specified)
- NH4N: µg N per litre
- TON: µg N per litre
- PO4P: µg P per litre
- TOTP: µg P per litre
- SIO2: µg per litre (as SiO2)
- TOCA: µg per litre
- Sign(if<LOD): indicates below detection limit with a "<" sign
- Flag: sampling location indicator (1 = buoy at marked location; 2 = shore sampling when buoy visit not possible)

## Sampling regime and location
- Part of an ongoing monitoring program with integrated water samples (0–7 m depth).
- Primary sampling at a marked buoy (deepest part of the lake); if buoy visit not possible, shore sampling was conducted (beginning 2023 onward).
- Data collection method: fortnightly measurements throughout 2023.

## Data structure and access
- Data delivered as comma-separated values (CSV).
- Columns include:
  - sdate: measurement date
  - Description: variable name and description (e.g., TEMP, OXYG, etc.)
  - Value: measured value for each variable
  - Sign(if<LOD): indicator if value is below detection limit
  - Flag: sampling location indicator (1 or 2)

## Quality control and data status
- These are raw data and have not yet been quality controlled and calibrated.
- TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have been double-entered from field notebooks/lab sheets and validated visually by a database manager.
- Missing data occur due to weather, equipment limitations, or staff shortages.
- Data status: some QC performed, but full calibration and formal QC procedures are not completed at time of reporting.

## Methods (instrumentation and analyses)
- Temperature and oxygen: measured with YSI ProODO; oxygen expressed as mg/L and % saturation; regular calibration and checks against standards.
- Secchi depth: measured with a Secchi disk on a labeled rope.
- Alkalinity and pH: integrated 0–7 m water sample; Gran titration with a calibration electrode; analyses performed with standard calibration.
- Nitrogen species (NH4N, TON): measured colorimetrically using SEAL AQ2 with filtration; method details and UKAS accreditation noted.
- Phosphorus (TP): digestion with potassium persulphate followed by molybdenum blue colorimetric analysis; UV/visible spectrophotometer used.
- Dissolved reactive silicon (SIO2): colorimetric method using ammonium molybdate and ascorbic acid; read at 880 nm; QC samples included.
- Phytoplankton chlorophyll a (TOCA): extraction and spectrophotometric analysis after filtration.
- Foundational references and standard methods cited (e.g., Mackereth et al., Mortimer, Talling); methods are UKAS-accredited for some analyses.

## Data provenance and funding
- Data collection supported by Natural Environment Research Council (NERC award NE/R016429/1) as part of the UK-SCaPE programme.
- Data validation supported by NERC through UKCEH National Capability for UK Challenges Programme NE/Y006208/1.
- References include established standard methods for freshwater analysis.

## GIS relevance and considerations
- The dataset is designed for map-based visualization of temporal changes across multiple water quality parameters.
- Strengths: date-stamped, multi-parameter measurements; clear sampling regime (buoy-based with shore fallback); raw data with notes on detection limits and sampling location.
- Considerations for GIS use:
  - Spatial mapping is constrained by limited explicit coordinates; buoy location is known conceptually, but precise coordinates are not provided in the summary. Additional georeferencing would be needed for precise GIS mapping.
  - Data are at 2023 Fortnightly intervals; users may need to aggregate by date or depth integration (0–7 m) for thematic maps.
  - Quality status: data are largely raw with partial QC; for authoritative map products, incorporate planned QC/calibration when available.
  - The “Flag” variable enables basic spatial differentiation between buoy-based and shore-based samples, useful for initial GIS layering pending exact geolocations.