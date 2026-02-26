# Soil sampling

- Six soil samples per site were collected using a 4 cm width auger to a depth of 10 cm where possible.
- Samples were sieved through a 2 mm aperture to remove stones and roots.
- Collected soils were stored at 5 °C until processing.

## Bulk density

- Bulk density was determined from two cores per site, split into 0-5 cm and 5-10 cm depths.
- Samples were dried at 80 °C for 48 hours after sieving.
- Bulk density calculated as mass per unit volume (mass/volume).

## Volumetric moisture content

- 5 ± 0.001 g of fresh soil per sample was dried at 80 °C for 48 hours.
- Post-drying weight recorded; moisture content calculated as a proportion of the wet weight.

## Water extractable N and C

- 5 g fresh soil mixed with 25 ml Milli-Q water and shaken at 150 rpm for 1 hour.
- Solution filtered through Whatman No. 1 paper.
- Undiluted filtrate analyzed for DIN (NH4, NO3, total N) using a Seal Analytical AA3 autoanalyser with UV digester.
- Undiluted filtrate analyzed for DOC using a Shimadzu TOC analyser.
- Extracts corrected for soil moisture using: DIN/DOC mg/kg = (raw analyser value × (water content of sample (L) + extract volume (L) × dilution factor) × 1000) / dry weight of soil used.

## KCl extractable N and potential mineralisation

- 5 g fresh soil combined with 25 ml of 1 M KCl; shaken at 150 rpm for 1 hour.
- Filtered through Whatman No. 1 paper; filtrate diluted 2:1 and analyzed for DIN (NH4 and NO3) using an autoanalyser.
- Extracts adjusted for soil moisture using: DIN mg/kg = (raw AA value × (water content of sample (L) + extract volume (L) × dilution factor) × 100) / dry weight of soil used.
- A separate 5 g sample was incubated in extraction bottles with Parafilm and kept at 25 °C for 14 days.
- After incubation, samples were extracted and analysed as above.
- Mineralisation calculated as (NO3 + NH4) × bulk density ÷ number of days, expressed as g m⁻² day⁻¹.

## Microbial biomass

- 5 g fresh soil placed in glass beakers and subjected to chloroform fumigation using a desiccator with damp paper towels; vacuum applied until chloroform boiled, maintained for 24 hours.
- A second 5 g soil sample was kept as an unfumigated control.
- Post-fumigation, nutrients were extracted with 25 ml 0.5 M K2SO4, shaken at 150 rpm for 30 minutes.
- Solution filtered through Whatman No. 1 and analysed on the autoanalyser at dilutions of 4:1 for fumigated and 2:1 for unfumigated samples; measured DIN and extractable PO4.
- Dissolved carbon analysed using the TOC-L at the same dilutions as N.
- Values adjusted for water content as per the moisture correction equation above.
- Microbial biomass was quantified using fumigation-extraction with extraction efficiency corrections (KEC = 0.35; KEN = 0.54), applied to the dissolved carbon and nitrogen measurements.

## Data governance considerations for Data Stewards

- Ensure detailed metadata accompanies the dataset, including site ID, sample ID, depth, replicate, collection date, processing date, and processing steps.
- Capture instrument specifics and calibration details (e.g., Seal AA3 autoanalyser, Shimadzu TOC analyser, model numbers, calibration curves).
- Record all volumes, weights, temperatures, times, and dilution factors used in calculations.
- Include QA/QC notes: use of fumigated vs unfumigated comparisons, standards, blanks, and calculation of extraction efficiencies (KE constants).
- Store both raw (unaltered) and processed (moisture-adjusted, per kg, per m²) values, with clear unit definitions (e.g., mg/kg, g m⁻² d⁻¹, mg/L).
- Document data processing formulas and their application context to support reproducibility and data sharing across systems.
- Ensure data are discoverable and interoperable by adopting consistent field names, units, and formats, and provide versioning and lineage information for updates.