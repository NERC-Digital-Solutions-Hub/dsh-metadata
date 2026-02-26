# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) Soil functional measurements (enzymatic activities) across geo linked sampling locations, on grassland, UK (2016)

## Executive summary
- 32 grassland sites across the UK, with land-use contrasts between low and high intensity management.
- Paired intensive and extensive systems sampled during winter and spring 2015–2016 to assess extracellular hydrolytic enzyme activities.
- Enzymes measured using fluorescent substrates: acetate esterase, fluorescein diacetate hydrolysis, β-glucosidase, arylsulfatase, phosphatase, leucine aminopeptidase, chitinase, and lipase.
- Analyses performed at CEH Wallingford; data collected under the NERC U-GRASS Soil Security Programme.
- Data collected to understand soil functional change under different management and climatic scenarios; results compiled into a CSV and deposited into the EIDC.
- Samples stored at -20°C prior to processing; data lineage and processing documented to support transparency and reuse.

## Protocols

### 2.1 Soil sampling
- 32 UK sites chosen with a land-use contrast (low vs. high intensity practices) at the interface.
- Soil cores (15 cm × 5 cm) collected along 100 m of the land-use interface, every 25 m (5 paired replicates per site).
- Sampling period: November 2015 to February 2016; cores stored frozen at -20°C before further processing.

### 2.2 Enzyme activity
- Enzyme activities assessed by CEH Wallingford; units: nmol of product per minute per gram of dry soil.
- Enzymes and associated processes:
  - Acetate esterase (global activity/plant hemicellulose degradation)
  - Fluorescein diacetate hydrolysis (microbial activity potential)
  - β-glucosidase (glucose release from cellulose)
  - Arylsulfatase (sulfur cycle and mineralization)
  - Phosphatase (phosphorus mineralization)
  - Leucine aminopeptidase (protein degradation)
  - Chitinase (chitin degradation)
  - Lipase (lipid degradation)
- Procedure per soil sample:
  - Prepare slurry with 20 mL deionized water and 1.5 g soil; shake to create slurry.
  - Add 30 µL soil slurry to 170 µL substrate solution in 96-well plates; incubate 4 hours at 28°C in the dark.
  - Kinetic fluorescence measured every 30 minutes (instrument: Cytation 5 with BioSpa 8 incubator) at substrate-specific wavelengths.
  - Methodological replicates include sample+buffer+substrate and quenched standards (4-MUB or 7-AMC); fluorescence controls to monitor degradation.
  - Enzyme activities calculated as nmol product per minute per g of dry soil.

## Data structure
- File: UgrassSoilFunctionalMeasurements.csv
- Content: 450 data rows, 12 columns.
- Key columns:
  - id: unique cross-reference identifier
  - management_intensity: qualitative descriptor of land-use management
  - Latitude, Longitude: GPS coordinates
  - ace: acetate esterase activity
  - fda: fluorescein diacetate activity (overall microbial activity potential)
  - glu: β-glucosidase (glucose release from cellulose)
  - sul: arylsulfatase (sulfur cycling)
  - pho: phosphatase (phosphorus mineralization)
  - leu: leucine aminopeptidase (protein degradation)
  - chin: chitinase (chitin degradation)
  - lip: lipase (lipid degradation)
- Units: nmol of product per minute per g of dry soil (EEA on a dry soil mass basis)
- NA indicates data not recorded

## Associated files
- UgrassSoilFunctionalMeasurements.csv (data outputs)
- Protocols and data structure details are documented to support data reuse, integration with monitoring frameworks, and governance.