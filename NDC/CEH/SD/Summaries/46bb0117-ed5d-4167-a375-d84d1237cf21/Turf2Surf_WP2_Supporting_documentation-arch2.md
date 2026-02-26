# Turf2Surf WP2 Supporting documentation for data

## Overview
- Turf2Surf WP2 investigates coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
- Aim is to generate standardized environmental data to support understanding of ecosystem processes, water quality, carbon sequestration, and biodiversity, with links to the JULES model.

## Study Area: Conwy catchment
- Location: North Wales, ~500 km²; diverse landscapes enabling comparative studies.
- Climate: strong gradient (500 mm to >1000 mm annually).
- Habitats: blanket bog, moorland, conifer woodlands, grasslands, lakes, flood plains, salt marshes.
- Stakeholders: water utilities, agriculture, forestry, shellfish, tourism, conservation groups, local communities.
- Sampling framework: extensive baseline data across multiple habitat types (17 sites) to understand pressures on resources and ecosystem services.

## Data collected and methods
- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - Annual NPP for dominant species at all sites (2013–2015); 4 plots per habitat; winter clipping and grazing protection where applicable.
  - Standing biomass measured at 10 of 17 sites (3–9 replicates per habitat); biomass estimated separately for grasses/bogs and woody plants; includes tree cores and litter biomass.
  - Purpose: link plant productivity to soil nutrients and ecosystem processes; inputs prepared for JULES.

- 3.1.2 Plant photosynthesis measures
  - Parameters: Vcmax, Jmax, Asat for dominant species.
  - Field protocols using CIRAS-I with CO2 chambers and LICOR 6400; CO2 curves from 50–2000 ppm; temperature corrections to 25°C.
  - Data processing via Farquhar-based models and Levenberg–Marquardt fitting; scripts available in project repository.
  - Purpose: characterize photosynthetic capacity for integration into ecosystem modelling.

- 3.1.3 Leaf traits and plant community traits
  - Traits measured: leaf N, leaf P, LDMC, SLA, LMA, canopy height, bryophyte cover.
  - Leaf traits linked to photosynthesis and nutrient cycling; LMA and SLA derived from leaf imaging and dry weight measurements.
  - Purpose: improve understanding of species strategies and nutrient use in relation to soil processes.

- 3.2.1 General soil measures
  - Soil cores to 1 m depth across 17 habitats (n=3 per habitat); depth-resolved sampling.
  - Measurements: soil water content, bulk density, LOI and LOI-C, pH, EC, total C and N.
  - QA/QC and multi-lab analyses to support dataset reliability.

- 3.2.2 Phosphorus fractions
  - Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P; multiple extractants and colorimetric assays (Malachite Green method) to quantify P pools representing different bioavailability.
  - Includes steps for sample preparation, extraction, and analysis.

- 3.2.3 Available carbon and nitrogen
  - DOC and TDN measured after 0.5 M K2SO4 extraction; NO3 and NH4 determined by colorimetric methods using microplate assays.
  - NO3: vanadate-based method; NH4: salicylate-nitroprusside/hypochlorite method.
  - Analysis performed at CEH Bangor with QA protocols.

- 3.2.4 Soil available cations (Ca, Na, K)
  - 0.5 M acetic acid extraction; cations quantified by flame photometry.
  - Data contribute to understanding cation exchange and nutrient availability.

- 3.2.5 Root biomass
  - Standing root biomass: 15 cm cores with 0–5, 5–10, 10–15 cm depth intervals; roots scanned (WinRhizo) for length/diameter/branching; dry-weight biomass calculated.
  - In-growth root cores: 63 mm tubes with soil, deployed for ~3–4 months to measure root growth.
  - Data support belowground carbon and nutrient cycling understanding.

- 3.2.6 Soil elements – TXRF
  - Total elemental analyses (Al, Fe, Ca, K, Ti, S, Mn, P, etc.) by TXRF (S2 PICOFOX).
  - Sample preparation includes grinding to fine powder and preparation on discs; data used to characterize elemental composition across habitats.

## Dataset structure and contents
- Five data files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Key columns:
  - Site number (Table 1 mapping)
  - Habitat and detailed habitat description
  - Site name
  - Ecosystem component (Plant, Soil, Roots)
  - If Plant: specific plant species; otherwise NA
  - Plot number (1–4) and Replicate number
  - Soil depth interval for Soil and Roots components
- Data quality notes:
  - Missing values indicated as NA due to depth limits, replicates, or outliers.
- Purpose: deliver integrated plant and soil datasets for environmental monitoring and model parameterisation (e.g., JULES).

## Data management, authors, and versioning
- Data responsible: key researchers including Simon Smart, Bridget Emmett, Helen Glanville, Lina Mercado, Sabine Reinsch, and colleagues from CEH, Bangor University, Exeter University.
- Authors: Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart.
- Version dates: 01/06/2016; 25/08/2016; 04/11/2016.
- Outputs intended for storage in appropriate data portals; designed to be usable for cross-study comparisons and integration with environmental monitoring datasets.

## Relevance to environmental monitoring and data use
- Standardised methods across plant and soil domains enable consistent comparison over time and with policy indicators.
- Datasets support assessment of environmental health, nutrient cycling, and ecosystem services in the Conwy catchment.
- Data are prepared for integration into ecosystem models (e.g., JULES) and for broader data sharing to enhance the value of monitoring datasets beyond single-use applications.

## Considerations for data value and accessibility
- WP2 explicitly aims to increase dataset value by linking plant and soil nutrient data and enabling access to underlying data used to produce outputs.
- Dataset structure and documentation facilitate reuse by other researchers, policy analysts, and environmental managers.
- Clear, standardised protocols and QA practices enhance reliability for monitoring and comparative analyses.