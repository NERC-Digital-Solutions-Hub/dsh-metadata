# Soil metals data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey (Great Britain) detailing soil metal concentrations collected in 1998/1999.
- Covers up to 256 1km squares across Great Britain.

## Data content and structure
- Source file: CS1998_SOIL_METALS.csv
- Key points:
  - SQUARE: 1km square sampling site code
  - PLOT: Plot identifier within each 1 km square
  - YEAR: Survey year
  - Cd, CR, CU, NI, PB, ZN: Metal concentrations in ppm (equivalent to mg/kg and µg/g)
  - LC07, LC07_NUM: ITE Land Classification (2007) and numeric code
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: County or Council designation for the square
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Units: metals reported as ppm; interpret as mg/kg or µg/g as appropriate
- Notes: 12 measurements were observed below detection limits (8 Cd, 3 Cr, 1 Ni)

## Laboratory methods and quality control
- Sample preparation: air dried, sieved (<2 mm); sub-sampled for ball milling
- Digestion: aqua regia digestion (3 g soil to 100 ml)
- Analysis: ICP-OES (JY38plus) for most metals; ICP-MS used by EA NLS for samples near detection limits
- Calibration: 12.5% HNO3 solutions matrix-matched with Ca, Mg, Fe, Al
- Batch structure: batches of 20 samples plus 2 QC samples and 2 blanks
- Quality control:
  - Certified Reference Materials and samples from international soil exchange schemes
  - Methods aligned to standard references (e.g., HMSO methods)
  - Internal QC: 2 reference samples, blanks, and a random duplicate per batch
  - Results traceable to CRM 1646 (NBS Estuarine Sediment) and 280 (BCR Lake Sediment)
- Documentation: Methods and QA referenced in accompanying literature and EH/CEH resources

## Usage notes for analysts
- Data can support regional to local assessments of soil metal contamination and correlations with land classification (ITE LC07) and environmental zones.
- The LC07 and EZ_DESC_07 fields enable cross-tabulation with land cover and environmental context.
- Cautions:
  - Detection limits affected interpretation of low concentrations (noted limited detections for some metals)
  - Aqua regia digestion provides total metal concentrations but does not capture all speciation forms
  - Time context: data reflect 1998/1999 conditions; should be considered in trend analyses
- Access and acknowledgment:
  - All use of Countryside Survey data must be acknowledged with the provided statement
  - Acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” along with copyright note
  - References and methodologies are described in the Countryside Survey materials and linked publications

## References and related materials
- Countryside Survey website and project methodologies
- Key publications including MASQ and ITE Land Classification documents
- Countryside Survey: UK Results from 2007 (for context on land classification and broader soil results)

## Acknowledgement and rights
- Acknowledgement and copyright: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”