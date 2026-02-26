# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) Soil functional measurements (enzymatic activities) across geo linked sampling locations, on grassland, UK (2016)

## Executive summary
- Study across 32 grassland sites in the UK, with land-use contrasts (intensive vs. extensive management) and varying soil pH, sampled in winter–spring 2015–2016.
- Measured extracellular hydrolytic enzyme activities using fluorescent substrates to assess eight enzymes: acetate esterase, fluorescein diacetate hydrolysis, β-glucosidase, arylsulfatase, phosphatase, leucine aminopeptidase, chitinase, and lipase.
- Analyses conducted at CEH Wallingford; data compiled into an Excel workbook and exported as a CSV for deposition into the Environmental Information Data Centre (EIDC).
- Aimed to understand how soil functional properties respond to management and climatic scenarios, linking biodiversity, soil properties, and ecosystem services under different geographic and climatic contexts.
- Data outputs support broader insights into soil function resilience and inform management decisions to balance soil organic matter, nutrient cycling, and productivity.

## Protocols

### 2.1 Soil sampling
- 32 UK sites chosen with a land-use intensity contrast (low vs. high intensity) near the land-use interface.
- Soil cores (15 cm x 5 cm) collected along 100 m with sampling every 25 m, yielding 5 paired replicates per site.
- Sampling conducted November 2015 to February 2016; cores stored frozen at -20°C prior to processing for chemical, physical, molecular, and functional analysis.

### 2.2 Enzyme activity
- Enzyme activities measured at CEH Wallingford.
- Units: nmol of product per minute per g of dry soil (EEA on a dry soil mass basis).
- Enzymes measured (with functional context):
  - Acetate esterase (global activity/plant hemicellulose degradation)
  - Fluorescein diacetate hydrolysis (microbial activity potential)
  - β-glucosidase (releases glucose from cellulose)
  - Arylsulfatase (sulfur cycle and mineralization)
  - Phosphatase (phosphorus mineralization)
  - Leucine aminopeptidase (protein degradation)
  - Chitinase (chitin degradation)
  - Lipase (lipid degradation)
- Procedure: prepare soil slurry by mixing 1.5 g soil with 20 mL deionized water; incubate with substrates in 96-well microplates (30 µL slurry + 170 µL substrate solution) and monitor fluorescence every 30 minutes over 4 hours at 28°C.
- Replicates and controls: three methodological replicates per sample, plus quenched standards; fluorescence checked against controls to correct for non-enzymatic changes.
- Detection: fluorescence measured with a Cytation 5 reader at substrate-specific excitation/emission wavelengths (4-MUB and 7-AMC fluorophores).
- Output units: nmol product min⁻¹ g⁻¹ dry soil; results inform comparative analyses of enzyme potential across management and site conditions.

## Data structure

- File format: flatbed CSV
- Dataset size: 450 data rows and 12 columns
- Columns and descriptions:
  - id: unique identifier for cross-referencing
  - management_intensity: qualitative description of land-use management
  - latitude: GPS latitude
  - longitude: GPS longitude
  - ace: acetate esterase (nmol min⁻¹ g⁻¹ dry soil)
  - fda: fluorescein diacetate hydrolysis (nmol min⁻¹ g⁻¹ dry soil)
  - glu: β-glucosidase (nmol min⁻¹ g⁻¹ dry soil)
  - sul: arylsulfatase (nmol min⁻¹ g⁻¹ dry soil)
  - pho: phosphatase (nmol min⁻¹ g⁻¹ dry soil)
  - leu: leucine aminopeptidase (nmol min⁻¹ g⁻¹ dry soil)
  - chin: chitinase (nmol min⁻¹ g⁻¹ dry soil)
  - lip: lipase (nmol min⁻¹ g⁻¹ dry soil)
- Notes: NA indicates data not recorded for a given entry.

## Associated files

- Analysis outputs: UgrassSoilFunctionalMeasurements.csv
- Data handling and deposition: results compiled from laboratory analyses and exported to CSV for submission to EIDC.

## Context and origin

- Authors and affiliations: Griffiths, R.I.; Puissant, J.; Goodall, T.I. (Centre for Ecology & Hydrology, Bangor and Wallingford)
- Context: Part of the NERC U-GRASS program addressing soil security and ecosystem services, with emphasis on how soil biogeochemical processes and biodiversity underpin multifunctionality under varying management and climate scenarios.