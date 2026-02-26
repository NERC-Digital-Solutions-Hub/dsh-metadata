# Soil physico-chemical properties 2007 [Countryside Survey], Great Britain

- The Countryside Survey 2007 provides soil physico-chemical properties measured across Great Britain on up to 591 1-km squares, with data collected from multiple plots within each square.
- Data are intended for national and country-level reporting and for analyses of correlations, trends, and potential predictive relationships in soil properties.

## Data content and columns

- SQUARE: 1 km square sampling site code (text)
- PLOT: Plot identifier within each 1 km square (number)
- YEAR: Year of survey (number)
- PH: Fresh soil pH (in water) (number)
- LOI: Percentage loss on ignition (number)
- C_CONC_LOI: Carbon concentration from LOI (g/kg) using 0.55 × LOI (number)
- C_STOCK_LOI: Carbon stock from LOI (t/ha) using 0.55 × LOI (number)
- BULK_DENSITY: Bulk density (g/cm3) (number)
- MOISTURE: Percentage moisture content (number)
- N_PERCENT: Percentage nitrogen (number)
- N_STOCK: Nitrogen stock (0–15 cm) (t/ha) (number)
- PO4_OLSEN: Olsen phosphorus (mg/kg) (number)
- LC07: ITE Land Class 2007 description (text)
- LC07_NUM: ITE Land Class 2007 numeric code (number)
- COUNTRY: Country location (England ENG, Scotland SCO, Wales WAL) (text)
- COUNTY07: County or council area (text)
- EZ_DESC_07: Countryside Survey Environmental Zone description (text)

- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © CEH. All rights reserved.

## Sampling design and coverage

- Sampling strategy based on a rigorous statistical design with 591 sample squares across Great Britain (289 England, 107 Wales, 195 Scotland).
- Original CS sampling (1978) used 256 squares; CS2007 extended to 591 squares with soils collected from the western corner of Main Plots.
- Topsoil samples (0–15 cm) were collected, with 15 cm southward offset in 1978 and then from various corners in later surveys; power analyses ensured sufficient samples for major habitats and country reporting.
- Field protocols and processing guidelines provided to ensure consistency across sites and years.
- Data are intended to support national statistics and comparisons across GB countries and land classes.

## Laboratory methods and analytes

- pH in fresh soil (water) and in 0.01 M CaCl2 measured on subsamples from each core (up to 3145 samples).
  - Method: 10 g soil with 25 ml deionised water, 1:2.5 soil-to-water ratio, mix, let stand 30 minutes, measure pH after 30 seconds.
  - QC: Batch calibrations with pH 4 and pH 7 buffers; re-calibration if deviation >0.02 pH units; standard soil and duplicate analyses per batch.
- LOI (loss on ignition)
  - Up to 3145 black cores analysed; 10 g air-dried sub-sample; dried at 105°C for 16 h; combusted at 375°C for 16 h; LOI calculated from weight loss.
  - Method: CEH Lancaster UKAS-accredited SOP3102; QA includes standard material and duplicate samples per batch.
  - Data reconciled to ensure comparability with CS2000 and 1978 methods (CS2007 used the 1978 LOI method for consistency with earlier surveys).
- Bulk Density (BD)
  - Measured on the same material as LOI; requires precise core dimensions and weights; BD calculated considering stones’ volume and density.
  - ISO 11272:1998 not adopted; CS-specific approach developed; QC via comparisons to expected values and cross-survey consistency checks.
- Olsen-P (phosphorus)
  - Up to 1280 samples; extraction with 0.5 M NaHCO3 (pH 8.5) on 5 g air-dried soil; colorimetric determination (molybdenum blue) with a skalar continuous-flow analyser.
  - QC: replicate analysis plus one standard soil and one certified reference soil per batch (25 samples per batch); controlled drying effects and temperature to minimize error.
  - Notes: Drying can affect extractable P; method is temperature- and soil-type sensitive; organic matter may co-extract.
- Total Nitrogen (N)
  - Up to 1280 samples analysed by CEH Lancaster using Vario-EL elemental analyser (CEH SOP3102); oxidative combustion with N2 detection after calibration with acetanilide standards.
  - Sample weights typically 15 mg for peat; 15–60 mg for mineral soils; QA with in-house reference materials.

## Quality assurance and data integrity

- QA/QAQC framework aligned with Defra/NERC/BBSRC Joint Codes of Practice.
- All analytical runs include standard materials, replicates, and cross-checks; re-analyses conducted if problems are detected.
- Labs chosen for analyte-specific accreditation; detailed accreditation status is documented.
- Documentation and cross-comparison testing were conducted (e.g., comparison with CS2000 methods for LOI; comparability checks for pH methods).

## Data processing, transformations, and documentation

- C_CONC_LOI and C_STOCK_LOI derived from LOI using CS conversion, enabling comparability across carbon metrics.
- Data processing and archiving followed standard CS procedures; metadata and data manipulation protocols documented in CS Soils Manual (Emmett et al. 2008).
- Statistical analysis conducted by Chartered Statisticians per CS Project Board protocols.

## References and related publications

- Emmett et al. 2008 Countryside Survey: Soils Manual; Countryside Survey Technical Report No. 3/07.
- Emmett et al. 2010 Countryside Survey: Soils Report from 2007 (CS Technical Report No. 9/07).
- Additional foundational references for soil methods and land classification (Avery & Bascombe; Bunce et al.; Allen; Jackson) are cited for methodological context.
- CS2007 UK results report (Carey et al. 2008) and related CS 2007 soil publications are available in the CS repository.

## Usage notes and acknowledgements

- Data must be acknowledged as Countryside Survey data owned by NERC – CEH.
- Documentation and protocols are available in the Countryside Survey Soils Manual and associated Technical Reports.
- The dataset supports national and country-level soil-health analyses, cross-site comparisons, and trend detection for management and research decision-making.