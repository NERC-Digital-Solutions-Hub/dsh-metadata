# Soil Organic Carbon Dynamics (SOC-D) – Data Description

- Purpose and scope
  - Describes co-located aboveground and belowground measurements from five long-term grassland-to-woodland contrasts across England (2018–2021) as part of the SOC-D project.
  - Aims to understand physical, chemical, and biotic controls on soil organic carbon (SOC) dynamics, identify UK areas most at risk of SOC loss, and inform land-management policies to enhance SOC storage.
  - Builds towards a flexible, process-based SOC dynamics model that can be embedded in broader soil models.

- Study design and sites
  - Five contrasts across England: Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, and Kielder Forest.
  - Each contrast comprises two plots (plot 1 = grassland, plot 2 = woodland) and is further divided into six grids (3 in grassland, 3 in woodland) with a boundary between grids 3 and 4.
  - Sampling: 18 locations per contrast (two plots × nine locations per plot), with in-situ measurements in grids 2 (grassland) and 5 (woodland), and soil cores collected to 100 cm depth.
  - Site selection criteria emphasized woodland age, management history, plot size, transition location, access, and permission.

- Datasets and measurements (four main data streams)
  - Aboveground Net Primary Productivity (ANPP) and litter layer depth
    - ANPP derived from leaf dry matter content (LDMC) and species cover; LDMC values linked to a regression model to produce ANPP estimates.
    - Litter depth measured at three points per sampling location.
    - ANPP and LDMC data cover 2021; litter depth data cover 2018–2019.
  - Soil physical, chemical, and biological properties (0–100 cm)
    - Common measurements across up to six depth increments (0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm) and site-specific measurements for top layers.
    - Properties include bulk density, pH (DIW and CaCl2), electrical conductivity, LOI (via TGA), SOC, total N, P, NO3–, DOC, CEC, SWC, PSD, ASD, and SOM density fractions (LP, OP, MA fractions) plus DOM.
    - Soil blocks and cores prepared using multiple corer types (Hyprop, national survey cores, Split Tube, Cobra, Russian Auger) with depth-resolved sampling and careful lab processing.
  - Soil hydraulic properties and water release
    - HYPROP-based soil water release curves (0–5 cm; 30–35 cm at some sites) and unsaturated hydraulic conductivity (K) via mini-disk infiltrometer.
    - Data include pF values, water content, and log10 K, with HYPROP raw data and processed outputs for multiple depths and grids.
  - Earthworms
    - Earthworm counts and fresh biomass per sampling location; species-level counts for a range of taxa.
    - Standardized hand-sorting method within a 25 cm × 25 cm soil block to 25 cm depth; field and lab handling details provided.

- Analytical methods and quality control
  - ANPP
    - LDMC values linked to dominant species; LDMC-specific regressions yield ANPP with uncertainty propagated via MCMC.
  - Soil properties
    - Bulk density from 1 m cores; EC and pH measured in DIW and CaCl2; LOI via TGA; SOC and total C/N by elemental analysis (Vario EL); total P by acid digestion; NO3–, DOC by colorimetric/UV methods; CEC by ammonium acetate extraction with ICP-OES; moisture and LOI QC with internal standards and replicates.
  - PSD, ASD, and SOM fractions
    - PSD via laser diffraction (Beckman Coulter), with OC dispersion steps; ASD derived from LD data; fractionation into DOC, LP, OP, and MA fractions for SOM characterization.
  - Enzyme activities and microbial community
    - Extracellular enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) using fluorogenic/substrate assays; data available for select sites.
    - Microbial community analyses: amplicon sequencing (16S rRNA for bacteria, ITS2 for fungi) and metagenomics; data processing includes OTU/ASV clustering (DADA2), sequence quality control, and downstream ordination metrics.
  - Data structure and connectivity
    - Two central connectors: SOC-D_DATABASE_CONNECTOR.csv (linking sample IDs to site/polygons/plots/grids/cores/slices) and SOC-D_DATABASE_LOCATIONS.csv (location coordinates and IDs).
    - Datasets organized as:
      - ANPP and litter depth (ANPP, LITTER_DEPTH)
      - Common soil metrics (0–1 m) linked by SAMPLE_ID
      - Soil metrics grid2/grid5 (topo/soil properties by grid)
      - Soil hydraulic properties and HYPROP data
      - Earthworms dataset
    - Missing values indicated as NA; top-of-sample depth decisions vary by site (0–5 cm or 0–15 cm) to ensure adequate material.

- Data quality, completeness, and limitations
  - Completeness: Common measurements (e.g., LOI, BD, pH, EC) are complete; more expensive or site-specific measurements are limited (e.g., SOM fractions, enzymes, certain soil chemistry fractions).
  - Site-specific gaps: Some measurements were not collected at certain plots or depths (e.g., HYPROP cores at Alice Holt; some earthworm or enzyme measurements missing at Gisburn sites).
  - Data handling constraints: Microbial biomass and enzymes can be affected by sample handling (e.g., freezing impacts microbial biomass; enzyme data only comparable within the same site/land-use pair due to buffer mismatches at Gisburn).
  - Field-to-lab propagation and processing decisions documented (e.g., depth increments, curation of cores, handling of peat vs mineral layers).

- Governance, access, and reuse
  - Data managed and quality-assured by UK Centre for Ecology & Hydrology (UKCEH) with collaboration from partner sites (e.g., Forest Research).
  - Metadata and dataset structure are clearly documented to enable cross-linking across data types and depths.
  - Supplementary information (A–C) provides field sheets, core-depth details, and planned measurement sets; some elements are site- and method-specific.
  - The study is positioned to inform environmental monitoring and policy decisions around SOC storage and risk under different land-use scenarios (grassland vs woodland).

- Policy and monitoring implications
  - Provides a comprehensive, multi-layered data framework to scrutinize SOC dynamics under changing land-use and climatic conditions.
  - Enables evaluation of policy-relevant questions such as SOC sensitivity to climate and land management, the role of soil structure and biology in SOC stabilization, and identification of UK regions most at risk of SOC loss.
  - Delivers a modular data architecture and suite of measurements suitable for integration into policy monitoring frameworks and process-based models.