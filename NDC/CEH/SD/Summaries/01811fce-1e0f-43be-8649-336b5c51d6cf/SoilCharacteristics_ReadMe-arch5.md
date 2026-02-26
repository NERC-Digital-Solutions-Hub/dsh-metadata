# ReadMe file for SoilCharacteristics.csv

## Overview
- Describes soil characteristics from two seasonal field trials (2017-2018) used to monitor greenhouse gas fluxes from sheep urine applied to an unimproved pasture.
- Location: common grazing land in the Carneddau mountain range, Snowdonia National Park, North Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Sampling design: soil samples (0–10 cm; n = 4) taken from the control plots of each seasonal study on two dates (18/07/17 for summer plots; 17/10/17 for autumn plots).
- Soils identified as Dystric Histosol (summer) and Humic Gleysol (autumn).
- Focus on characterising soil properties to support interpretation of greenhouse gas flux measurements.

## Data Collected (Variables and Structure)
- Measurements cover bulk density, moisture, organic matter, fertility, carbon and nitrogen pools, mineralisation, dissolved and microbial parameters, and exchangeable nutrients.
- Data headers are split by season suffixes: Summer and Autumn (e.g., BulkDensity_Summer, pH_Autumn, Nmin_Summer).
- Key variables include (with units described in the header list):
  - BulkDensity, GravMoist (bulk density and gravimetric moisture; g cm-3 and % of dry soil weight)
  - OrgMatter, TotC, TotN, CN (organic matter, total carbon, total nitrogen, carbon-to-nitrogen ratio)
  - pH, EC (electrical conductivity; units µS cm-1)
  - Nmin (N mineralisation rate; mg N kg-1 d-1)
  - DOC, TN (dissolved organic carbon, total dissolved nitrogen; mg C or N kg-1 soil dry weight)
  - MicC, MicN (microbial biomass C and N; g C kg-1 and mg N kg-1 soil dry weight)
  - Nitrate, Ammonium (extractable nitrate and ammonium; mg NO3--N or NH4+-N kg-1 soil dry weight)
  - Phos (phosphorus; mg P kg-1 soil dry weight)
  - Na, K, Ca (exchangeable cations; mg per kg soil dry weight)
- Documentation notes that all data were checked visually for quality assurance and compared against matrix-matched certified standards; procedural blanks were used where appropriate.

## Methods and Measurements (Procedures and Instruments)
- Sampling and preparation
  - Soil samples collected from control plots at 0–10 cm depth; cores processed by oven-drying, sieving, and correcting bulk density for stone content.
- Physical and chemical analyses
  - Bulk density: 100 cm3 metal rings; oven-drying at 105 °C; corrections for stones.
  - Gravimetric moisture: oven-drying at 105 °C for 24 h.
  - Organic matter: loss-on-ignition at 450 °C for 16 h.
  - pH and EC: 1:2.5 soil-to-distilled water suspensions; standard electrode measurements.
  - Total C and N: analysis with TruSpec® (Leco Corp.) against reference standards.
- Nutrient cycling and extractants
  - N mineralisation: based on Waring and Bremner (1964); NH4+ measured by Mulvaney (1996) before and after anaerobic incubation (40 °C, 7 d) in 1.0 M KCl extract (1:10 w/v).
  - N and P extracts: 0.5 M K2SO4 extraction (1:5); NH4+ and NO3- quantified by described methods.
  - Microbial biomass and organic C/N: CHCl3 fumigation-extraction (Voroney et al., 2008); extracts measured with 0.5 M K2SO4 before/after fumigation; KEC and KEN corrections (0.35 and 0.5).
  - PO4 and cations: final extraction with 1.0 M CH3COOH (1:5); PO4- measured by Murphy and Riley (1962); Na, K, Ca by flame photometry (Sherwood Model 410).
- Standards and QA
  - All solutions measured against matrix-matched certified reference standards.
  - Procedural blanks run to check for contamination.
  - Data subjected to quality assurance checks.

## Data Headers, Units, and Documentation
- Comprehensive headers provided for both Summer and Autumn datasets, including:
  - BulkDensity_Summer, BulkDensity_Autumn (g cm-3; dry soil weight basis)
  - GravMoist_Summer, GravMoist_Autumn (% of dry soil weight)
  - OrgMatter_Summer, OrgMatter_Autumn (% of dry soil weight)
  - pH_Summer, pH_Autumn
  - EC_Summer, EC_Autumn (µS cm-1)
  - TotC_Summer, TotC_Autumn (% of dry soil weight)
  - TotN_Summer, TotN_Autumn (% of dry soil weight)
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
- Units are specified alongside headers to support data consistency and interoperability.

## Data Use, Provenance, and Attribution
- Authors must be acknowledged if the data are reused or reproduced.
- The dataset provides a detailed methodological framework and reference standards to support reproducibility and validation.
- Provenance is documented through explicit references for each method and instrument used, enabling traceability of measurements.

## Context for Data Stewardship
- The dataset exemplifies a rich, multi-parameter soil characterization effort aligned with monitoring greenhouse gas processes.
- Suitable for integration into larger data portals, given the explicit metadata, standardized units, and clear QA procedures.
- Highlights common stewardship challenges noted in the archetype, such as aligning metadata to user needs and ensuring interoperability across studies (two seasons with different soil types).