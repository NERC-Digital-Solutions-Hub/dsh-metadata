# ReadMe file for SoilCharacteristics.csv

- This ReadMe documents a soil-characteristics dataset describing the 0-10 cm soil layer from two seasonal field trials (2017-2018) used to monitor greenhouse gas fluxes from sheep urine applied to unimproved pasture.
- Study site: common grazing land in the Carneddau mountain range, Snowdonia National Park, North Wales, UK (53°22'N, 3°95'W; 556 m above sea level).
- Sampling design:
  - Control plots used for characterisation (n=4 per seasonal study).
  - Summer sampling date: 18/07/17; Autumn sampling date: 17/10/17.
  - Soil types: Dystric Histosol (summer) and Humic Gleysol (autumn).
- Purpose: provide baseline soil properties to support interpretation of greenhouse gas flux measurements following sheep urine applications.

## What is included

- Comprehensive soil characterisation data and metadata, with:
  - Bulk density (0-5 cm)
  - Gravimetric soil moisture (as % of dry soil weight)
  - Organic matter content (loss-on-ignition)
  - Soil pH and electrical conductivity (EC)
  - Total soil carbon (TotC) and total soil nitrogen (TotN); carbon-to-nitrogen ratio (CN)
  - Nitrogen mineralisation rate (Nmin)
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN)
  - Microbial biomass carbon (MicC) and microbial biomass nitrogen (MicN)
  - Extractable nitrate (Nitrate), ammonium (Ammonium)
  - Extractable phosphorus (Phos)
  - Exchangeable cations and elements (Na, K, Ca)
- Each variable has a corresponding summer and autumn measurement, with explicit units.

## Methods and procedures

- Analytical framework and QA:
  - All solutions analysed against matrix-matched certified reference standards.
  - Procedural blanks checked for contamination.
  - Data visually checked and subjected to quality assurance procedures.
- Measurement methods (highlights):
  - Bulk density: 100 cm3 metal rings; core dried at 105 °C; stone correction.
  - Gravimetric moisture: oven-dried (105 °C, 24 h).
  - Organic matter: loss-on-ignition (Ball 1964).
  - pH and EC: 1:2.5 soil-to-distilled water suspensions; calibrated with standard buffers.
  - Total C and N: dry soils analysed with TruSpec® (Leco) against standards.
  - N mineralisation: NH4+ measured before/after anaerobic incubation (40 °C, 7 d); KCl extract (1:10); additional 0.5 M K2SO4 extracts for NH4+ and NO3- (Miranda et al. 2001).
  - CHCl3-fumigation-extraction: microbial biomass C and N using 0.5 M K2SO4 extracts; analysed on Multi N/C 2100S; corrections KEC = 0.35, KEN = 0.5.
  - PO4- and exchangeable cations: CH3COOH extraction; phosphate via Murphy & Riley (1962); cations measured with flame photometry.
- Data handling and provenance:
  - All data associated with the dataset are linked to the described methods and references, with explicit data headers and units.

## Data headers and units (structure)

- Data include paired summer and autumn variables, with explicit units such as:
  - BulkDensity_Summer, BulkDensity_Autumn (g cm-3)
  - GravMoist_Summer, GravMoist_Autumn (% of dry soil weight)
  - OrgMatter_Summer, OrgMatter_Autumn (% dry soil weight)
  - pH_Summer, pH_Autumn
  - EC_Summer, EC_Autumn (µS cm-1)
  - TotC_Summer, TotC_Autumn (% dry soil weight)
  - TotN_Summer, TotN_Autumn (% dry soil weight)
  - CN_Summer, CN_Autumn
  - Nmin_Summer, Nmin_Autumn (mg N kg-1 d-1)
  - DOC_Summer, DOC_Autumn (mg C kg-1 soil dry weight)
  - TN_Summer, TN_Autumn (mg N kg-1 soil dry weight)
  - MicC_Summer, MicC_Autumn (g C kg-1 soil dry weight)
  - MicN_Summer, MicN_Autumn (mg N kg-1 soil dry weight)
  - Nitrate_Summer, Nitrate_Autumn (mg NO3--N kg-1 soil dry weight)
  - Ammonium_Summer, Ammonium_Autumn (mg NH4+-N kg-1 soil dry weight)
  - Phos_Summer, Phos_Autumn (mg P kg-1 soil dry weight)
  - Na_Summer, Na_Autumn (mg Na kg-1 soil dry weight)
  - K_Summer, K_Autumn (mg K kg-1 soil dry weight)
  - Ca_Summer, Ca_Autumn (mg Ca kg-1 soil dry weight)
- Each header is tied to its seasonal counterpart, enabling direct season-to-season comparison.

## Data usage notes

- Attribution: Authors must be acknowledged if the data are reused or reproduced (as stated in the ReadMe).
- Context: Data document standard, peer-reviewed–adjacent soil analytical methods and instrumentation (cited refs), enabling reproducibility and benchmarking in environmental monitoring frameworks.

## References (methods and context)

- Ball, D.F. (1964). Loss-on-ignition method for organic matter/carbon in noncalcareous soil.
- Miranda, K.M., Epsey, M.G., & Wink, D.A. (2001). Spectrophotometric detection of nitrate/nitrite.
- Mulvaney, R.L. (1996). Methods of Soil Analysis; nitrogen inorganic forms.
- Voroney, R.P., Brookes, P.C., & Beyaert, R.P. (2008). Soil microbial biomass C, N, P and S; extraction methods.
- Waring, S.A., & Bremner, J.M. (1964). Ammonium production under waterlogged conditions as an index of nitrogen availability.

## Relevance for monitoring frameworks

- Demonstrates a comprehensive, QA-backed suite of soil health indicators relevant to environmental monitoring and policy evaluation.
- Provides explicit metadata, standardized measurement protocols, and clear data provenance, facilitating data integration, comparability, and governance.
- Includes explicit requirements for data attribution and transparent sharing of methodologies and references, aligning with best practices to overcome data silos and improve data usability in decision-making.