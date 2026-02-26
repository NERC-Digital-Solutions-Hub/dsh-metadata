# Countryside Survey:
Measuring Habitat Change over 30 years 1978 Data Rescue - Final Report (CEH Project no.: NEC03689)

## Overview
- Purpose: Rescue, digitise, and validate the 1978 Countryside Survey land-cover maps to enable GIS-based analysis of Broad Habitats and their change over time.
- Benefit: Extends the GB Countryside Survey time series back to 1978, aligning with later surveys (1984, 1990, 1998, 2007) for robust stock and change assessments.
- Scope: Digitisation of 256 1km survey squares from 1978; integration with later survey datasets; data stored in a GIS system at CEH Lancaster.

## Data rescued and scope
- Source data: Primary field records of land-cover and landscape features from the 1978 Countryside Survey, previously at risk of damage or loss.
- Output: Digitised maps linking 1978 field codes to Broad Habitats (BAP classifications) and enabling cross-year comparisons.
- Time series: Adds 1978 data to the existing 1984, 1990, 1998, and 2007 datasets, enabling long-term analyses of habitat stock and change.
- Data products: 
  - Digitised linework and maps stored in a GIS at CEH Lancaster.
  - Scanned field sheets and maps placed in field assessment booklet (FAB) boxes for backup.

## Digitization workflow
- Scanning: Maps scanned to .jpg and .pdf; back-ups created; originals stored securely.
- Digitisation: Maps digitised in summer 2009 by ADAS following the CS1978 data rescue protocol; linework aligned with GIS standards.
- Data integration: 1978 digitised linework reviewed for consistency with later datasets to minimise slivers and misalignment; overall linework deemed highly consistent with subsequent years.

## Data checking and validation
- Ongoing QA: Check for omissions, digitising errors, and inconsistencies by comparing digitised maps to original field maps.
- Cross-year validation: Survey squares for 1978, 1984, 1990, 1998, and 2007 reviewed to identify real changes versus artefacts; visual checks with field data and species data performed.
- Anonymisation: Spatial locations of survey squares are adjusted to prevent identification, while preserving analytical integrity.
- Outcome: 1978 dataset quality and consistency judged to be comparable to other Countryside Survey datasets, enabling reliable future change analyses.

## Broad Habitat allocations
- Translation: Most 1978 codes straightforwardly mapped to BAP Broad Habitats (e.g., Conifer Woodland -> Coniferous Woodland), but some categories were ambiguous and required additional review.
- Resolution: In ambiguous cases, original annotated maps and vegetation plot data were used to confirm allocations; each square visually checked.
- Notable challenges: 
  - Upland codes hardest to delineate due to heterogeneity; may be treated as mosaics in later work.
  - Specific codes (e.g., Calcareous/Acid Grasslands, Inland Rock, Urban associations) required careful cross-checking with vegetation data.
- Additional notes: Some areas could be identified as Priority Habitats (e.g., Coastal Saltmarsh, Blanket Bog, Purple Moor Grass Rush Pasture).

## Land Classification context (ITE and All Squares)
- Original approach (1978): ITE Land Classification using a 15 x 15 km sampling grid across Britain; 6039 squares classified; 256 squares directly surveyed; national estimates derived from mean habitat per square and area of Land Class.
- Evolution of classification:
  - 1984: Reanalysis using a 1978 base with updated methods.
  - 1990: All Squares classification introduced; 509–508 squares surveyed; urban and sea corrections included; national estimates recalibrated.
  - 1998: Land Classification expanded to 40 classes; Scottish reporting separated.
  - 2007: Land Classification expanded to 45 classes; Welsh reporting separated.
- Implication for comparability: National estimates for 1978 were calculated using the 1990 All Squares classification (32 classes); direct comparability to later 45-class results is limited, and some habitats may not map one-to-one across classifications.

## Results: National Estimates of Broad Habitat Stock 1978
- Presentation: Stock estimates for selected Broad Habitats in Great Britain for 1978; caution that values are not directly comparable to 2007 due to sampling and classification differences.
- Key points:
  - 1978 data enable calculation of habitat stock and change when integrated with later years using consistent modelling approaches.
  - The time-series extension to 1978 enhances reliability for detecting long-term trends in Broad Habitats.
  - The 1978 results depend on the 1990 All Squares Land Classification due to sample size and class availability; cross-year reanalysis could alter later year estimates slightly.
- Example results (mean area in thousands of hectares and % GB, highlights):
  - Arable and Horticulture: large share (around 21.9%)
  - Improved Grassland: large share (around 22.3%)
  - Urban: notable share (around 6.2%)
  - Dwarf Shrub Heath, Bog, Acid Grassland, Fen/Marsh/Swamp, etc.: substantial components to be considered in analyses
- Important caveat: Some habitat classes have not direct one-to-one correspondence with later reporting classes; differences explained in the notes and comparisons with earlier publications.

## Comparability with previously published data
- New digitised results differ from earlier publications (Bunce & Heal 1984; Barr et al. 1993) due to classification changes and allocation methods.
- Reasons for differences:
  - Differences in Broad Habitat reporting classes and aggregation.
  - Ambiguities in 1978 polygon allocations corrected using available data.
  - Shift from 1978 ITE Land Classification to the updated All Squares (1990) framework.
- Implication: The new 1978 figures are more aligned with Barr et al. (1993) than with Bunce & Heal (1984); direct cross-year comparisons should consider classification context.

## Notes on Specific Habitats (summary)
- Boundary and Linear Features: 1984-era estimates tend to be lower/higher due to class definitions; differences explained by classification approach.
- Arable and Horticulture; Fen/Marsh/Swamp; Urban; Calcareous Grassland; Acid Grassland; Bog and others show varying degrees of discrepancy across publications due to classification and mapping rules.
- Overall: The rescued dataset provides a more consistent basis for cross-year analyses once classifiers are harmonised.

## Data accessibility and format for GIS work
- Formats: Digitised linework and maps stored in a GIS at CEH Lancaster; scanned originals (.jpg, .pdf) retained for reference.
- Metadata: Includes habitat code lookup and summaries linking 1978 codes to Broad Habitats; appendices provide mapping details and classifications.
- Usage: Enables spatial analyses, overlay with species and soil data, and integration into broader CS time-series studies.

## Appendices and additional resources
- Appendix II: Habitat Code Lookup Table (1978 descriptions and corresponding Broad Habitat Allocations).
- Appendix I & III: Maps showing Broad Habitat stock as percentages by Land Class; Summary of ITE Land Classification evolution.
- References: Documentation of related Countryside Survey work, methodologies, and classifications for context.

## Takeaways for GIS practice
- The 1978 data rescue successfully digitised and validated historical maps, enabling GIS-based time-series analyses of Broad Habitats back to 1978.
- When integrating 1978 with later years, account for changes in Land Classification schemes (ITE 1978 vs All Squares 1990, and later 32 vs 40/45 classes) and potential allocation ambiguities.
- The dataset provides a robust foundation for assessing long-term habitat stock and drivers of ecological variation, with built-in QA processes and anonymised square data to protect location specifics.