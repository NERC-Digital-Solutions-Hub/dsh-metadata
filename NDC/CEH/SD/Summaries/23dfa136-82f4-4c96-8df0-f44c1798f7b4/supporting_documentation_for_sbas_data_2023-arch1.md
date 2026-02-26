# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Windermere South Basin, UK, 2023

- Purpose and scope
  - Ongoing fortnightly monitoring dataset for Windermere South Basin, Cumbria, England (0–7 m integrated water samples).
  - Focus on surface temperature (TEMP, °C), surface oxygen saturation (OXYG, % air-saturation), Secchi depth (SECC, m), alkalinity (ALKA, µg CaCO3 L−1), pH, and nutrients and pigments: NH4N, TON, PO4P, TOTP, SIO2, TOCA (all in µg L−1 where applicable, except TEMP and SECC in their units).
  - Data cover January–December 2023 and are downloadable as CSV.

- Data variables and units
  - TEMP: surface temperature, °C
  - OXYG: dissolved oxygen saturation, % air-saturation
  - SECC: Secchi depth, m
  - ALKA: alkalinity, µg CaCO3 L−1
  - pH: measured pH
  - NH4N: total ammoniacal nitrogen, µg N L−1
  - TON: total oxidised nitrogen, µg N L−1
  - PO4P: soluble reactive phosphate, µg P L−1
  - TOTP: total phosphorus, µg P L−1
  - SIO2: dissolved reactive silicon (SiO2), µg L−1
  - TOCA: phytoplankton chlorophyll a, µg L−1
  - Sampling integrates from 0 to 7 m; measurements taken from a boat at a designated buoy in the deepest basin area.

- Sampling regime and site specifics
  - Fortnightly sampling schedule.
  - Location: South Basin of Windermere, UK.
  - Instruments and field protocol emphasize consistent sampling depth and in-situ measurements complemented by lab analyses.

- Measurement methods and calibration
  - Temperature and dissolved oxygen: YSI ProODO handheld instrument; DO% calibrated daily; oxygen saturation calculated from Mortimer (1981) model; regular biweekly and bimonthly calibrations for DO% in air-saturated conditions.
  - Secchi depth: Secchi disk with measured rope.
  - Alkalinity and pH: integrated sample sealed to prevent atmospheric exchange; Gran titration with a combination electrode; electrode calibration before sampling.
  - NH4N and TON: SEAL AQ2 discrete analyser after filtration; colorimetric detection with standard calibration curves; UKAS-accredited methods; QC includes control standards and duplicates.
  - TP: digestion with potassium persulphate and subsequent molybdenum blue colorimetric analysis; UV-Vis measurement at 880 nm; standards and reference materials used for accuracy; blank-corrected.
  - SIO2: colorimetric silica assay with ammonium molybdate and ascorbic acid; measurement at 880 nm; QC with mid-range standards.
  - TOCA: filtration, methanol extraction, and spectrophotometric pigment analysis per established protocol.
  - All methods aligned with established limnology practices and quality controls; UKAS accreditation applied to supported analyses.

- Data quality and control
  - Data presented here are raw and have not yet undergone full quality control and calibration.
  - TEMP, OXYG, SECC, ALKA, pH, PO4P, and TOCA have undergone double-entry by separate operators and initial validation; data visuals checked by database manager.
  - Missing data attributed to weather, equipment limitations, or staff availability.
  - Some values are below detection limits, indicated with a "<" sign in the dataset.

- Data structure and accessibility
  - Data delivered as comma-separated values (CSV) with columns:
    - sdate: measurement date
    - Variable: description of the parameter
    - Value: measured value
    - Sign(if<LOD): indicator for measurements below detection limit
  - Data preparation notes emphasize traceability: data provenance, calibration notes, and aging handling are applicable for subsequent analyses.

- Limitations and considerations for analysis
  - Raw, not fully quality-controlled dataset; incorporate QC steps before formal analysis.
  - Potential gaps due to weather or operational issues; consider imputation or sensitivity analyses for missing periods.
  - Localized sampling in the deepest part of the lake; caution when extrapolating to broader Windermere basins.

- Funding and references
  - Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme.
  - Validation supported by NERC through UKCEH National Capability NE/Y006208/1.
  - Methodological references include Mackereth et al. (1978), Mortimer (1981), and Talling (1974).