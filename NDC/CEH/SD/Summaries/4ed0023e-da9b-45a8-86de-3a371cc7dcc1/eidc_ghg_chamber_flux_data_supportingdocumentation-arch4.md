# Fluxes of carbon dioxide, nitrous oxide and methane from winter wheat treated with organic and inorganic fertilisers

## Overview
- 2-hourly observations of biogenic fluxes of CO2, N2O, and CH4 from a winter wheat crop on mineral soil in the UK.
- Treatments: i) inorganic fertiliser (IF); ii) pig slurry + inorganic fertiliser (PS); iii) pig slurry treated with plasma-induction + inorganic fertiliser (TPS).
- Measurements span 83 days during the winter wheat growing season (20/03/2022–13/06/2022) using automated GHG flux chambers.
- Data intended to support understanding of how fertiliser treatments influence greenhouse gas fluxes from a field cropping system.

## Study site and experimental design
- Location: University of Leeds Research Farm (coordinates provided).
- Field history: continuous arable rotation since 1970.
- Climate: temperate oceanic.
- Soil: well-drained loamy calcareous brown earth; pH 6.9; bulk density 1.3 g cm^-3.
- Soil C and N (0–30 cm): 39.5 g kg^-1 and 2.3 g kg^-1, respectively.
- Agriculture: rainfed (no irrigation).
- Winter wheat: planted 21/10/2021 at 440 seeds m^-2; harvested 27/07/2022.
- Replication: three replicates per fertiliser treatment (total 9 plots).
- Nutrient input: all treatments received 220–253 kg available N ha^-1.

## Collection methods and fieldwork instrumentation
- Fluxes measured every 2 hours from 20/03/2022 to 13/06/2022.
- Instrumentation: Eosense eosAC-LT chambers and Picarro G2508 analyser.
- Data collection supported by automated field equipment and routine fieldwork.

## Data processing
- Fluxes calculated offline with eos-AnalyzeMX/AC V3.5.0.
- Method: linear fit to raw CO2 concentration to derive fluxes for CO2, N2O, and CH4.

## Quality control
- Outliers identified/removed using a modified Elbers et al. (2011) approach.
- Uncertainty quantified for CO2 fluxes using a combination of threshold (u*), statistical screening, measurement errors, and flux calculation uncertainties.

## Gap-filling
- N2O and CH4: gap-filled by linear interpolation.
- CO2: gap-filled by linear regression, with separate gap-filling for daytime and nighttime data.

## Details of data structure
- File: GHG_chamber_flux_data.csv
- Variables:
  - Date_Time: dd/mm/yyyy HH:MM (GMT) – start time of the 2-hour measurement.
  - Chamber_Number: identifier for chamber.
  - CO2: μmol CO2 m^-2 s^-1 – gap-filled flux.
  - N2O: nmol N2O m^-2 s^-1 – gap-filled flux.
  - CH4: nmol CH4 m^-2 s^-1 – gap-filled flux.
  - Gap_Fill: 1 = observed, 2 = gap-filled.
  - Treatment: IF = inorganic fertiliser; PS = pig slurry + inorganic fertiliser; TPS = treated pig slurry + inorganic fertiliser.

## Usage and potential applications for data leaders
- Enables assessment of how different fertiliser strategies affect biogenic GHG fluxes in winter wheat systems.
- Useful for calculating annual or seasonal flux totals with documented gap-filling approaches.
- Supports data governance practices: explicit metadata, units, measurement timings, and flags for gap-filled data.
- Can inform cross-site or networked data collaborations on agricultural GHG emissions and data interoperability.

## Data provenance and acknowledgements
- Funded by Leeds-York-Hull Natural Environmental Research Council (NERC) Doctoral Training Partnership (DTP) Panorama, grant NE/S007458/1.
- Acknowledgements to field site access, materials, fieldwork assistance, farm management information, and fertiliser management guidance.

## References (as cited in the dataset)
- Barba et al., 2019; Cranfield University, 2018; Dorich et al., 2020; Elbers et al., 2011; Eosense; Lucas-Moffat et al., 2022; Met Office MIDAS data; Petrakis et al., 2017; Picarro.