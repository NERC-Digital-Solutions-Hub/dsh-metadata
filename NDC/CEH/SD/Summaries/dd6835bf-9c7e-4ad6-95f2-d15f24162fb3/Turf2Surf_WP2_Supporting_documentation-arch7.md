# Turf2Surf WP2 Supporting documentation for data

## Overview
- Project focus: Turf2Surf investigates coupled nutrient cycling in terrestrial and freshwater ecosystems, linking nitrogen and phosphorus impacts to carbon exchange, water quality, biodiversity, and related processes.
- WP2 objective: Study nitrogen and phosphorus related impacts on land–atmosphere carbon exchange; information intended to support data integration and modeling efforts (e.g., parameters for JULES).

## Study Area
- Location: Conwy catchment, North Wales, ~500 km2.
- Characteristics: Diverse landscapes with climatic gradient (precipitation from ~500 mm to >1000 mm; Snowdonia mountains up to 1064 m). Habitats range from blanket bogs, montane/moorland, conifer plantations, grasslands, lakes/reservoirs, floodplains to salt marshes.
- Stakeholders: Water industries, shell fisheries, farmers/foresters, tourism, conservation groups, local communities.
- Data visualization: Figure 1 maps sampling locations across the catchment.

## Habitats, Sampling Sites, and Design
- Coverage: 17 soil habitats across sampling sites 1–21 (with some site groupings for soil analysis; several sites include multiple plots).
- Habitat examples: blanket bog, valley bogs, heather on blanket bog, conifer woodland, lowland mixed deciduous woodlands, upland oakwood, hay meadow, improved/semi-improved grasslands, arable (barley), montane vegetation.
- Sampling detail: Table 1 lists habitat type, number of plots per site, and dominant plant species where applicable.
- Spatial and temporal scope: Sampling undertaken across multiple years (notably 2013–2016 for various measurements).

## Measurements and Data Processing (Methods)
- 3.1.1 Aboveground Net Primary Productivity (NPP) and Biomass
  - Annual NPP measured for dominant species at all sites (4 plots per site) between 2013–2015.
  - Biomass: 10 of 17 sites measured; methods differ by habitat (grassland/bog vs woodland).
  - Process: Winter clipping, exclusion of grazers where applicable, drying and weighing; biomass calculations include tree components in woodland plots.
  - Connection: NPP data integrated with ecosystem processes and JULES model parameters.
- 3.1.2 Plant Photosynthesis Measures
  - Parameters: Asat, Vcmax, Jmax (25°C) for dominant species.
  - Field and lab approaches: CO2 response curves using CIRAS-I and LICOR equipment, with temperature corrections and model fitting (Farquhar framework).
  - Data handling: Calculations and processing linked to JULES via published scripts (GitHub mdekauwe/FitFarquharModel).
- 3.1.3 Leaf Traits and Plant Community Traits
  - Traits measured: leaf N and P, leaf dry matter content (LDMC), specific leaf area (SLA), leaf mass per area (LMA), canopy height, bryophyte cover.
  - Procedure: Leaf sampling around measurement sites; LMA from scanned leaves; chemical analyses for N and P.
- 3.2.1 General Soil Measures
  - Sampling: Intact soil cores to 1 m depth from 17 habitats; cores divided into depth intervals (0–15 cm up to 90+ cm).
  - Measurements: Soil water content (SWC), bulk density (BD), loss on ignition (LOI and LOI-C), pH, electrical conductivity (EC), total C and N (C_tot, N_tot).
  - QA/QC: Detailed protocols and calibration steps; multiple personnel involved across sites.
- 3.2.2 Phosphorus (P) Fractions
  - Olsen P, Root P (CaCl2 extraction), Complex-P (citric acid extractable P), Enzyme-P (phosphatase and phytase activity), and Proton-P (1 M HCl) fractions.
  - Analysis: Colorimetric Malachite Green method; 96-well plate assays; standard curves for concentration calculations.
- 3.2.3 Available Carbon and Nitrogen
  - Soil available C and N measured via 0.5 M K2SO4 extraction; subsequent analyses for DOC and TDN (using CEH Bangor procedures).
  - Nitrate and Ammonium analyses: Standard colorimetric methods with microplate readers.
- 3.2.4 Soil Available Cations (Ca, Na, K)
  - Extraction: 0.5 M acetic acid; cation concentrations measured with a flame photometer.
- 3.2.5 Root Biomass
  - Aboveground and belowground biomass: 15 cm soil cores; root separation into >2 mm and <2 mm; root scanning (WinRhizo) for biomass, length, and diameter; oven-dried biomass determination.
  - In-growth cores: Root growth monitored using buried tubes and subsequent root retrieval and analysis.
- 3.2.6 Soil Elements (TXRF)
  - Total elemental analysis (Al, Fe, Ca, K, etc.) across 17 sites using TXRF (S2 PICOFOX Bruker).
  - Sample prep: Drying, grinding, suspension in TritonX, deposition on discs for TXRF analysis.
  - Note: Limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.

## Data Processing, Integration, and Accessibility
- JULES integration: WP2 aims to embed measured plant and soil nutrient parameters into JULES (land-surface model).
- Scripts and tools: Photosynthesis data processed via De Kauwe model scripts; data processing handled by CEH Bangor and Bangor/Exeter teams.
- QA/QC: Multiple QA/QC steps implied through collaborative data processing; TXRF limitations documented in a separate file.

## Dataset Structure and File Descriptions
- The data are provided as five CSV files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common structure across files:
  - Column A: Site number (as per Table 1).
  - Column B: Habitat name.
  - Column C: Habitat description.
  - Column D: Site name.
  - Column E: Ecosystem Component (Plant, Soil, Roots).
  - Column F: If Plant, the specific plant species; otherwise NA.
  - Column G: Plot number (1–4).
  - Column H: Replicate number (used when measurements are not co-located with plots).
  - Column I: Soil depth interval (for Soil and Roots components).
- Missing data: Represented as NA where data are restricted or not available.
- Spatial and temporal relevance: Data are designed to support geospatial mapping of habitats, plots, and depth-resolved soil properties; suitable for GIS-based visualization and integration with ecosystem models.

## Authors, Versions, and Access
- Project members: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch.
- Authors (document): Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart.
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- Data scope: Datasets cover Conwy catchment ecology, biogeochemistry, and hydrology, with extensive documentation and methodological details for reuse and integration into data products and GIS workflows.