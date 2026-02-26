# Data description, Measures of peatland carbon cycling from peat mesocosm incubation experiments.

## Overview
- Two laboratory-based studies on peatland carbon cycling examining interactive effects of abiotic and biotic controls.
- Location: blanket bog peatland at Black Law Wind Farm, Lanarkshire, Scotland.
- Study 1: test interactions of small-scale temperature change, water table level, and plant functional type legacy effects on CO2 and CH4 fluxes; peat and supplementary samples analyzed for biochemical and physical properties.
- Study 2: test interactions of small-scale temperature change and plant functional type legacy effects on peat and litter decomposition; includes CO2 emissions and litter mass loss, with initial biochemical compositions measured.
- Aims align with standardised monitoring data practices: verify, quality-assure, clean, transform data; present outputs in clear formats; store datasets and potentially upload to portals.

## Data scope and Content

### Study 1 (peat CO2 and CH4 fluxes)
- Core material: 108 intact peat cores (PVC, 11 cm diameter, 30 cm depth) collected May 2011 from beneath three plant functional types (PFTs): Calluna vulgaris (shrubs), Eriophorum vaginatum (graminoid), Sphagnum capillifolium (Sphagnum bryophyte).
- Experimental design: fully factorial with three temperatures, three water table levels, three PFTs; replicated four times.
  - Temperatures: 12, 14, 16°C (above mean annual 8°C; range chosen to simulate summer and small-scale climate changes).
  - Water table levels: low (25 cm depth), intermediate (15 cm), high (5 cm) below surface.
  - Total cores per condition: 36 cores per temperature, with 12 per PFT per temperature.
- Incubation: 322 days in controlled rooms; CO2 and CH4 fluxes measured six times (sample days listed include 7, 35, 154, 223, 322 days post-start; data collection points intended to be six).
- Measurements: headspace gas samplings and concentrations for CO2 and CH4; calculations based on changes in concentration, temperature, chamber volume, and area.
- Supplementary data (under each PFT area): 5 cm diameter, 15 cm depth cores used to quantify peat properties:
  - Bulk density, pH, total C, total N, C:N, C stock, N stock.
  - Soil microbial biomarkers: total PLFAs, fungal PLFAs, bacterial PLFAs, ratio F:B, gram-positive and gram-negative PLFAs, and their ratios.
  - PLFA analysis method: Bligh and Dyer extraction with GC; internal standards and a suite of identified fatty acids mapped to microbial groups.
- Biochemical/physical peat properties measured on supplementary samples: total C, total N, C:N, plus microbial community composition (via PLFAs).

### Study 2 (peat and litter decomposition; decomposition rates and respiration)
- Core material: 288 intact peat cores (PVC, 5 cm diameter, 15 cm depth) collected Oct 2012 from Black Law Wind Farm; 96 cores per PFT.
- Plant litter inputs: senesced litter from three PFTs (bryophytes, graminoids, shrubs) plus shed Calluna vulgaris leaves and Eriophorum vaginatum leaves; litter from all three PFTs used to create single-species and mixed litter treatments.
- Experimental design: fully factorial with three temperatures, three PFTs, and eight litter bag treatments; replicated four times per combination.
  - Temperatures: 12, 14, 16°C to simulate small-scale warming.
  - Litter bag treatments: no litter; single-species litter from each PFT; mixture of all three PFTs in equal proportions.
- Incubation: 363 days; maintained field-moisture conditions with deionised water.
- Measurements:
  - Litter decomposition: percent litter mass remaining after 363 days (from initial air-dried mass; corrected to oven-dried mass).
  - CO2 emissions: measured six times (0, 56, 119, 174, 230, 363 days) using an airtight chamber and IRGA; respiration rates derived from CO2 gradients and chamber parameters.
- Initial biochemical composition (peat and litter): measured total C, total N, C:N, and microbial community composition for five peat samples per PFT and four litter samples per PFT and PFT mixture, using the same methods as Study 1.

## Instruments and Methods

- Gas analysis:
  - CO2 and CH4 concentrations measured in headspace with Perkins Elmer AutosystemXL GC (FID and methaniser) for Study 1.
  - CO2 fluxes and CH4 fluxes calculated from changes in concentration, headspace temperature, and chamber geometry.
  - CO2 respiration rates in Study 2 measured with an EGM-4 portable IRGA; enclosure times and calculation based on δCO2/δt.
- Biochemical and physical properties:
  - Carbon and nitrogen contents measured with LECO Truspec CN Analyser (furnace at 950°C).
  - pH measured in a 1:2.5 peat:deionised water slurry with a Hanna 211 pH meter.
  - Dry bulk density measured per standard methods; C and N stocks calculated per area.
- Microbial community analysis (Study 1):
  - Phospholipid fatty acid analysis (PLFA) using Bligh and Dyer extraction; GC quantification with external and internal standards.
  - Identification of PLFAs to microbial groups (bacteria: gram-positive and gram-negative; fungi: saprotrophic and ectomycorrhizal) and calculation of F:B and gram-positive to gram-negative ratios.

## Data Structure and Outputs

- Primary flux data:
  - CO2 and CH4 fluxes from peat mesocosms (Study 1) across multiple time points and conditions (temperatures, water table levels, PFTs).
  - CO2 emissions and litter decomposition rates (Study 2) alongside litter bag treatments and temperatures.
- Supplemental physical and biochemical properties:
  - Peat: bulk density, pH, total C, total N, C:N, C stock, N stock, PLFAs, F:B ratio, and Gram+/Gram− PLFA ratios.
  - Peat and litter initial chemistry: C, N, C:N, and microbial composition.
- Metadata considerations:
  - Detailed sampling dates, core dimensions, PFT classifications, and treatment levels.
  - Instrumentation and analytical methods aligned with established protocols and cited literature.

## Data Quality, Access, and Reuse

- Data described are generated using standardised, reproducible laboratory procedures; multiple replicates per treatment enable robust comparisons.
- QA/QC practices implied by use of certified gas standards, internal standards in PLFA analysis, calibration against multiple references, and adherence to recognized methods.
- Outputs are suitable for integration with broader environmental monitoring datasets (e.g., climate warming scenarios, peatland GHG inventories) and for cross-study meta-analyses.
- Data storage and sharing practices emphasized in aims, with mention of storing and uploading datasets to appropriate data portals, facilitating broader access and reuse.

## Relevance for Environmental Monitoring Analysts

- Provides longitudinal, controlled-lab-based data on how temperature, water table, and plant functional type legacy influence GHG fluxes and decomposition in peatlands.
- Contains rich ancillary data (peat and litter chemistry, microbial community structure) enabling mechanistic interpretation and data fusion with landscape-scale monitoring.
- Demonstrates standardised experimental designs, rigorous measurement protocols, and comprehensive metadata suitable for policy evaluation and monitoring of environmental health over time.