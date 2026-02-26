# Turf2Surf WP2 Supporting documentation for data

## Overview
- Documentation for Turf2Surf WP2 focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere in the Conwy catchment.
- Aims to link plant and soil nutrients to ecosystem processes and to integrate parameters into the JULES model.

## Project details and authorship
- Project emphasis: coupled nutrient cycling in terrestrial and freshwater ecosystems; information on nitrogen and phosphorus related impacts on carbon exchange.
- Members and authors: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch; corresponding author Sabine Reinsch; data processing by Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, etc.
- Version history: dated 01/06/2016; updates 25/08/2016 and 04/11/2016.
- Data responsibility and contact points provided for major datasets (e.g., NPP, photosynthesis, leaf traits, soils, TXRF).

## Data assets and scope
- Five data files comprising the dataset:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Focus areas:
  - Conwy catchment information (1.0 Information about the Conwy catchment)
  - Habitats and sampling sites (2.0 Habitats and sampling sites)
  - Equipment, protocols and data processing (3.0 Equipment, protocols and data processing) with detailed subsections for aboveground biomass, photosynthesis, leaf traits, soils, phosphorus, carbon and nitrogen, cations, root biomass, and TXRF
  - Dataset structure (4.0 Dataset structure)
- Data provenance includes site-level measurements across multiple habitats, with plots and replicates, spanning 2013–2016 for various measures.

## Dataset structure and schema
- Site-based dataset design:
  - Column A: unique Site number
  - Column B: Habitat
  - Column C: Detailed habitat description
  - Column D: Site name
  - Column E: Ecosystem Component (Plant, Soil, or Roots)
  - Column F: For Plant components, species; otherwise NA
  - Column G: Plot number
  - Column H: Replicate number
  - Column I: Soil depth interval (for Soil and Roots components)
- Data gaps are indicated as NA to reflect restricted depths, limited replicates, or outliers.
- Dataset structure supports cross-linking plant and soil data to ecosystem processes and model inputs (e.g., JULES).

## Methods and data processing highlights
- 1.0 Information about the Conwy catchment
  - ~500 km2 catchment in North Wales; diverse landscapes and stakeholders; climate gradient and varied soils; baseline data across gene-to-landscape processes.
- 2. Habitats and sampling sites
  - Table of 23 habitats with site-specific plots and dominant species (e.g., blanket bog, conifer woodlands, various grasslands, woodlands, heathlands, arable).
- 3. Equipment, protocols and data processing
  - 3.1.1 Aboveground net primary productivity (NPP)
    - Annual NPP measured for dominant species across sites (2013–2015) using 4 plots per habitat; winter clipping and grazing exclusion in some habitats; biomass calculation approaches vary by vegetation type; data processing linked to JULES (Smart as data custodian).
  - 3.1.2 Plant photosynthesis measures
    - Vcmax, Jmax, Asat measured for dominant species using CIRAS-I with CO2 chambers and LICOR 6400; 2013–2016; temperature corrections and modeling via Farquhar-based approaches; scripts available on GitHub (FitFarquharModel).
  - 3.1.3 Leaf traits and plant community traits
    - Leaf N and P, LDMC, SLA, LMA, canopy height, bryophyte cover; 2013–2014; LMA/LMA calculation from leaf scans and dry weights; analyses support parameterization for vegetation models.
  - 3.2.1 General soil measures
    - Intact soil cores (n=3 per habitat, 17 habitats) down to 1 m; depth-stratified sampling; SWC, BD, LOI, LOI-C, pH, EC, total C and N measured; QA/QC and collaboration across multiple labs.
  - 3.2.2 Phosphorus
    - Olsen P, Root-P, Complex-P, Enzyme-P, and other P fractions measured using colorimetric malachite green and related methods; detailed extraction protocols for each fraction; references to DeLuca et al. and Ohno & Zibilske.
  - 3.2.3 Available carbon and nitrogen
    - DOC and TDN measured via 0.5 M K2SO4 extraction with subsequent analyses; NO3 and NH4 analyzed by colorimetric methods; QA/QC procedures noted.
  - 3.2.4 Soil available cations
    - Ca, Na, K measured after 0.5 M acetic acid extraction using flame photometry.
  - 3.2.5 Root biomass
    - Total and fine root biomass via soil cores, WinRhizo analysis, and oven-dried weights; in-growth root cores to assess root growth; coordination across several sites.
  - 3.2.6 Soil elements – TXRF
    - Total elemental analysis (Al, Fe, Ca, K, etc.) by TXRF; sample prep and analysis workflow; limitations documented in a dedicated file.
- 4. Dataset structure
  - Clarifies the five data files, their column structure, and guidance on missing values.

## Data governance and access considerations
- Purpose-built dataset intended to supply baseline data for cross-site comparisons and model integration (notably JULES).
- Metadata and methods are documented to enable reuse, traceability, and reproducibility.
- TXRF limitations and other methodological caveats are acknowledged and described in separate documentation files.
- Versioned documentation with explicit responsible parties and data processing responsibilities to support data stewardship.

## Practical notes for data leaders
- Data are organized to enable integration with ecosystem models (e.g., JULES) and cross-link plant traits, NPP, photosynthesis metrics, and soil chemistry across multiple habitats.
- Clear site-habitat mappings, plot and replicate schemes, and depth-specific soil measures support aggregation, stratified analyses, and reproducible data pipelines.
- Missing values are transparently indicated as NA, reflecting measurement constraints or data gaps.
- Data processing scripts and model-fitting workflows (e.g., photosynthesis parameterization) are accessible (e.g., GitHub) for reproducibility and extension.