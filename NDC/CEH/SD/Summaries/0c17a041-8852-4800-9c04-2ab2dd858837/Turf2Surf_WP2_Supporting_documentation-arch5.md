# Turf2Surf WP2 Supporting documentation for data

- Purpose and scope
  - Turf2Surf WP2 investigates coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange between land and atmosphere.
  - Data are produced to support understanding of ecological, biogeochemical and hydrological processes across sites and to inform integration with the JULES model.

- Project and authorship
  - Project members: Bridget Emmett, Davey Jones, Simon Smart, Lina Mercado, Helen Glanville, Maria C Blanes, Harry Harmens, Sabine Reinsch.
  - Authors: Sabine Reinsch (corresponding), Helen Glanville, Simon Smart.
  - Data responsible contacts specified for key components (e.g., NPP, photosynthesis, leaf traits, soils, TXRF).

- Versioning and documentation
  - Document version dates: 01/06/2016; 25/08/2016; 04/11/2016.
  - A separate file (Turf2Surf_WP2_TXRF_Limitations_Glanville.rft) documents TXRF method limitations.
  - Code and processing scripts for photosynthesis modeling available (GitHub: mdekauwe/FitFarquharModel), supporting reproducibility.

- Dataset scope and structure
  - Study area: Conwy catchment, North Wales (~500 km2), with diverse habitats and a strong climatic gradient.
  - Data structure comprises five CSV data files:
    - Turf2Surf_Plant_biomass_data.csv
    - Turf2Surf_Plant_structural_data.csv
    - Turf2Surf_Plant_physiological_data.csv
    - Turf2Surf_Soil_Carbon_data.csv
    - Turf2Surf_Soil_raw data.csv
  - Core schema (shared across files)
    - Site number (primary key)
    - Habitat and detailed Habitat description
    - Site name
    - Ecosystem Component (Plant, Soil, or Roots)
    - For Plant components, species information; otherwise NA
    - Plot number (1–4) and Replicate number
    - For Soil and Roots components, Soil depth interval
  - Missing data are indicated as NA; depth and replicate coverage vary by dataset.

- Data collection, processing, and QA topics
  - Information about the Conwy catchment (habitats, plots, sites) and sampling design to support reproducibility and cross-site comparisons.
  - Aboveground net primary productivity (NPP)
    - Measured annually 2013–2015 for dominant plant species at all sites.
    - Four plots per site; winter clipping with grazing exclusion in some habitats; adjustments for plant life strategies.
    - Aboveground standing biomass measured at 10 of 17 sites with multiple replicates; biomass estimation methods differ by habitat (grassland/bog vs woodland).
    - NPP data linked to JULES via Turf2Surf WP2 workflows.
  - Plant photosynthesis measures (Vcmax, Jmax, Asat)
    - Measurements on dominant species using CIRAS-I with CO2 chambers and LICOR 6400 across 50–2000 ppm CO2; temperature corrections applied.
    - Data processing and modeling scripts referenced, with links to code and documentation.
  - Leaf traits and plant community traits
    - N, P, LDMC, SLA, LMA, canopy height, bryophyte cover; measurements in 2013–2014.
    - Leaf traits linked to photosynthesis and nutrient parameters for integration into models.
  - Soil measurements and nutrient pools
    - General soil measures: intact cores to 1 m depth; SWC, BD, LOI, LOI-C, pH, EC, Ctot, Ntot; spring 2014 sampling.
    - Phosphorus fractions: Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P, with colorimetric assays.
    - Available carbon and nitrogen: 0.5 M K2SO4 extraction for DOC and TDN; analyses described.
    - Soil available cations: Ca, Na, K via 0.5 M acetic acid extraction; measured with flame photometry.
    - Root biomass: total and fine roots across six sites; root scanning with WinRhizo; in-growth root cores and biomass measurements.
    - TXRF soil elemental analysis: multi-element soil chemistry across 17 sites; detailed prep and analysis workflow; limitations documented in a separate file.
  - Data provenance and roles
    - Clear attribution of data responsibility to individuals for each data type (e.g., Glanville, Blanes, Harmens, Smart, etc.).
    - Multiple institutions involved (e.g., CEH, Bangor University, Exeter University, etc.), with documented QA/QC processes.

- Governance, access, and reproducibility considerations for Data Stewards
  - Dataset designed to support integration with the JULES model, including explicit metadata and a defined dataset structure to facilitate discovery and reuse.
  - Availability of data processing scripts and reference procedures to enable reproducibility (GitHub link for photosynthesis modeling; detailed methods for soil and nutrient analyses).
  - Documentation of QA/QC steps, calibration procedures, and standard analytical sequences (e.g., six-point calibration for C and N, colorimetric assay protocols for P fractions, TXRF sample preparation and standards).
  - TXRF limitations acknowledged, with a dedicated file to capture methodological caveats.
  - Version control and provenance captured through stated version dates and author contributions, enabling traceability of data lineage.
  - Explicit data dictionary aspects embedded in the dataset schema (column mappings and NA handling) to support consistent data interpretation.

- Data use and reuse guidance
  - Five data files cover plant biomass, plant structure, plant physiology, soil carbon, and raw soil data, enabling cross-domain analyses (aboveground, belowground, and soil nutrient dynamics).
  - Site, habitat, plot, replicate, and depth interval fields enable robust stratification and replication in meta-analyses.
  - Clear guidance on missing values and depth-specific data helps quantify uncertainty and avoid misinterpretation.
  - Researchers should reference the data in conjunction with the project documentation and the linked modeling scripts to ensure proper context and reproducibility.

- Contacts and governance calls
  - Data responsible individuals listed for each data domain, with contact details (emails provided in the document) to facilitate data requests, metadata clarifications, and updates.