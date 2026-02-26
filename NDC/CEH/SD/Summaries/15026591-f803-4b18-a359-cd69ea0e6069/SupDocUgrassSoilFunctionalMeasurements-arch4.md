# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) Soil functional measurements (enzymatic activities) across geo linked sampling locations, on grassland, UK (2016)

## Executive summary
- Study of enzymatic activity in soils from paired intensive and extensive grassland systems across 32 UK sites, including variations in soil pH and land-use.
- Samples collected in winter and spring 2015-2016 and analysed for eight extracellular hydrolytic enzyme activities using fluorescent substrates.
- Enzymes measured: Acetate Esterase, Fluorescein diacetate hydrolysis, β-glucosidase, Arylsulfatase, Phosphatase, Leucine aminopeptidase, Chitinase, Lipase.
- Analysis conducted at CEH Wallingford; data compiled into a CSV for deposition into the EIDC.
- Project context within NERC U-GRASS aims to understand soil functional change under different management and climatic scenarios, linking soil biodiversity, properties, and functionality to ecosystem services.

## Protocols

### 2.1 Soil sampling
- 32 UK sites selected to contrast land-use intensity (low vs high).
- Soil cores (15 cm x 5 cm) collected along 100 m land-use interface, every 25 m, yielding 5 paired replicates per site.
- Sampling conducted November 2015 to February 2016.
- Cores stored frozen at -20°C prior to chemical, physical, molecular, and functional analyses.

### 2.2 Enzyme activity
- Measured by CEH Wallingford using fluorescent substrates.
- Enzyme set and functional associations:
  - Acetate Esterase (global activity / plant hemicellulose degradation)
  - Fluorescein diacetate hydrolysis (microbial activity potential)
  - β-glucosidase (cellulose-derived glucose release)
  - Arylsulfatase (sulfur cycle & mineralization)
  - Phosphatase (phosphorus mineralization)
  - Leucine aminopeptidase (protein degradation)
  - Chitinase (chitin degradation)
  - Lipase (lipid degradation)
- Procedure: soil slurry (1.5 g soil + 20 mL deionized water) mixed, added to 96-well plates with substrate, incubated at 28 °C for 4 hours; fluorescence read every 30 minutes.
- Replicates: three methodological replicates per sample plus quenched standards; fluorescence controlled against blanks and degradation over time.
- Output units: nmol of product per minute per gram of dry soil (EEA on a dry soil mass basis).

## Data structure

- File format: flatbed CSV.
- Size: 450 data rows, 12 columns.
- Key columns:
  - id: unique cross-reference identifier
  - management_intensity: qualitative land-use management
  - Latitude, Longitude: GPS coordinates
  - ace: acetate esterase activity
  - fda: fluorescein diacetate hydrolysis
  - glu: β-glucosidase
  - sul: arylsulfatase
  - pho: phosphatase
  - leu: leucine aminopeptidase
  - chin: chitinase
  - lip: lipase
  - NA: indicates data not recorded
- Data are reported as nmol of product per minute per gram of dry soil for each enzyme.

## Associated files

- UgrassSoilFunctionalMeasurements.csv

## Data provenance and context

- Lineage: 32 grassland sites across the UK; samples stored at -20°C before processing for multiple characteristics; enzyme activities measured and results compiled into a CSV and deposited in EIDC.
- Relevance: supports understanding of how soil biodiversity and biogeochemical processes respond to land management and climatic variation, informing soil security and ecosystem service assessments.
- Potential uses for data leaders:
  - Integrate with broader soil function datasets to map service provision across landscapes.
  - Benchmark soil enzymatic activity as indicators of soil health under different management regimes.
  - Develop data governance and metadata standards to ensure discoverability, interoperability, and reproducibility across soil function studies.