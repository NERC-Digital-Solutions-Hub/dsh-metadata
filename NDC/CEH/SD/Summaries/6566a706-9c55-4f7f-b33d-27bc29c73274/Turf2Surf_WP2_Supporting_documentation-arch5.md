# Turf2Surf WP2 Supporting documentation for data

## Overview
- The Turf2Surf project examines coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- WP2 aims to link plant and soil nutrients to ecosystem processes and to inform data integration with the JULES model.
- Project members and authors are listed, with versioned documentation dated 2016.

## Data governance and stewardship notes
- Data responsibilities are assigned to specific researchers for each data subset (e.g., NPP, photosynthesis, leaf traits, soils, TXRF, etc.).
  - NPP and data processing: Simon Smart
  - Plant photosynthesis measures: Lina Mercado
  - Leaf traits and plant community traits: Lina Mercado and Simon Smart
  - General soil measures, available carbon and nitrogen, soil cations, root biomass, TXRF: Helen Glanville and collaborators
- Documentation includes methodological details, QA/QC notes, and links to code and standard references.
- Data are structured to support cross-site comparisons and integration into JULES; measurements span 2013–2016 and cover the Conwy catchment.

## Study area and sampling
- Location: Conwy catchment, North Wales (~500 km²), with diverse habitats and a climatic gradient.
- Habitats sampled include blanket bogs, moorland, grasslands (including improved and semi-improved), woodlands, lakes, reservoirs, flood plains, and salt marshes.
- Sampling sites and plots are documented with site numbers and descriptions; multiple plots per habitat were used to capture variability.

## Dataset structure and files
Five data files comprise the dataset:
- Turf2Surf_Plant_biomass_data.csv
- Turf2Surf_Plant_structural_data.csv
- Turf2Surf_Plant_physiological_data.csv
- Turf2Surf_Soil_Carbon_data.csv
- Turf2Surf_Soil_raw data.csv

Key schema details:
- Column A: Site number (aligns with Table 1 in the document)
- Column B: Habitat
- Column C: Habitat description
- Column D: Site name
- Column E: Ecosystem Component (Plant, Soil, or Roots)
- Column F: If Plant, the specific plant species; otherwise NA
- Columns G and H: Plot number (1–4) and Replicate number
- Column I: Soil depth interval (for Soil and Roots); NA otherwise
- Missing values are indicated as NA and reflect restricted depths, limited replicates, or data not available

## Data content and methods by component

- 1.0 Information about the Conwy catchment
  - Description of catchment size, landscape variety, stakeholders, and purpose for providing baseline data for process studies.

- 2.0 Habitats and sampling sites
  - Table of habitats with unique site numbers, plots, and dominant plant species.
  - Sites include blanket bogs, conifer woodland, various grasslands, upland oakwood, broadleaved woodlands, montane sites, and arable or downstream agricultural areas.

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - NPP measured annually 2013–2015 for dominant species at each site (four plots per site).
  - Winter clipping and grazing exclusion (where applicable); biomass measured in lab after drying; for woodland/shrub habitats, different methods used (e.g., tree cores, litter).

- 3.1.2 Plant photosynthesis measures
  - Parameters measured: Asat, Vcmax, Jmax (25°C) for dominant species.
  - Field measurements with CIRAS-I and Licor systems at various CO2/conductance conditions; data processed with Farquhar-based models and temperature corrections.
  - Aimed at providing parameters for JULES model integration.

- 3.1.3 Leaf traits and plant community traits
  - Leaf N, Leaf P, LDMC, SLA, LMA, canopy height, bryophyte cover measured at most sites (2013–2014).
  - LMA derived from leaf area and dry weight; N and P analyzed chemically.
  - Traits linked to WP2 goals for ecosystem process modeling.

- 3.2.1 General soil measures
  - Intact soil cores collected to 1 m depth across 17 habitats; analyses include soil water content, bulk density, LOI and LOI-C, pH, EC, total C and N.
  - QA/QC and methodological notes referenced; data intended for incorporation into soil-plant-process links.

- 3.2.2 Phosphorus
  - Olsen P, Root-P, Complex-P, Enzyme-P, Protons-P measured using multiple extraction and colorimetric methods (Malachite Green), plus enzyme assays (phosphatase and phytase).
  - Procedures emulate plant/microbial P release and uptake; results expressed in appropriate units.

- 3.2.3 Available carbon and nitrogen
  - Soil available C and N measured via 0.5 M K2SO4 extraction; NO3 and NH4 analyzed with colorimetric assays; DOC and TDN analyzed via CEH Bangor methods.
  - Detailed QA/QC and extraction steps described.

- 3.2.4 Soil available cations (Ca, Na, K)
  - 0.5 M acetic acid extraction; cations measured with a flame photometer.
  - Data contribute to understanding base cation availability and nutrient status.

- 3.2.5 Root biomass
  - Total and fine root biomass measured at six sites using soil cores; roots scanned with WinRHIZO, dried, and weighed.
  - In-growth root cores used to assess root growth over a season; methodology documented.

- 3.2.6 Soil elements – TXRF analysis
  - TXRF applied to all 17 sites for broad elemental composition (Al, Fe, Ca, K, etc.).
  - Sample preparation includes grinding, suspension with TritonX, and disc deposition; instrument and QA notes provided.
  - Limitations discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.

## Data provenance, QA, and integration
- Each data subset includes clearly identified responsible researchers and contact points.
- Method descriptions reference standard literature and bespoke scripts (e.g., R-based fitting for photosynthesis curves) to enable reproducibility.
- The dataset is designed to support cross-site synthesis and parameterization for the JULES model, with explicit links to plant and soil nutrient flux processes.

## Version history and contact details
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- Corresponding data authors/contacts provided for each data area (e.g., Simon Smart, Lina Mercado, Helen Glanville) with email addresses in the document.

## Abbreviations
- A comprehensive table of abbreviations used in the dataset (e.g., Asat, BD, Jmax, N, P, SLA, LMA, SWC, Vcmax, etc.) is provided to support correct interpretation of measurements and parameters.

## Practical notes for Data Stewards
- Ensure consistent site numbering and habitat coding when integrating across the five CSV files.
- Handle NA values as missing data per the documented schema; document any restricted depths or replicates in future updates.
- Maintain provenance by preserving data responsibility, method references, and versioning for traceability.
- Use the five-file structure to facilitate discovery, reuse, and model integration (notably for linking to JULES parameters).