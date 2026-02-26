# Soil Organic Carbon Dynamics (SOC-D) data description

- Purpose: Document a nationally relevant, multi-maceted data collection to understand soil organic carbon (SOC) dynamics, identify where UK SOC stocks are at risk, and explore management options to increase SOC. The project aims to test emergent biological and physical controls on SOC and develop a modular process-based model that can integrate with existing soil models.

## Study design and site information

- Five grassland-to-woodland contrasts across England:
  - Gisburn-1, Gisburn-2 (Gisburn area, North England)
  - Alice Holt (South England)
  - Wytham Woods (South England)
  - Kielder Forest (North England)
- Experimental layout per site:
  - Plot 1: grassland; Plot 2: woodland
  - Each plot divided into six grids (1–3 in grassland; 4–6 in woodland)
  - 9 sampling locations per grid, totaling 18 per site
  - Contrasts sampled along transects to capture proximity effects of trees on soil processes
- Site selection context:
  - 42 potential sites identified; 10 accessed; 5 contrasts selected based on age, management history, size, transect placement, access
- Rationale for grassland-to-woodland contrasts:
  - Planned woodland expansion to meet Net Zero targets
  - Uncertainty about when and where trees increase SOC

## Data collected (datasets)

- Aboveground measurements
  - ANPP (aboveground net primary productivity) and litter layer depth
  - ANPP estimates derived from leaf traits (LDMC) and cover-weighted LDMC
- Soil physical, chemical, and biological properties (0–100 cm, up to six depth increments)
  - Common measurements: bulk density (BD), soil moisture, pH (DIW and CaCl2), electrical conductivity (EC), LOI (loss on ignition)
  - Chemical/biological: SOC, total C and N, total P, dissolved organic carbon (DOC), nitrate-N (NO3-N), cation exchange capacity (CEC), base cations (Ca, Mg, K, Na)
  - Physical: soil texture (particle size distribution, PSD; aggregate size distribution, ASD), soil bulk properties
  - Biological/biogeochemical: soil enzymes (selected sites), microbial community DNA (bacteria, fungi via 16S/ITS amplicons) and metagenomes
- Soil hydraulic properties
  - Soil water release curves (HYPROP) and unsaturated hydraulic conductivity (K via mini-disk infiltrometer)
  - HYPROP measurements include pF curves and conductivity across tensions; some sites lack HYPROP data due to logistics
- Earthworms
  - Counts and species identifications; fresh biomass measured in field and lab
- Density fractions of soil organic matter (SOM)
  - Four fractions after density fractionation: DOC, LP (free light/particulate OM), OP (occluded particulate OM), MA (mineral-associated OM)
  - Associated C and N contents for each fraction; C:N ratios
- Microbial community metrics
  - Amplicon sequencing (16S rRNA for bacteria, ITS for fungi)
  - Shotgun metagenomics for functional gene content
  - Derived ordination scores (e.g., NMDS axes) for microbial community structure
- Additional soil properties by depth
  - Depth-resolved NO3-N, DOC, EC, pH, BD, LOI, total C and N, total P
  - Topsoil (0–15 cm) and subsoil measurements aligned with national datasets (LUCAS, GMEP, ERAMMP)

## Data structure and data access

- Core data organization
  - SOC-D_DATABASE_CONNECTOR.csv: links sample IDs to site, land use (grassland vs woodland), plot, grid, core, transition distance, lateral distance, slice, lab layer, and location metadata
  - SOC-D_DATABASE_LOCATIONS.csv: location IDs with coordinates (OS grid references and lat/long)
- Datasets (four main thematic groups)
  - ANPP and litter depth: linking to location IDs; ANPP estimates (mean, high, low) and litter depth means per grid
  - Soil metrics (0–1 m; common metrics across all sites): field water content, EC, BD, pH (DIW and CaCl2), LOI, total C and N, total P, NO3-N, DOC, CEC, metals (Ca, Mg, K, Na), enzyme activities (where available)
  - Soil metrics by grids 2/5 (grassland/woodland) and depth, including fraction-specific carbon and nitrogen, CEC, major ions, enzyme metrics, and microbial NMDS scores
  - HYPROP-related data (water release curves and conductivity) and associated raw HYPROP files
  - Earthworms: species counts, biomass, and notes
  - Optional top- and subsoil data subsets for 0–15 cm vs deeper layers
- Sequencing data
  - Raw sequence data deposited in ENA under project PRJEB66294
  - Derived metrics include OTU tables, NMDS scores, and gene abundance matrices
- Data quality and completeness
  - NA indicates missing values
  - Quality control via internal standards, duplicates, and site-specific QA (EC, pH, LOI checks)
  - Some measurements not collected at all sites (e.g., HYPROP cores at Alice Holt; earthworms at certain plots)
- Access and usage notes
  - Datasets are designed for integration with UKCEH long-term monitoring data
  - Supplementary materials (A–C) provide field mapping, coring details, and measurement prioritization

## Collection and analytical methods (summary)

- Aboveground productivity
  - ANPP estimated from leaf material; LDMC values from observed leaves or trait databases; regression-based predictions with uncertainty propagated via MCMC
- Litter and soil sampling
  - Litter depth measured at three points per sampling location
  - Multiple soil core types used to capture vertical profiles:
    - Hyprop cores for 0–5 cm (and 30–35 cm where possible)
    - National survey style cores for 0–15 cm
    - 0–30 cm blocks for undisturbed sampling
    - 0–100 cm cores (minidisk, Cobra precision corer, Split Tube Sampler, or Russian Auger depending on site) to capture deep SOC and physical properties
- Soil hydraulic properties
  - HYPROP to derive water retention curves; HYPROP-FIT software used for analysis
  - Unsaturated hydraulic conductivity (K) from mini-disk infiltrometer at targeted tensions
- Earthworms
  - Hand-sorted blocks (25 cm × 25 cm × 25 cm) within 15 minutes, weighed and identified to species
- Soil physical/chemical analysis
  - Bulk density, EC, pH (DIW and CaCl2), LOI by thermogravimetric analysis
  - C, N, and P via elemental analysis and digestion chemistry
  - Nitrate, DOC, and CEC via standardized extraction and detection methods (ICP-OES, colorimetric assays)
  - PSD and ASD via laser diffraction; OC removal procedures and QC with internal standards
- Soil organic matter fractions
  - Density fractionation with sodium polytungstate (SPT) to separate DOC, LP, OP, MA
  - Carbon and nitrogen content measured for each fraction
  - Enzyme activities (where available) for hydrolytic and oxidative enzymes
- Microbial analyses
  - DNA extraction for 16S and ITS amplicon sequencing; metagenomes for functional gene content
  - Data processing using DADA2, DIAMOND/SEED-based annotation, and ordination analyses
- Supplementary site information
  - Supplementary maps and field sheets document precise sampling locations, distances from transition, and site-specific conditions

## Project context and outputs

- Objective throughout: establish a robust, repeatable data framework for SOC-D across nationally relevant land-use contrasts
- Outputs include:
  - A modular SOC dynamics model framework to explore SOC sensitivity to climate and land management
  - A suite of harmonized datasets suitable for cross-site comparisons and model calibration
  - Connections to long-term monitoring programs and national soil datasets
- Acknowledgments
  - Support from UK-SCAPE (NER/NERC) and collaboration with Forest Research; access to Alice Holt and Kielder Forest