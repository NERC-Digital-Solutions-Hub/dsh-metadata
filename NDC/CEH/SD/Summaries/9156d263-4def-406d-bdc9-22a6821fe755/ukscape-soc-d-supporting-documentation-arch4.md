Soil Organic Carbon Dynamics (SOC-D) data description

- Overview
  - A UK-wide, multi-method study (2018–2021) to understand biotic and abiotic controls on soil organic carbon (SOC) dynamics across five grassland-to-woodland contrasts in England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest).
  - Aims to identify SOC stocks at risk and opportunities to increase SOC via land management; develop a modular, process-based SOC dynamics model for integration with other soil models.
  - Data collected include aboveground productivity, litter depth, comprehensive soil physico-chemical properties to 100 cm (up to six depth increments), soil hydraulic properties, earthworm counts/IDs, and extensive microbial sequencing data.

- Data scope and structure
  - Field design: two plots per site (grassland vs woodland), each plot divided into six grids (grassland grids 1–3; woodland grids 4–6); nine sampling locations per plot (total n ≈ 18 per contrast).
  - Datasets (four main data files plus connectors):
    - ANPP and litter depth (0–5 cm litter; 0–100 cm soils in 0–60 cm increments where applicable).
    - Soil physical, chemical, and biological properties (0–1 m; common measurements across all sites; some measurements limited to top/bottom layers or specific grids).
    - Soil hydraulic properties (HYPROP-derived water release curves; unsaturated hydraulic conductivity; field K using mini-disk infiltrometer).
    - Earthworms: counts and species identification, weights; site-level summaries.
  - Data connectivity: SOC-D_DATABASE_CONNECTOR.csv links sample IDs to site/location/plot/grid; SOC-D_DATABASE_LOCATIONS.csv provides site coordinates and grid references; additional site-specific ANPP and litter depth files connect via LOCATION_ID.

- Specific data collected
  - Aboveground net primary productivity (ANPP) estimated from dominant species LDMC (cover-weighted LDMC as predictor; regression-based prediction with uncertainty via MCMC).
  - Litter depth measured at three points per sampling location.
  - Soil core sampling (0–100 cm) with multiple depth increments (e.g., 0–5, 5–15, 15–30, 30–50/60, 50/60–100 cm; depth scheme adjusted per site for consistency).
  - HYPROP cores for soil water release curves (0–5 cm across most sites; 30–35 cm in some sites) and KFSunsaturated measurements via mini-disk infiltrometer in grids 2 and 5.
  - Earthworm sorting and weighing; species-level counts where possible.
  - Laboratory soil metrics at multiple depths: bulk density, pH, EC, LOI, total C and N, total P, NO3-N, DOC, CEC and exchangeable cations, and, where feasible, enzyme activities (phenol oxidase, phosphatase, glucosidase, N-acetylglucosaminidase, leucine aminopeptidase).
  - Soil particle size distribution (laser diffraction with OC removal) and aggregate size distribution; SOM density fractionation into LP (light particulate), OP (occluded particulate), MA (mineral-associated), and DOM fractions; carbon and nitrogen content for each fraction; C:N ratios.
  - Microbial analyses: amplicon sequencing (16S rRNA; ITS2) and shotgun metagenomics; derived community composition metrics (OTU-like counts, NMDS axes) and functional gene profiles; fungi-to-bacteria ratio metrics.
  - Supplemental data: grid-level ANPP and litter depth with site- and grid-specific metadata; soil metrics for topsoil (0–15 cm) and subsoil (below 50 cm) for cross-site comparability.

- Data quality, completeness, and controls
  - Completeness: common soil metrics complete; less common/expensive measurements limited to some layers or grids; missing values marked NA.
  - Quality control: use of UKAS-accredited SOPs (e.g., SOP3102) for carbon, nitrogen, and related nutrients; internal standards and replicates for EC, pH, LOI; cross-checks with reference materials.
  - Lab processing notes: some measurements (e.g., microbial biomass, certain enzymes) impacted by logistic constraints or sample preservation (e.g., freezing) leading to unreliable data for those analyses; such issues documented in data notes.
  - Metadata and data structure: explicit linking of sample IDs to site/plot/grid and coordinates; supplementary location files enable spatial alignment and re-projection if needed.

- Analytical approaches and outputs
  - ANPP: predicted from LDMC with site-specific calibration; provides mean and 95% credible intervals from converged MCMC chains.
  - Soil hydraulic properties: HYPROP-derived water release curves, active pore size, saturated hydraulic conductivity; field and lab measurements harmonized through HYPROP-FIT software.
  - SOM fractions: density fractionation data (LP, OP, MA, DOC) with corresponding C and N contents and C:N ratios; enzyme activities standardized to µmol g-1 soil h-1 where available.
  - Microbial data: processing of 16S and ITS amplicons; metagenomic readouts; ordination scores (NMDS) for bacteria, fungi, and functional genes; fungi-to-bacteria ratio metrics.
  - Earthworms: species-level counts and biomass totals; location-based aggregations available.

- Data accessibility and reuse
  - Datasets are organized for cross-site comparability and model integration; two connector files plus four main data files enable assembly of a complete, co-located dataset.
  - Sequence data and metagenomes deposited in ENA under project PRJEB66294; derived microbiome metrics provided within the soil metrics dataset.
  - Some data (e.g., certain earthworm data or specific site measurements) may be accessible through partner institutions (e.g., Forest Research) or site-specific files.
  - Projects and机构: UK-SCAPE programme (NE/R016429/1) with collaborations from UKCEH and Forest Research; supplementary materials in Supplements A–C document field-site specifics, coring details, and measurement planning.

- Notable site and data design details
  - Five England sites chosen to span grassland–woodland contrasts with varying species and management histories; site selection emphasized age of woodland, management history, transect confounding controls, and access feasibility.
  - Transect-based sampling designed to capture proximity effects from trees and to quantify horizontal gradients relative to the land-use boundary.
  - Data structure includes both topsoil-focused datasets (0–15 cm) and deeper soil layers, enabling analysis of SOC dynamics over depth and across soil types.

- Practical implications for data strategy and governance
  - Rich, multi-modal SOC dataset suitable for process-based SOC modelling, policy-relevant land-management assessment, and cross-site meta-analyses.
  - Importance of robust metadata, consistent depth interval definitions, and clear linking identifiers to maintain cross-dataset integration and reproducibility.
  - Potential data access considerations: some datasets and analyses are governed by partner institutions; best-practice data-sharing agreements and provenance tracking recommended.
  - Data Leaders should consider implementing standardized metadata schemas, data provenance workflows, and tiered access controls to maximize reuse while respecting site-specific restrictions.

- Acknowledgments
  - Funded by the Natural Environment Research Council as part of UK-SCAPE; collaborations with Forest Research; data generation and processing across UKCEH laboratories.