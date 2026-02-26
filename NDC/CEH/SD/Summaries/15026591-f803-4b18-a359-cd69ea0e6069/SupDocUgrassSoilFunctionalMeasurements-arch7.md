# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) Soil functional measurements (enzymatic activities) across geo linked sampling locations, on grassland, UK (2016)

## Executive summary
- Study of soil enzymatic activity from paired intensive and extensive grassland systems across 32 UK sites, collected during winter/spring 2015–2016.
- Measured extracellular hydrolytic enzyme activities using fluorescent substrates for eight enzymes (acetate esterase, FDA hydrolysis, β-glucosidase, arylsulfatase, phosphatase, leucine aminopeptidase, chitinase, lipase).
- Analyses performed at CEH Wallingford to understand soil functional changes under varying management and climatic scenarios; part of the NERC U-GRASS Soil Security Programme.
- Spatial data framework designed for map-based visualization: 32 geo-referenced grassland sites across the UK with sampling along land-use interfaces.
- Output data prepared as a CSV (UgrassSoilFunctionalMeasurements.csv) for deposition into data repositories (EIDC), enabling GIS-style analyses and mapping of enzyme activities.

## Protocols

- 2.1 Soil sampling
  - 32 sites with land-use contrasts (low vs high intensity).
  - Soil cores (15 x 5 cm) collected along a 100 m interface, every 25 m (five paired replicates per site).
  - Sampling period: November 2015 – February 2016; samples stored at -20°C prior to processing.

- 2.2 Enzyme activity
  - Enzyme activities measured as nmol of product per minute per g dry soil (EEA on dry soil basis).
  - Enzymes measured (with linked processes): acetate esterase, FDA hydrolysis, β-glucosidase, arylsulfatase, phosphatase, leucine aminopeptidase, chitinase, lipase.
  - Assay method: soil slurry (1.5 g soil with 20 mL DI water) incubated with substrate solution in 96-well plates; 4-hour incubation at 28°C; fluorescence read every 30 minutes.
  - Quality controls: triplicate methodological replicates and quenched standards; fluorescence checks to monitor enzyme stability over the assay.
  - Instrumentation: Cytation 5 spectrophotometer with automated incubator; specific excitation/emission settings per substrate.

## Data structure

- Data file: UgrassSoilFunctionalMeasurements.csv
- Structure: flat CSV with 450 data rows and 12 columns.
- Key fields:
  - id: unique cross-reference identifier
  - management_intensity: qualitative descriptor of land-use management
  - Latitude, Longitude: GPS coordinates
  - ace: acetate esterase activity
  - fda: fluorescein diacetate hydrolysis (overall microbial activity potential)
  - glu: β-glucosidase (glucose release from cellulose)
  - sul: arylsulfatase (sulfur cycle/mineralization)
  - pho: phosphatase (phosphorus mineralization)
  - leu: leucine aminopeptidase (protein degradation)
  - chin: chitinase (chitin degradation)
  - lip: lipase (lipid degradation)
- NA values indicate data were not recorded.

## Associated files
- Analysis outputs: UgrassSoilFunctionalMeasurements.csv

## Context and applications for GIS
- Enables spatial mapping and comparison of soil functional potential across managed grassland landscapes in the UK.
- Supports exploration of relationships between enzyme activities and management intensity, climate context, and soil properties at differing geographic locations.
- Provides georeferenced data suitable for integration with other spatial layers to assess soil ecosystem services and resilience under land-use change.