SOC-D: Soil Organic Carbon Dynamics - Data Description

Overview
- A comprehensive data package from the SOC-D project investigating biotic and abiotic controls on soil organic carbon (SOC) dynamics across five grassland-to-woodland contrasts in England (2018–2021).
- Co-located aboveground and belowground measurements, including ANPP, litter depth, soil chemical/physical properties (0–100 cm), soil hydraulic properties, earthworm counts, and molecular microbial data.
- Aims to understand SOC sensitivity to climate/land-management changes, links between SOC, soil structure/biota/chemistry, and to identify UK regions at SOC risk or with storage potential.

Datasets and data structure
- Datasets (produced across five contrasts/sites):
  - Aboveground Net Primary Productivity (ANPP) and litter layer depth (0–5 cm and other depths as specified).
  - Soil properties (chemical, physical, biological) for 0–100 cm across up to six depth increments.
  - Soil hydraulic conditions: soil water release curves (HYPROP) and unsaturated hydraulic conductivity (K) measurements.
  - Earthworm counts and biomass, by species.
  - Microbial data: amplicon sequencing (16S rRNA for bacteria, ITS2 for fungi) and metagenomes (ENA PRJEB66294) with derived community composition and functional metrics.
  - Density-fractionated SOC pools (LP, OP, MA) and associated C/N metrics; dissolved organic carbon (DOC) and related soil chemistry (NO3-N, NH4-N, CEC, etc.).
  - Extracellular enzyme activities (limited to selected sites: Alice Holt, Wytham Woods, Kielder Forest).
- Data access and linking:
  - Central data connector file: SOC-D_DATABASE_CONNECTOR.csv (layout, sampling geometry, transition distances, grids, sample IDs).
  - Location file: SOC-D_DATABASE_LOCATIONS.csv (site IDs, coordinates, grid references).
  - Site- and measurement-specific files:
    - SOC-D_DATABASE_ANPP.csv (ANPP estimates and LDMC-derived predictions).
    - SOC-D_DATABASE_LITTER_DEPTH.csv (three-point litter depth means per location).
    - SOC-D_DATABASE_COMMON_SOIL_METRICS.csv (top-level 0–1 m soil metrics for all sites).
    - SOC-D_DATABASE_SOIL_METRICS.csv and SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv (detailed soil metrics across depths; grid-specific topsoil/subsoil data).
    - SOC-D_DATABASE_SOIL_HYDRAULIC_CONDUCTIVITY.csv (field-measured Kfs by location).
    - HYPROP_RETENTION_T_PF.csv / HYPROP_CONDUCTIVITY_K_PF.csv / HYPROP_CONDUCTIVITY_K_T.csv (HYPROP raw data and processed outputs).
    - SOC-D_DATABASE_EARTHWORMS.csv (earthworm counts and biomass by species).
  - DNA/RNA data: sequencing/omics data deposited in ENA PRJEB66294; pre-processed metrics included (nMDs, OTUs, metagenome reads, and taxonomic/functional annotations).
- Missing data:
  - Missing values marked as NA; some measurements absent at certain sites/grids (notably enzyme data due to field issues or buffer errors).
  - Topsoil depth definitions adapted (0–5 cm or 0–15 cm depending on site) to ensure material availability and alignment with national datasets.

Sites and sampling design
- Five grassland-to-woodland contrasts across England:
  - Gisburn-1, Gisburn-2 (North England); Alice Holt (South); Wytham Woods (South); Kielder Forest (North).
- Each site has two plots: grassland (plot 1) and woodland (plot 2); each plot divided into three grids (grassland grids 1–3; woodland grids 4–6) with nine sampling locations per grid, totaling 18 sampling locations per site.
- Sampling window:
  - Field soil cores collected Nov 2018–Mar 2019.
  - Additional measurements (infiltration, earthworms, ANPP) conducted 2020–2021.
- Core types and depth coverage:
  - 1-m soil cores in most sites; depth increments include 0–5, 5–15, 15–30, 30–50/60, and 50/60–100 cm.
  - Site-specific variations (e.g., Wytham/Woodland HYPROP at 0–5 and 30–35 cm; topsoil measurements at 0–15 cm in some locations).
- Aboveground measurements:
  - ANPP estimated from leaf LDMC of dominant species (cover-weighted LDMC) using regression linked to Smart et al. (2017) model.
  - Litter depth measured at three sub-sampling points around each location.

Collection methods and quality control
- Soil sampling and processing:
  - Pre-defined field contrast with randomized sampling points within grids.
  - Infiltration and HYPROP measurements conducted in grids 2 and 5; earthworms sampled by hand-sorting; litter depth recorded.
  - Soil cores prepared via multiple methods (Hyprop cores, national survey cores, Split Tube, Cobra precision corer, Russian auger) depending on depth and soil type.
  - Depth increments standardized to enable cross-site comparability; adjustments made for peat and mineral boundaries where applicable.
- Laboratory analyses:
  - Bulk density (BD), pH (DIW and CaCl2), electrical conductivity (EC) using DIW suspensions with QA controls (internal standards, duplicates).
  - LOI via thermogravimetric analysis (TGA) to estimate soil organic matter content.
  - Total C and N by elemental analyzer (Vario-EL); total P by acid digestion and colorimetric detection; NO3–N and DOC via standard extraction and analysis workflows.
  - CEC via ammonium acetate extraction and ICP-OES; NH4–N and related ammoniac measurements by colorimetry.
  - PSD and aggregate size distribution via laser diffraction; OM removal steps for PSD; cross-check with sieve data for sand fraction.
  - SOM density fractionation into DOC, LP, OP, MA fractions with sodium polytungstate (SPT) density fractionation; carbon and nitrogen quantified by elemental analysis for LP/OP/MA fractions.
  - Extracellular enzyme activities (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase, phenol oxidase) at selected sites with fluorescence/absorbance readouts; treated with site-specific buffers; QA excluded Gisburn data due to buffer mismatch.
  - Microbial community profiling:
    - DNA extraction from 0.2 g (topsoil) and 2.5 g (subsoil) samples; amplicon sequencing for bacteria (16S V4-V5) and fungi (ITS2); metagenomic sequencing for functional genes.
    - Sequence processing via DADA2 (OTU/ASV), Kraken2 taxonomic annotation, and meta-omics analyses; outputs include ordination scores (NMDS), and microbial biomass proxies.
- Quality controls and issues:
  - Use of internal standards, duplicates, and blanks across chemical analyses; LOI QA with in-batch controls.
  - Enzyme data incomplete for Gisburn; enzyme buffers incorrect at Gisburn sites leading to exclusion from cross-site comparisons.
  - Microbial biomass and CUE measurements faced logistics constraints (sample freezing affected microbial biomass interpretations).
  - LAB and field notes include coring depth consistency checks and documentation of compaction issues where relevant.

Data governance, provenance, and accessibility
- Program context:
  - Funded under UK-SCAPE (National Capability) with project NE/R016429/1; data underpin a modular SOC dynamics model and national-scale interpretation.
  - Sequencing data deposited in ENA (PRJEB66294); other data prepared for deposition in UKCEH data repositories.
- Data management and documentation:
  - Extensive metadata framework including site coordinates, grid layouts, core IDs, sample IDs, and depth slices.
  - Data files include explicit linkage identifiers (LOCATION_ID, SAMPLE_ID, CORE/LAYER) to enable cross-dataset joins (connectors and location table).
  - Data files specify units and descriptions for all variables; NA values indicate missing measurements.
- Intended use and reuse:
  - Datasets designed for integration into open-access soil datasets for UKCEH and for use in SOC modeling and policy-relevant analyses.
  - Clear pathways for re-use include linking ANPP, litter depth, soil physical/chemical properties, hydraulic properties, earthworm data, and microbial data for SOC turnover and storage analyses.
- Documentation and supplementary materials:
  - Supplement A–C provide field mapping, coring details, and measurement prioritization/analysis notes.
  - Supplementary references detailing measurement methods, QA, and data interpretation.

Key considerations for Data Stewards
- Metadata completeness and consistency:
  - Ensure linking keys (SITE_NAME, LOCATION_ID, PLOT, GRID, CORE, SLICE, LAB_LAYER_cm) are preserved for cross-dataset joins.
  - Maintain clear records of depth increments and any site-specific deviations (e.g., 0–5 vs 0–15 cm topsoil; 15–60 cm adjustments).
- Data quality and provenance:
  - Preserve QA flags (e.g., Gisburn enzyme data exclusion) and document any post-hoc data corrections or methodological changes.
  Ensure raw HYPROP data, K data, and derived curves are stored with traceable processing steps (HYPROP-FIT/SHYPFIT outputs).
- Access and licensing:
  - Coordinate with UKCEH data portals and ENA to ensure appropriate access permissions, embargo periods (if any), and usage licenses; maintain clear data provenance and attribution requirements.
- Dataset completeness and curation:
  - Monitor gaps or NA entries across datasets; consider implementing a data completeness report to accompany dataset releases.
  - Align with national soil datasets (e.g., Countryside Survey, LUCAS) by preserving defined topsoil depth conventions and ensuring compatibility where possible.

Notes on scope and limitations
- The five-site design, while enabling cross-site SOC comparisons, includes site-specific data limitations (e.g., limited depth coverage for some measurements; selective measurement of enzymes and microbial metrics).
- Some data are not directly comparable across sites due to methodological differences (e.g., enzyme buffers, sampling logistics) and have site-specific QA notes.
- The dataset is intended as a foundation for SOC process understanding and modeling, with explicit documentation to support re-use and integration with broader UK soil data resources.