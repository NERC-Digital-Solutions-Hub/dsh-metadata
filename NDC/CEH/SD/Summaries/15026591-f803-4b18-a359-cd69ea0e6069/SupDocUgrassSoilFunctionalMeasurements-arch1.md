# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) Soil functional measurements (enzymatic activities) across geo linked sampling locations, on grassland, UK (2016)

## Executive summary
- Study of soil enzymatic activity from paired intensive and extensive grassland systems across 32 UK sites, including low and high pH parent soils.
- Sampling conducted in winter and spring 2015–2016; analyses performed on extracellular hydrolytic enzyme activities.
- Enzymes measured using fluorescent substrates: Acetate Esterase, Fluorescein diacetate hydrolysis, β-glucosidase, Arylsulfatase, Phosphatase, Leucine amino peptidase, Chitinase, Lipase.
- Conducted at CEH Wallingford to explore soil functional change under different management and climate scenarios as part of the NERC U-GRASS Soil Security Programme (NE/M017125/1).

## Data collection and methods

### Soil sampling
- 32 UK grassland sites chosen with land-use contrast (low vs high intensity) at each site.
- Soil cores (15 x 5 cm) collected along 100 m land-use interface, every 25 m, yielding 5 paired samples per site.
- Sampling window: November 2015 – February 2016.
- Samples stored frozen at -20°C prior to processing for chemical, physical, molecular, and functional analyses.

### Enzyme activity measurements
- Conducted by CEH Wallingford.
- Units: nmol of product per minute per gram of dry soil (extracellular enzyme activity, dry soil basis).
- Enzymes assayed (functions in parentheses): 
  - Acetate Esterase (global activity/plant hemicellulose degradation)
  - Fluorescein diacetate hydrolysis (microbial activity potential)
  - β-glucosidase (release of glucose from cellulose)
  - Arylsulfatase (sulfur cycle/mineralization)
  - Phosphatase (phosphorus mineralization)
  - Leucine aminopeptidase (protein degradation)
  - Chitinase (chitin degradation)
  - Lipase (lipid degradation)
- Protocol: soil slurry preparation, fluorescence-based substrate assays in 96-well plates; measurements every 30 minutes over 4 hours at 28°C.
- Quality controls: three methodological replicates per sample plus quenched standards; controls to monitor fluorescence drift; calibration with 4-MUB or 7-AMC standards.
- Equipment: Cytation 5 spectrophotometer with automated incubator; fluorescence measurements at specific excitation/emission settings for each substrate.

## Data structure and contents

- File format: flat CSV (UgrassSoilFunctionalMeasurements.csv) with 450 data rows and 12 columns.
- Columns (descriptions):
  - id: unique cross-referencing identifier
  - management_intensity: qualitative description of land-use management
  - Latitude: GPS latitude
  - Longitude: GPS longitude
  - ace: acetate esterase activity (nmol min⁻¹ g⁻¹ dry soil)
  - fda: fluorescein diacetate hydrolysis activity (nmol min⁻¹ g⁻¹)
  - glu: β-glucosidase activity (nmol min⁻¹ g⁻¹)
  - sul: arylsulfatase activity (nmol min⁻¹ g⁻¹)
  - pho: phosphatase activity (nmol min⁻¹ g⁻¹)
  - leu: leucine aminopeptidase activity (nmol min⁻¹ g⁻¹)
  - chin: chitinase activity (nmol min⁻¹ g⁻¹)
  - lip: lipase activity (nmol min⁻¹ g⁻¹)
- NA values indicate data not recorded.

## Provenance and data availability

- Lineage: samples collected from 32 grassland sites, stored at -20°C, processed for chemical, physical, molecular, and functional measurements; results compiled into an Excel file and exported as CSV for deposition.
- Data outputs: UgrassSoilFunctionalMeasurements.csv.
- Publication/hosting context: part of the U-GRASS project within the NERC Soil Security Programme; data deposited for reuse and analysis.

## Potential uses and analytical opportunities

- Assess relationships between management intensity and soil enzyme activities across different soil types and climatic contexts.
- Develop predictive models linking biodiversity, soil properties, and enzyme-mediated soil functions under various land-use scenarios.
- Combine with other datasets (chemical/physical properties) to evaluate soil functional resistance and resilience to management and climate change.
- Support meta-analyses on how soil biodiversity and edaphic status influence biogeochemical processes and ecosystem services.

## Key considerations and challenges for analysts

- Spatial scale and heterogeneity: 32 sites with site-level contrasts but potential variability within sites; careful handling of scale when modeling.
- Data completeness: some NA values; need to account for missing data in analyses.
- Measurement context: enzyme activities are potential activities under controlled conditions and may not directly translate to in-situ rates.
- Integration with broader datasets: potential to link enzyme data with soil organic matter, climate, and land management records for robust inference.