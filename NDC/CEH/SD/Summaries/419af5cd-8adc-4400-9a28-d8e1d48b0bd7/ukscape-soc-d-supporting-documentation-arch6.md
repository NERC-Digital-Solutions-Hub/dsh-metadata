SOC-D: Soil Organic Carbon Dynamics Data Description and Methods

Overview
- Aims to understand biotic and abiotic controls on soil organic carbon (SOC) dynamics across UK grassland–woodland contrasts.
- Five long-term site contrasts across England (Gisburn-1, Gisburn-2, Alice Holt, Wytham Woods, Kielder Forest) sampled between 2018–2021.
- Collects co-located aboveground and belowground measurements to test SOC sensitivity to climate/land management and to identify drivers of SOC stability and storage.
- Outputs include four main data areas: aboveground productivity, soil physical/chemical/biological properties, soil hydraulic properties, and earthworm data, plus extensive microbial and soil organic matter (SOM) fraction data.

Study design and sites
- Contrasts: each site comprises a grassland plot (Plot 1) and a woodland plot (Plot 2); contrasts sampled to capture edge effects and tree-soil interactions.
- Transect/grid layout: within each plot, the area is divided into six grids (Grids 1–3 in grassland, Grids 4–6 in woodland) with the boundary between Grids 3 and 4; sampling locations are randomized within each grid.
- Sampling points: 9 locations per plot (18 per grassland–woodland contrast).
- Timeframe and measurements:
  - 2018–2019: field sampling for soil cores (0–100 cm) and initial site measurements.
  - 2020–2021: additional measurements for infiltration, earthworms, and aboveground productivity.
  - Aboveground net primary productivity (ANPP) and litter layer depth measured; ANPP used leaf dry matter content (LDMC) with cover-weighted LDMC as predictor.
- Sites and context:
  - Gisburn-1: grazed grassland x conifer
  - Gisburn-2: ungrazed grassland x broadleaf
  - Alice Holt: grazed grassland x broadleaf
  - Wytham Woods: grazed grassland x broadleaf
  - Kielder Forest: unmanged grassland x conifer
- Site selection criteria focused on woodland age, management history, plot size, and accessibility, ensuring representative UK land-use–soil combinations.

Datasets and key variables
- Four main dataset groups (plus connectors):
  - ANPP and litter depth (0–5 cm in some grids; 0–15/30 cm in others)
  - Soil physical, chemical, and biological properties (0–100 cm; up to six depth increments)
  - Soil hydraulic properties (hydraulic conductivity Kfs and HYPROP-derived curves; pF curves)
  - Earthworm counts and species IDs (ecology of soil biota)
- Supplemental datasets:
  - Soil organic matter density fractionation (SOM fractions: LP, OP, MA; plus dissolved organic carbon DOM)
  - Soil texture and size distribution (PSD, LD, clay/silt/sand fractions; LD/ASD)
  - Enzyme activities (cellulolytic, chitinase, leucine aminopeptidase, phosphatase, phenol oxidase) for select sites
  - Microbial ecology data (amplicon sequencing of bacteria 16S, fungi ITS; metagenomics)
  - SOC-D linking files to connect sample IDs with site, plot, grid, and location coordinates
- Data availability notes:
  - Raw and derived microbial sequencing data deposited in ENA under PRJEB66294
  - NA values used where measurements were not collected or not analysed (documented in methods)

Collection methods and field workflow
- Field layout and sampling
  - Homogeneous vegetation and slope chosen per grassland–woodland contrast; sampling points selected within grids to minimize confounding proximity to trees.
  - A randomized map and GPS coordinates guided the sampling matrix, enabling calculation of distance to transition boundary and sampling point spacing.
  - In-field selection refined to consider proximity to trees, slope, etc.
- Soil cores and depth increments
  - Deep soil cores (0–100 cm) collected with multiple approaches:
    - Mineral soils: Cobra precision corer (0–100 cm or 30–100 cm), sometimes split into 0–30 cm plus 30–100 cm using a Split Tube Sampler for compaction concerns.
    - Peat/wet soils: Russian auger (0–50 cm and 50–100 cm combined).
  - Topsoil increments: 0–5 cm and 5–15/30 cm depending on site planning and soil type.
  - Depth increments defined per site for lab analyses: generally 0–5 cm, 5–15/30 cm, 15–30 cm, 30–50/60 cm, and 50/60–100 cm.
- In-field measurements
  - HyPROP cores (0–5 cm; 30–35 cm at some sites) for soil water release curves and saturated hydraulic conductivity.
  - Unsaturated hydraulic conductivity measured in the field with mini-disk infiltrometer (grids 2 and 5).
  - Earthworms collected via hand-sorting, sorted in the field, weighed, and identified in the lab.
  - Litter depth measured around sampling points.
- Aboveground productivity sampling
  - ANPP estimated from fresh leaf material collected May–July 2021 (longer at higher latitudes/altitudes); LDMC values used to predict ANPP via LDMC-based regression.
- Sample processing and storage
  - All samples stored at 4°C until analyses; a structured processing flow ensures samples are prepared consistently across depth increments.

Analytical methods and quality control
- Soil properties and nutrient metrics
  - Total carbon and nitrogen: elemental analysis (Vario EL) on air-dried samples.
  - Phosphorus: acid digestion and colorimetric measurement.
  - Nitrate (NO3-N) and dissolved organic carbon (DOC): standard extraction and analysis workflows.
  - Cation exchange capacity (CEC): ammonium acetate extraction with ICP-OES; NH4–N and NH3–N measured via colorimetric methods with calibration and QC standards.
  - pH (DIW and CaCl2), electrical conductivity (EC), and bulk density (BD) calculated from core samples.
  - Loss-on-ignition (LOI) and soil moisture via thermogravimetric analysis (TGA) for SWC and SOM estimation.
- Particle size distribution and texture
  - PSD measured by laser diffraction after organic matter removal; textures reported as clay, silt, sand fractions and additional <53 μm and <2 μm fractions for comparability.
  - Aggregate size distribution (ASD) obtained from laser data; attention to occluded organic matter in aggregates.
- SOM fractions
  - Density fractionation using sodium polytungstate (SPT) to separate DOM, LP (light particulate), OP (occluded), and MA (mineral-associated) fractions.
  - Each fraction analyzed for total C and N; C:N ratios computed (LP-C, OP-C, MA-C and corresponding N fractions); ES activities and EC-to-N/P ratios reported when available.
- Enzyme activities
  - Hydrolytic enzymes (β-glucosidase, N-acetylglucosaminidase, leucine aminopeptidase, phosphatase) and oxidative enzyme (phenol oxidase) assayed with fluorogenic or colorimetric substrates.
  - Data quality: some sites excluded due to buffer issues; results reported only for comparable sites.
- Microbial ecology
  - DNA extraction from soil, amplicon sequencing (16S rRNA for bacteria; ITS2 for fungi) and shotgun metagenomics.
  - Data processing: OTU/ASV generation with DADA2; taxonomic and functional annotation; ordination analyses (NMDS) and related sample metrics provided.
  - Ratios such as fungi-to-bacteria derived from metagenomic reads; data linked to soil layers and sample IDs.
- Data integration and provenance
  - Two connectors: SOC-D_DATABASE_CONNECTOR.csv to join sample IDs with site/plot/grid/location details; SOC-D_DATABASE_LOCATIONS.csv containing location coordinates and reference IDs.
  - Datasets 2–5 house the main measurements (ANPP, litter; common soil metrics; soil metrics grid2/grid5; hydraulic data; earthworms).
  - Missing values recorded as NA; metadata describes measurement scope, depth increments, and site-specific adjustments.

Data structure and accessibility
- File structure
  - SOC-D_DATABASE_CONNECTOR.csv: 14 columns; 458 rows linking site, land use, plot, grid, core, transition distance, lateral distance, slice, lab layer, and location/sample IDs.
  - SOC-D_DATABASE_LOCATIONS.csv: 6 columns; 91 rows with location IDs and OS grid references/lat-long coordinates.
  - SOC-D_DATABASE_ANPP.csv and SOC-D_DATABASE_LITTER_DEPTH.csv: ANPP estimates and litter depths with 88–91 rows, linked by LOCATION_ID.
  - SOC-D_DATABASE_COMMON_SOIL_METRICS.csv and SOC-D_DATABASE_SOIL_METRICS_GRID2_GRID5.csv: extensive soil metrics across depths with 458 rows and 170 rows respectively.
  - SOC-D_DATABASE_SOIL_HYDRAULIC_CONDUCTIVITY.csv and HYPROP-related files: field and lab hydraulic data; multiple files for raw HYPROP outputs and derived K values.
  - SOC-D_DATABASE_EARTHWORMS.csv: earthworm counts and biomass per location; detailed species-level counts.
  - Supplementary materials describe site images, field sheets, core-hole details, and additional methods.
- Data availability and usage notes
  - Datasets include both raw and derived metrics; some data were excluded or flagged due to methodological issues (e.g., Gisburn enzyme buffers) and are annotated accordingly.
  - All data values are NA where not collected or not analysed; data are suitable for cross-site comparisons and process-based SOC modelling.

Analytical scope and objectives
- Core questions addressed by the SOC-D program:
  - Question 1: How sensitive is SOC to local/global climate and land-management changes?
  - Question 2: What are the critical feedbacks between SOC, soil structure, chemistry, and functional biota?
  - Question 3: Which soil metrics and modelling approaches best reflect modern SOC dynamics?
  - Question 4: Which UK areas are at risk of SOC loss and where can SOC be enhanced through management?
- Outputs are designed to feed a modular, process-based SOC dynamics model that can be embedded in larger community soil models.
- The dataset supports testing biotic–abiotic interactions, including the role of soil biota (earthworms, microbes) and physical structure in SOC storage and turnover across realistic UK land-use gradients.

Notes and acknowledgments
- Funding and collaboration: UK-SCAPE programme (NE/R016429/1) and ERAMMP/GMEP/UGRASS collaborations; thanks to Forest Research for access at multiple sites.
- Data limitations and caveats: some measurements excluded or partially collected at certain sites; microbial biomass data affected by freezing; some enzyme data limited to select sites for comparability.

Supplementary references and project context
- The dataset builds on established soil science methods (LOI, BD, CEC, PSD, SOM fractions), HYPROP laboratory methods, and standard microbial ecology pipelines (16S/ITS sequencing, metagenomics).
- Links to related projects and resources (ELUM, GMEP, UGRASS, ERAMMP) for broader context and modelling efforts.