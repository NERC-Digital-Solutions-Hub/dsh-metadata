# Soil Organic Carbon Dynamics (SOC-D) data description

- Purpose: Characterize biotic and abiotic controls on soil organic carbon (SOC) dynamics in UK grassland-to-woodland contrasts to identify SOC risk areas and opportunities to enhance SOC storage; develop a modular, process-based SOC dynamics model for integration with other soil models.

- Scope: Data from five long-term grassland-to-woodland contrasts across England (2018–2021), combining aboveground and belowground measurements to link soil structure, chemistry, biology, and hydrology with SOC dynamics.

- Datasets (four main co-located measurements per site):
  - Aboveground net primary productivity (ANPP) and litter layer depth (0–5 cm litter and 0–100 cm soil cores used for common properties).
  - Soil physical, chemical, and biological properties across up to six depth increments (0–100 cm).
  - Soil hydraulic conditions: water release curves (HYPROP) and unsaturated hydraulic conductivity (K) measurements.
  - Earthworm counts and species IDs (with biomass).

- Sites and sampling design:
  - Locations: Gisburn-1, Gisburn-2 (N England); Alice Holt (S England); Wytham Woods (S England); Kielder Forest (N England).
  - Each site features a grassland plot and an adjacent woodland plot (two plots per site). Within plots, nine sampling locations were selected in grids arranged to capture distance to the grassland–woodland boundary (grids 1–3 grassland; 4–6 woodland).
  - Sampling across locations included in situ measurements (ANPP, infiltration, earthworms) and soil cores (0–100 cm) for laboratory analyses.
  - Temporal span: soil cores collected late 2018–early 2019; additional measurements 2020–2021; vegetation sampling in 2021.

- Depths and core methods:
  - Common soil measurements on 0–100 cm cores across up to six depth increments (e.g., 0–5 cm, 5–15 cm, etc.; site-dependent adjustments up to 60 cm).
  - Deep soil cores (0–100 cm) obtained with Cobra precision corers or alternative methods (Split Tube, Russian Auger) depending on site and soil type.
  - HyPROP cores for soil water release curves: 0–5 cm (all sites except Alice Holt); 30–35 cm (Wytham Woods, Kielder).
  - Infiltration: mini-disk infiltrometer in grids 2 and 5 (grassland and woodland respectively).

- Analytical methods and quality control:
  - ANPP: derived from leaf dry matter content (LDMC) with cover-weighted LDMC as predictor; LDMC values linked to species via LDMC/SLA databases.
  - Soil properties: EC, pH (DIW and CaCl2), bulk density, LOI (via TGA), total C and N (elemental analyzer; SOP3102), total P, NO3–N, DOC, CEC, base cations, and related QC procedures.
  - Soil physical properties: PSD and aggregate size distribution via laser diffraction; texture (clay, silt, sand) and SOC fractions; SOM density fractions (LP, OP, MA) and dissolved organic carbon (DOC) using density fractionation with sodium polytungstate (SPT).
  - Enzyme activities: hydrolytic (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase) and oxidative (phenol oxidase) activities for select sites.
  - Microbial communities: amplicon sequencing (16S rRNA for bacteria; ITS2 for fungi) and metagenomics; data processed for OTUs and functional gene markers; microbial biomass proxies included.
  - Data linking: two connector files (SOC-D_DATABASE_CONNECTOR.csv; SOC-D_DATABASE_LOCATIONS.csv) to join site, plot, grid, core, sample, and spatial coordinates; per-dataset files provided (ANPP, litter depth, common soil metrics, soil metrics grid, soil hydraulics, HYPROP, earthworms).

- Data structure and connectivity:
  - CONNECTOR file links sample IDs to site/plot/grid/location and sampling geometry (transition distance, lateral distance, slice depth, etc.).
  - LOCATIONS file provides coordinates (OS grid references, latitude/longitude) for all locations.
  - Four primary data files (ANPP, litter depth, common soil metrics, soil metrics by grid), plus four hydraulics-related files and Earthworm dataset, with missing values denoted as NA.
  - Additional supplemental datasets include top- and sub-soil metrics for mineral soil fractions and enzymatic activities (where applicable).

- Project context and data provenance:
  - Part of the SOC-D project under UK-SCAPE (Grant NE/R016429/1) to test SOC controls, identify at-risk areas, and develop process-based SOC models.
  - Sequencing and metagenomics data deposited in ENA (PRJEB66294); project and datasets linked to UKCEH laboratories and national programs (Countryside Survey, GMEP, ERAMMP, ELUM).
  - Supplementary materials document field mapping (Supplement A), coring details (Supplement B), and measurement planning (Supplement C).

- Limitations and data quality notes:
  - Completeness varies by site and measurement; some top-/sub-soil or enzyme measurements missing due to field constraints or data handling issues.
  - Microbial biomass and certain Enzyme measurements affected by sample preservation and processing (e.g., freezing artifacts) and thus flagged accordingly.
  - Some field-derived measurements (e.g., certain deep soil layers or specific depth increments) were adjusted or omitted to avoid inconsistencies.

- Key outputs and potential analyses:
  - Enables cross-site comparisons of ANPP, litter depth, soil chemistry, hydrology, and biodiversity alongside SOC fractions to infer drivers of SOC stability and vulnerability.
  - Supports development and calibration of process-based SOC models for UK soil-vegetation-climate contexts.
  - Provides co-located datasets suitable for linking aboveground productivity with belowground SOC pools, litter input, root distribution, soil structure, and microbial community composition.