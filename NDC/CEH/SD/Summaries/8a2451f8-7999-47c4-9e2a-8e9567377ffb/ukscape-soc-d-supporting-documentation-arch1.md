# Soil Organic Carbon Dynamics (SOC-D) data description

- Purpose and scope
  - Describes co-located aboveground and belowground measurements across five grassland-to-woodland contrasts in England (2018–2021) as part of the SOC-D project within UK-SCAPE.
  - Aims to understand biotic and abiotic controls on soil organic carbon (SOC) dynamics, identify UK regions at SOC risk, and inform land-management policies to increase SOC storage.
  - Part of a broader program to test a paradigm shift toward biological/structural controls on SOC and to develop a modular process-based SOC model.

- Study design and site contrasts
  - Five long-term contrasts across England: Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest.
  - Each contrast pairs grassland with woodland, organized into plots and grids: Plot 1 = grassland, Plot 2 = woodland; grids 1–3 in grassland and 4–6 in woodland.
  - Sampling locations: nine per grid, totaling 18 sampling points per contrast.
  - Sampling windows: initial soil cores (Nov 2018–Mar 2019) with follow-up measurements 2020–2021.
  - Site selection criteria emphasized woodland age, management history, plot size, accessibility, and minimization of confounding factors.

- Datasets and data products
  - Four main data collections (datasets 2–5 in the data package):
    - Aboveground Net Primary Productivity (ANPP) and litter layer depth (0–5 cm and 0–15 cm context) with LDMC-based ANPP estimates.
    - Soil properties (chemical, physical, and biological) for up to six depth increments within 0–100 cm.
    - Soil hydraulic properties, including soil water release curves (HYPROP) and unsaturated hydraulic conductivity (Kfs) from field and lab measurements.
    - Earthworm counts and species identification with biomass data.
  - Additional microbial data (6.4 and 6.5): amplicon sequencing (16S, ITS2) and metagenomes from topsoil and subsoil; includes microbial community metrics and functional gene data.
  - Supplementary connectivity files:
    - SOC-D_DATABASE_CONNECTOR.csv: links sample IDs to site, plot, grid, core, depth slice, and sampling geometry (transition distance, lateral distance, etc.).
    - SOC-D_DATABASE_LOCATIONS.csv: site coordinates and OS grid references.
  - Specific datasets:
    - SOC-D_DATABASE_ANPP.csv and SOC-D_DATABASE_LITTER_DEPTH.csv: ANPP estimates and litter-depth means by location.
    - SOC-D_DATABASE_COMMON_SOIL_METRICS.csv: common soil metrics across all depths (0–1 m).
    - SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv: grid2/grid5 soil metrics across all depths.
    - SOC-D_DATABASE_HYPROP_*, HYPROP retention and hydraulic conductivity data: four HYPROP-related files (raw and modeled outputs).
    - SOC-D_DATABASE_EARTHWORMS.csv: earthworm counts, weights, and species-specific biomass data.
  - Missing data and QA: NA entries mark missing data; several site-specific measurements were not collected or were excluded due to QA issues (e.g., Gisburn enzyme data omitted; microbial biomass data affected by freezing).

- Measurements and methods (high-level)
  - ANPP and LDMC
    - Fresh leaf material collected May–July 2021 (longest/northern sites later). LDMC used with a cover-weighted approach (cLDMC) to predict ANPP via a regression model.
  - Litter depth
    - Measured at three points per sampling location; average reported.
  - Soil physical, chemical, and biological properties (0–100 cm)
    - Common measurements on 0–100 cm cores; additional analyses on limited top or bottom layers or limited grids.
    - Analyses include LOI (via TGA), SOC, TN, P, NO3–, DOC, EC, pH, BD, CEC, and a suite of elemental analyses (Ca, Mg, K, Na, etc.).
  - Soil texture and structure
    - PSD via laser diffraction; OMsfractions via density fractionation (LP, OP, MA) with DOM; aggregates characterization (ASD) and associated OC/N fractions.
  - Soil hydraulic properties
    - HYPROP-derived water release curves for 0–5 cm (and 30–35 cm for some sites) and Kfs (unsaturated conductivity) from mini-disk infiltrometers.
  - Earthworms
    - Hand-sorted sampling (25 cm × 25 cm block to 25 cm depth) with 15-minute sorting limit; species-level counts and biomass.
  - Microbial communities (6.4/6.5)
    - DNA extraction from 0.2–2.5 g samples; amplicon sequencing of 16S rRNA (bacteria) and ITS2 (fungi); shot-gun metagenomics; downstream OTU/ASV/functional profiling and ordination metrics.
  - Ancillary/quality controls
    - Internal standards, duplicates, reference materials, and QA steps across chemistry and sequencing workflows.
    - Documentation of field and lab processing steps, core lengths, and depths for reproducibility.

- Depth framework and soil layers
  - Primary depth increments across 0–100 cm: 0–5 cm, 5–15 cm, 15–30 cm, 30–50/60 cm, 50/60–100 cm.
  - Topsoil definition adjustments per site: some sites use 0–15 cm topsoil; Gisburn sites sometimes used 0–5 cm and 15–60 cm (adjusted for consistency and sample sufficiency).
  - Core types and lab processing: multiple corer types (Cobra precision, Split Tube, Russian Auger) with site-specific processing notes; 1-m cores sliced into the five depth increments for analyses.

- Data structure and interoperability
  - Data are organized to enable co-location of soil and vegetation data; the connector file links all measurements to a common sampling location (SITE, PLOT, GRID, CORE, SLICE, DEPTH_TOP/BOTTOM).
  - Location-level metadata include geographic coordinates, OS grid references, and lat/long coordinates for mapping and spatial analyses.
  - Datasets are designed for integration with national soil datasets (e.g., LUCAS, GMEP, ERAMMP) and model development for SOC dynamics.

- Analytical focus and potential uses
  - Four guiding questions frame analyses:
    - How sensitive is SOC to local/global climate and land-management changes?
    - What feedbacks link SOC with soil structure, chemistry, and functional biota?
    - Which soil metrics and models best reflect updated SOC dynamics understanding?
    - Which UK regions/land-use combinations are most at risk of SOC loss or are suitable for SOC enhancement?
  - The acquired data enable testing of biotic–abiotic interactions (soil structure, biota, chemistry) and their influence on SOC storage across a national-scale set of soil-vegetation-climate combinations.
  - The inclusion of microbial sequencing data and density-fractionation fractions supports mechanistic exploration of SOC stabilization pathways.

- Limitations and caveats
  - Some measurements were site-specific and not uniformly collected across all sites (e.g., HYPROP cores not collected at Alice Holt; extracellular enzyme data for Gisburn were excluded due to buffer issues).
  - Microbial biomass measurements were compromised by freeze-thaw effects in some samples, affecting reliability.
  - Data are stored with NA placeholders for missing measurements; cross-site comparability may require careful normalization and alignment of depth intervals when aggregating.
  - Data are released with rich metadata and supplementary materials (Supplements A–C) to aid interpretation and reproducibility.

- Data provenance, governance, and access
  - Funded by UK Natural Environment Research Council as part of the UK-SCAPE program (NE/R016429/1).
  - Collaboration with UKCEH and partner sites (e.g., Forest Research at Alice Holt and Gisburn; Kielder Forest).
  - Raw sequencing data deposited in ENA under project PRJEB66294; processed data and connectors provided in the SOC-D data package.
  - Analytical workflows and quality checks documented; data are designed to be discoverable and usable via metadata and dataset connectors.

- Related resources and references
  - Supplementary materials and project documentation (Supplements A–C) provide field maps, coring details, and measurement decisions.
  - Notable methodologies referenced include HYPROP, plant trait databases (LEDA, ECPE), standard soil analytic methods (SOP3102), and established soil carbon/organic matter fractionation frameworks.