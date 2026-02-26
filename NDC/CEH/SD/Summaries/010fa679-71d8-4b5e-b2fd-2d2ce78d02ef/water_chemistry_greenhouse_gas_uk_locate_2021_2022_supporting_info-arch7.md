UK water chemistry and greenhouse gas emissions study, LOCATE, 2021-2022: Supporting information

## Overview
- LOCATE is a multidisciplinary NERC project to improve understanding of carbon flow from land to the ocean.
- Field campaign aimed to characterise diurnal greenhouse gas emissions from inland water bodies, considering water body type and seasonality (summer vs winter).
- Method: floating chambers deployed for 24 hours to quantify emitted gases; paired with water chemistry measurements.

## Objectives and scope
- Characterise diurnal GHG emissions from various inland water bodies across the UK.
- Assess how emissions vary with water body type (pond, broad, dyke, loch, stream, wetland) and season.
- Include data collection from July 2021 to March 2022 at diverse sites chosen for geographical and land-type variation.

## Sampling locations and spatial coverage
- Sampling conducted across the UK at ponds, streams, lochs, dykes, broads, and wetlands.
- Site selection aimed for geographical and land-type variation; full site details provided in Table 1 and Figure 1.
- Example locations include Wroxham Broad, Upton Broad/Dyke, Barton Wetland, Hickling Broad, Duddingston Loch, St. Margaret’s Loch, and many others with precise coordinates and sampling dates.

## Field sampling methods
- In-field chemistry: dissolved organic carbon (DOC), total dissolved nitrogen (TdN), total phosphorus (TP), and soluble reactive phosphorus (SRP) collected with a 60 mL syringe; filtration performed for SRP and DOC samples.
- Physicochemical measurements: pH, conductivity, dissolved oxygen (DO) and temperature using a multi-parameter meter; regular calibration performed.
- GHG sampling: floating chambers assembled with floats, modified basins and three-way taps to trap air above water for 24 hours; headspace gas sampling for initial and 24-hour concentrations.
- Duplicate or triplicate chamber deployments at sites; gas samples analyzed by injecting trapped air into pre-evacuated vials.
- Dissolved GHGs (CH4, CO2, N2O) measured from water using headspace sampling at the start and end of the 24-hour period.

## Sample storage and handling
- TP, SRP and spare filtered samples frozen at -18°C until batch analysis.
- DOC/TdN/UV-Vis samples kept at 4°C and analysed within a week or as soon as possible.
- GHG samples stored at room temperature until analysis.

## Laboratory analyses
- DOC/TdN: Shimadzu TOC-LCPH analyser with TNM unit; calculates non-purgeable organic carbon (NPOC) as DOC after acidification and sparging.
  - Calibration and quality controls include NPOC and TdN standards, blanks, and duplicate measurements with outliers removed.
- UV/Vis (SUVA): Absorbance from 230–800 nm; SUVA254 calculated to indicate DOC aromaticity.
- Total Phosphorus (TP) and Soluble Reactive Phosphorus (SRP): SEAL AQ2 Discrete analyser; TP after potassium persulfate digestion; SRP via colorimetric molybdate-blue method.
- Greenhouse gases: Gas chromatography (Agilent 7890B) with μECD for N2O and FID for CH4/CO2; concentrations calibrated against mixed standards; results in ppmv converted to µg/L using Henry’s law.
- All analyses referenced standard methods and calibration procedures described in the dataset documentation.

## Data structure and content
- Dataset name: MERLIN 2022-2023 dataset structure described.
- Data organization:
  - Columns A–F: sampling information (Site_name, Site_type, Date, Latitude, Longitude, Time).
  - Columns G–M: field physicochemical measurements (Conductivity, Conductivity_temp, pH, pH_temp, DO, DO_temp, Temp_av, Chambers).
  - Columns O–AD: laboratory analysis results (DOC, TdN, C_N, Abs_at_254, SUVA, TP, SRP, CH4_C, CO2_C, N2O_N, Chamber_CH4_C_time_0, Chamber_CH4_C_time_24, Chamber_CO2_C_time_0, Chamber_CO2_C_time_24, Chamber_N2O_N_time_0, Chamber_N2O_N_time_24).
- Units and descriptions provided in Table 3 (e.g., µS/cm for conductivity, mg/L for DO, °C for temperatures, mg/L for DOC/TdN/TP/SRP, µg/L for CH4_C/ N2O_N, and ppmv for dissolved gas concentrations).

## Data quality and completeness
- Data completeness and exclusions documented in Table 4.
- Exclusions largely due to issues such as time not recorded, missing DO_temp, sample contamination, or missing samples.
- Examples include exclusions at Auchencorth Pond, Hoveton Broad, Dunsapie Loch, St Margaret’s Loch, Bush Estate Pond, and others for specific determinants (e.g., pH, DO_temp, CH4_C, CO2_C, N2O_N).

## GIS and data use considerations
- Rich, spatially explicit dataset with site-level coordinates, site type, sampling dates, and times suitable for map-based visualization and spatial analysis.
- Data supports comparisons across water body types and seasons, and integration with other geographic/environmental layers.
- Important considerations for GIS use:
  - Some data points excluded due to QA issues; account for missing/NA values.
  - Multi-institutional data origin implies potential differences in metadata standards; ensure harmonization when merging with other GIS datasets.
  - Figure 1 provides a map of all sampling sites; Table 1 contains full site details.

## Acknowledgements
- Acknowledgement of permissions and sampling access from Norfolk Wildlife Trust, Historic Environment Scotland, Scottish Wildlife Trust, and Dŵr Cymru Welsh Water.

## References
- Dawson et al. (1995) and Weishaar et al. (2003) cited for methodological context on GHG and SUVA calculations.