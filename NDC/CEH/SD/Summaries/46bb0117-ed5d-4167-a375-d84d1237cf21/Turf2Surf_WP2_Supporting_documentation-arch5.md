# Turf2Surf WP2 Supporting documentation for data

## Overview
- Project focuses on coupled nutrient cycling in terrestrial and freshwater ecosystems, linking nitrogen and phosphorus dynamics to carbon exchange and water quality.
- WP2 centers on measuring nitrogen and phosphorus impacts on carbon exchange between land and atmosphere, with data intended for integration into ecosystem modeling (e.g., JULES).

## Data governance and stewardship
- Roles and responsibilities are documented per data type:
  - NPP data: Simon Smart
  - Plant photosynthesis measures: Lina Mercado
  - Leaf traits and plant community traits: Lina Mercado and Simon Smart
  - General soil measures: Helen Glanville
  - Phosphorus measurements: Helen Glanville
  - Available C and N: Helen Glanville
  - Soil available cations: Helen Glanville
  - Root biomass and in-growth roots: Helen Glanville
  - Soil elements (TXRF): Helen Glanville
  - Dataset structure: team members across WP2
- Metadata and documentation
  - Table of contents, list of abbreviations, and version dates are provided to support data interpretation.
  - Detailed methodologies for key measurements are documented, with links to separate documents and code repositories.
- Provenance, processing, and reproducibility
  - Data processing for photosynthesis uses a documented workflow; example code and scripts are hosted (GitHub: mdekauwe/FitFarquharModel).
  - NPP methodology and data processing are described in Turf2Surf_WP2_NPP_Smart.rft (separate document).
  - TXRF limitations are explicitly noted in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.
- Data access, sharing, and updates
  - Data are organized into five standardized CSV files with consistent site and habitat identifiers, enabling discovery and reuse.
  - Missing data are clearly indicated as NA to maintain transparency about data completeness.
  - Data are structured to support integration with modeling work (e.g., JULES).

## Dataset structure and content
- Five data files (CSV):
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema across files:
  - Column A: Site number (matches Table 1)
  - Column B: Habitat
  - Column C: Habitat description
  - Column D: Site name
  - Column E: Ecosystem component (plant, soil, or roots)
  - Column F: Plant species (for plant data; NA for soil/root)
  - Column G: Plot number
  - Column H: Replicate number
  - Column I: Soil depth interval (for soil and roots)
- Site coverage
  - Conwy catchment sites with a range of habitats (bogs, moorlands, woodlands, grasslands, rivers, and arable land)
  - Depth intervals for soils extend up to 1 m (with multiple sub-intervals up to 90+ cm)
- Data quality and gaps
  - Missing values indicated as NA
  - Some sites have restricted depths or fewer replicates; explicit note of data limitations is included

## Measurements and methods (high-level)
- 3.1.1 Aboveground net primary productivity (NPP)
  - Annual NPP measured for dominant species (2013–2015) across sites
  - Four plots per site; winter cutting and grazing exclusion where applicable
  - Aboveground biomass measured by species-specific sampling and, for woody vegetation, allometric approaches using DBH, height, and wood density
- 3.1.2 Plant photosynthesis measures
  - Parameters: Asat, Vcmax, Jmax (at 25°C), derived from A–Ci curves
  - Field and laboratory measurements using CIRAS-I, Licor 6400; data are processed with a Farquhar-based model
  - Temperature corrections and species-specific parameters applied
  - Data processing scripts available in GitHub repository
- 3.1.3 Leaf traits and plant community traits
  - Metrics: leaf N, leaf P, LDMC, SLA, LMA, canopy height, bryophyte cover
  - Leaf area and dry weight used to compute LMA; images analyzed with ImageJ
- 3.2.1 General soil measures
  - Intact soil cores collected to 1 m, depth-sliced; analyses include SWC, bulk density, LOI, LOI-C, pH, EC, total C and N
- 3.2.2 Phosphorus
  - Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P
  - Methods include malachite green colorimetry and various extractants (e.g., Olsen, CaCl2, citrate, HCl)
- 3.2.3 Available carbon and nitrogen
  - DOC and TDN measured after 0.5 M K2SO4 extraction
  - NO3 and NH4 measured via colorimetric/enzymatic methods
- 3.2.4 Soil available cations
  - Ca, Na, K measured after 0.5 M acetic acid extraction; flame photometry
- 3.2.5 Root biomass
  - Total and fine roots quantified via soil cores; roots scanned with WinRhizo; in-growth root cores used to assess production
- 3.2.6 Soil elements (TXRF)
  - Multi-element TXRF analysis (Al, Fe, Ca, K, etc.) on soil samples; sample prep and analysis described
  - Limitations and caveats noted in dedicated TXRF limitations document

## Data quality, provenance, and reproducibility
- QA/QC
  - QA/QC procedures are described for C and N analyses; other QA notes are embedded in methodology references
  - Documentation emphasizes cross-site standardization and traceability of samples and analyses
- Reproducibility and modeling integration
  - Data and processing steps are aligned with JULES ecosystem modeling needs
  - Code and methodological references provided to enable replication of analyses (e.g., NPP method doc, photosynthesis modeling scripts)
- Limitations
  - TXRF limitations acknowledged in a separate document
  - Some data gaps exist due to site/topography/restrictions; NA indicates missing data

## Project context, authors, and versioning
- Project members
  - Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch
- Authors
  - Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart
- Version dates
  - 01/06/2016
  - 25/08/2016
  - 04/11/2016
- Contact for data
  - Data responsible contacts are listed for each data domain (e.g., ssma@ceh.ac.uk for NPP; L.Mercado@exeter.ac.uk for photosynthesis)

## Contextual notes for data discovery and reuse
- The Conwy catchment is described in terms of geography, climate gradient, soil diversity, and stakeholder engagement, providing context for data interpretation and transferability.
- The dataset structure is designed to support discoverability, with consistent site identifiers, habitat descriptions, and clear delineation between plant, soil, and root data.
- Data are intended for integration into ecosystem models and for cross-site analyses of nutrient and carbon dynamics across a gradient of habitats.