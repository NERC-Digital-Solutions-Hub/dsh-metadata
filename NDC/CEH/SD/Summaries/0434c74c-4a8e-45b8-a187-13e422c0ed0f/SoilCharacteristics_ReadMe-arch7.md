# SoilCharacterstics.csv read me file

## Overview
- Describes the characteristics of Orthic Podzol soil sampled twice in the year (spring and autumn) during 2016–2017 field trials.
- Purpose: monitor greenhouse gas emissions from sheep urine applied to a semi-improved pasture.
- Field located at Henfaes Research Station, North Wales; 270 m above sea level, slope 13%.
- Experimental design includes 4 replicates from control plots within spring and autumn trials.

## Site and sampling context
- Location coordinates: 53°13'N, 4°0'W.
- Soil sampling depths: 0–5 cm (bulk density) and 0–10 cm (other properties).
- Seasonal factors: spring (SP) and autumn (AT) measurements for each property.
- Replication: 4 replicates per seasonal plot (control plots).

## Measurements and key variables
- Physical properties:
  - BD_SP, BD_AT: Bulk density (g cm-3), 0–5 cm, dry weight basis; corrected for stones.
  - Gravmoist_SP, Gravmoist_AT: Gravimetric moisture content (%), 0–10 cm, dry weight basis.
- Soil organic matter:
  - Orgmat_SP, Orgmat_AT: Organic matter (% of dry soil weight).
- Chemical properties (pH, EC, C, N, CN, etc.):
  - pH_SP, pH_AT: Soil pH (0–10 cm).
  - EC_SP, EC_AT: Electrical conductivity (µS cm-1) (0–10 cm).
  - C_SP, C_AT: Total carbon (% dry soil weight) (0–10 cm).
  - N_SP, N_AT: Total nitrogen (% dry soil weight) (0–10 cm).
  - CN_SP, CN_AT: Carbon-to-nitrogen ratio (0–10 cm).
- Nitrogen dynamics:
  - Nmin_SP, Nmin_AT: Nitrogen mineralisation rate (mg N kg-1 day-1) (0–10 cm).
  - Nitrate_SP, Nitrate_AT: Extractable nitrate (mg NO3--N kg-1 soil) (0–10 cm with 0.5 M K2SO4 extract).
  - Ammon_SP, Ammon_AT: Extractable ammonium (mg NH4+-N kg-1 soil) (0–10 cm with 0.5 M K2SO4 extract).
- Dissolved organic carbon and nitrogen:
  - DOC_SP, DOC_AT: 0.5 M K2SO4-extractable dissolved organic carbon (mg C kg-1 soil).
  - TDN_SP, TDN_AT: 0.5 M K2SO4-extractable total dissolved nitrogen (mg N kg-1 soil).
- Inorganic nutrients (phosphorus and cations) with specific extracts:
  - Phosph_SP, Phosph_AT: 1 M acetic acid extractable phosphate (mg PO4--P kg-1 soil).
  - Na_SP, Na_AT: Extractable sodium (mg Na kg-1 soil).
  - K_SP, K_AT: Extractable potassium (mg K kg-1 soil).
  - Ca_SP, Ca_AT: Extractable calcium (mg Ca kg-1 soil).
- Notes: All values are reported with corresponding depth and season; many measurements are on a dry soil weight basis and/or use specific extractants.

## Methods and quality assurance
- Bulk density: determined with 100 cm3 metal rings; cores oven-dried; stones removed; values corrected for stone weight/volume.
- Gravimetric moisture: oven-dried at 105 °C for 24 h.
- Organic matter: determined by loss-on-ignition (Ball 1964).
- pH and EC: 1:2.5 soil-to-distilled water suspensions; calibrated with standard buffers.
- Total C and N: measured with TruSpec® Analyzer (Leco) against reference standards.
- N mineralisation: method of Waring and Bremner (1964); NH4+ by Mulvaney (1996); 1.0 M KCl extracts (1:10 w/v).
- Additional extracts: 0.5 M K2SO4 (for NH4+, NO3-, and DOC/TDN); CHCl3 fumigation for microbial biomass C/N (Voroney et al. 2008) with KEC/KEN corrections.
- Phosphorus and cations: 1 M acetic acid extract for PO4--P and cations; measurements by standard methods (Murphy & Riley 1962; flame photometer for cations).
- Quality assurance: all solutions analyzed against matrix-matched certified references; procedural blanks used; data visually inspected for QA.

## Data structure and interpretation notes
- Headers indicate season (SP = spring, AT = autumn) and depth (0–5 cm or 0–10 cm) for each parameter.
- Values are typically expressed per dry soil weight basis; BD values corrected for stones.
- Data are intended for GIS applications to map spatial and seasonal variation in soil properties.

## References
- Ball, D.F. (1964). Loss-on-ignition as a proxy for organic matter in noncalcareous soils.
- Miranda, K.M. et al. (2001). Nitrate/nitrite detection method.
- Mulvaney, R.L. (1996). Inorganic N forms (in Methods of Soil Analysis).
- Voroney, R.P. et al. (2008). Soil microbial biomass and related measurements.
- Waring, S.A., Bremner, J.M. (1964). Ammonium production under waterlogged conditions.

## Attribution
- Authors must be acknowledged if the data are reused or reproduced.