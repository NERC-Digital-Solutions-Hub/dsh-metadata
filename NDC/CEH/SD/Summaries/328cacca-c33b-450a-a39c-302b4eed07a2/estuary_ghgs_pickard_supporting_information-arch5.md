# Sampling regime

## Overview
- Conducted at seven UK estuaries: Clyde, Forth, Tay (central Scotland); Conwy, Clwyd (northern Wales); Dart, Tamar (southwest England).
- Four coordinated sampling campaigns: July 2017; October 2017; January 2018; April 2018.
- Aimed to span the salinity gradient and collect greenhouse gas (GHG) and water-chemistry data across estuarine environments.

## Study design and sampling sites
- Sampling locations selected to cover a salinity gradient; target salinities: 1, 2, 5, 10, 15 and >25 ppt (not always achieved).
- For each estuary, six sampling locations were used, starting furthest upstream (freshwater) toward downstream (saline).
- Field sampling logistics included rigid inflatable boats or fixed points (e.g., bridges).

## Field measurements and sampling procedures
- In situ measurements of temperature and salinity at each sample location using a probe placed ~10 cm below the water surface; readings taken with a Hach HQ30D sensor.
- Surface water samples collected in acid-washed buckets at target salinity intervals; bulk water samples split into subsamples for various analyses.
- Sampling point locations varied with salinity, reflecting gradients across each estuary.

## Greenhouse gas sampling and analysis
- Estuarys Clyde, Clywd, Conwy, Forth and Tay:
  - Headspace method with duplicate samples: 40 mL water equilibrated with 20 mL ambient headspace in a syringe; shaken underwater to equilibrate; headspace injected into pre-evacuated 12 mL vials for GC analysis.
  - Ambient air sample collected at each site.
  - GC configuration: FID for CH4 and CO2; μECD for N2O.
- Tamar and Dart estuaries:
  - Gas samples collected in 500 mL borosilicate bottles; overfilled three times to remove air bubbles; poisoned with mercuric chloride prior to GC analysis.
  - GC configuration: CH4 by FID; N2O by ECD; calibration with certified standards traceable to NOAA WMO; temperature equilibrated ~25°C.
- Analytical details:
  - Detection limits: CH4 40 ppb; CO2 5000 ppb; N2O 5 ppb.
  - Concentrations calibrated against standards; solubility calculations using Henry’s Law and temperature/salinity adjustments (Weiss & Price, 1980; related solubility references).

## Water chemistry analyses
- Dissolved organic carbon (DOC) measured at UKCEH using a Shimadzu TOC-L after filtration (0.45 μm); method described in García-Martín et al. 2021.
- Total dissolved carbon (TDC) measured similarly for freshwater samples, including inorganic carbon (with modified step to exclude inorganic carbon for freshwater as needed); LoD 0.6 mg/L C.
- Freshwater nutrients (Position 1; Conwy had extended positions 1–6 on 01/02/2018):
  - Nitrate + nitrite (NO3-N + NO2-N) via Dionex ICS2000 IC; LoD 0.06 mg/L N; QC checks at intervals.
  - Ammonium (NH4-N) via indophenol blue colorimetry; LoD 0.033 mg/L N; calibration and QC procedures described.
  - Total Nitrogen (TN) via Shimadzu TOC-L with TNM-L; LoD 0.08 mg/L N.
  - Total Phosphorus (TP) via K2S2O8 digestion and molybdenum blue colorimetry (SEAL AQ2); LoD 0.008 mg/L P.
  - Soluble reactive phosphorus (PO4-P) via colorimetric SEAL AQ2 with ammonium molybdenum blue chemistry; LoD 0.005 mg/L P.
- Saline nutrients (Positions 2–6; Plymouth Marine Laboratory):
  - Anions (NO3+NO2, etc.), ammonium, phosphate, silicate analyzed by SEAL Analytical AAIII autoanalyser using established GO-SHIP protocols; LoD values provided per analyte.
  - Calibration ranges and QA/QC aligned with GO-SHIP methods.
- Data handling for nutrients follows GO-SHIP/standard methods; seawater analyses have site- and lab-specific considerations.

## Data structure, units, and quality notes
- Data are organized with explicit columns for estuary, position, location coordinates, date, salinity, temperature, and each chemical parameter.
- Units are specified in Table 1 (not reproduced here); common units include mg/L, μM/L, and µM/L as appropriate.
- Missing data:
  - Missing values are marked with an asterisk in the CSV.
  - A large number of missing values arise because saline and freshwater analyses were performed at different laboratories; related columns may be missing while corresponding related columns in other parts of the dataset contain data.
- Data resolution:
  - All values are reported to two decimal places.
- Documentation references:
  - Methods and unit details are supported by the listed references (García-Martín et al., 2021; GO-SHIP protocols; standard GHG and nutrient analyses).

## References (methods and context)
- Becker et al. 2020; Brewer & Riley 1965; García-Martín et al. 2021; Grasshoff 1976; Kirkwood 1989; Mantoura & Woodward 1983; Upstill-Goddard et al. 1996; Weiss & Price 1980; Wiesenburg & Guinasso 1979.