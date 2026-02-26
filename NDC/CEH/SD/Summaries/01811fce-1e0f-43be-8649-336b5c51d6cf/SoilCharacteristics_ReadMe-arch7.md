# ReadMe file for SoilCharacteristics.csv

## Overview
- Describes soil characteristics from two seasonal field trials (2017-2018) used to monitor greenhouse gas fluxes from sheep urine on unimproved pasture.
- Study area: common grazing land in the Carneddau mountain range, Snowdonia National Park, North Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Data collected from control plots to characterise soil attributes; supports map-based data visualisation and analysis of spatial and temporal soil properties.

## Study Area and Sampling Design
- Sampling dates: summer plots on 18/07/17 and autumn plots on 17/10/17.
- Soil types: Dystric Histosol (summer) and Humic Gleysol (autumn).
- Depths and samples: 0-10 cm soil, n = 4 per seasonal study.
- Bulk density measured for 0-5 cm using 100 cm3 rings; corrections applied for stone weight/volume.
- Data quality: procedural blanks and certified standards used where appropriate; QA checks performed.

## Measured Variables and Units
- BulkDensity_Summer, BulkDensity_Autumn: g cm-3 (soil bulk density, 0-5 cm)
- GravMoist_Summer, GravMoist_Autumn: % (gravimetric soil moisture)
- OrgMatter_Summer, OrgMatter_Autumn: % (organic matter by loss-on-ignition)
- pH_Summer, pH_Autumn: pH (soil-water suspensions)
- EC_Summer, EC_Autumn: µS cm-1 (electrical conductivity)
- TotC_Summer, TotC_Autumn: % (total soil carbon)
- TotN_Summer, TotN_Autumn: % (total soil nitrogen)
- CN_Summer, CN_Autumn: (carbon-to-nitrogen ratio)
- Nmin_Summer, Nmin_Autumn: mg N kg-1 d-1 (N mineralisation rate)
- DOC_Summer, DOC_Autumn: mg C kg-1 soil dry weight (dissolved organic carbon)
- TN_Summer, TN_Autumn: mg N kg-1 soil dry weight (total extractable dissolved nitrogen)
- MicC_Summer, MicC_Autumn: g C kg-1 soil dry weight (microbial biomass C)
- MicN_Summer, MicN_Autumn: mg N kg-1 soil dry weight (microbial biomass N)
- Nitrate_Summer, Nitrate_Autumn: mg NO3--N kg-1 soil dry weight (extractable nitrate)
- Ammonium_Summer, Ammonium_Autumn: mg NH4+-N kg-1 soil dry weight (extractable ammonium)
- Phos_Summer, Phos_Autumn: mg P kg-1 soil dry weight (extractable phosphate)
- Na_Summer, Na_Autumn: mg Na kg-1 soil dry weight (exchangeable sodium)
- K_Summer, K_Autumn: mg K kg-1 soil dry weight (exchangeable potassium)
- Ca_Summer, Ca_Autumn: mg Ca kg-1 soil dry weight (exchangeable calcium)

## Laboratory Methods and References
- Bulk density: core method with correction for stones.
- Gravimetric moisture: oven-drying at 105 °C (24 h).
- Organic matter: loss-on-ignition (Ball 1964).
- pH and EC: 1:2.5 soil-to-distilled water suspensions, calibrated with standards.
- C and N: total carbon and nitrogen by TruSpec analyzer against reference standards.
- N mineralisation: based on Waring and Bremner (1964); NH4+ measured before/after anaerobic incubation.
- Extractants: 0.5 M K2SO4 for NH4+/NO3-, CHCl3-FE for microbial biomass C/N, 1.0 M CH3COOH for PO4- and exchangeable cations.
- Analyses: matrix-matched certified reference standards; procedural blanks to check for contamination.
- References: Ball (1964), Miranda et al. (2001), Mulvaney (1996), Voroney et al. (2008), Waring & Bremner (1964).

## Data Quality, Standards, and Documentation
- Data visually checked and subjected to quality assurance.
- Use of matrix-matched standards and blanks to ensure accuracy and detect contamination.
- All data headers and units explicitly defined to enable proper interpretation and GIS mapping.
- Authors must be acknowledged if data are reused or reproduced.

## Usage Notes for GIS Applications
- The dataset provides a suite of soil physical, chemical, and biological properties suitable for spatial and temporal GIS analyses.
- Can support mapping of soil fertility, carbon and nitrogen pools, moisture regimes, and potential drivers of greenhouse gas fluxes in pasture systems.
- Ensure proper handling of seasonal comparisons (summer vs autumn) and soil type differences (histosol vs gleysol) during analysis and visualization.