# Soil metals data 1998 [Countryside Survey], Great Britain

- Soil metal concentrations from soil samples in up to 256 1km squares across Great Britain, surveyed in 1998/1999 as part of the Countryside Survey.
- Data are organized by square, plot, and year, with concentrations for cadmium (CD), chromium (CR), copper (CU), nickel (NI), lead (PB), and zinc (ZN), plus land classification and geographic codes.

## Data Content and Structure
- Key fields:
  - SQUARE (1km square site code), PLOT (plot within square), YEAR
  - CD, CR, CU, NI, PB, ZN (ppm; mg/kg; µg/g)
  - LC07, LC07_NUM (ITE Land Classification 2007)
  - COUNTRY (ENG, SCO, WAL), COUNTY07, EZ_DESC_07 (environmental zone description)
- Included metadata references to Countryside Survey environmental and land-classification frameworks.

## Sampling and Laboratory Methods
- Soil samples: air-dried, sieved (<2 mm), sub-sampled (coning and quartering) for ball milling.
- Digest: aqua regia digestion (3 g soil to 100 ml solution).
- Measurements: metals by ICP-OES; some samples measured by ICP-MS (EA NLS, Llanelli) for low concentrations.
- Analytical batches: typically 20 samples plus 2 QC, 2 blanks; reflux digestion performed in groups of 12.

## Quality Control and Data Integrity
- QC procedures reference: Certified Reference Materials and international soil exchange samples (ISE) for method verification.
- Traceability to Certified Reference Materials: NBS Estuarine Sediment 1646 and BCR Lake Sediment No 280.
- Batch-level QC: 2 internal reference samples, blanks, and a random duplicate per batch.
- Note: A small number of measurements (12 for Cd, 8 for Cr, 1 for Ni) fell below the computed limit of detection.

## Attribution and Usage Rights
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement language: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Data are © NERC - Centre for Ecology & Hydrology; rights reserved; data sharing and publication must maintain this acknowledgement.

## Context and References
- Laboratory and methodological references follow standard Countryside Survey practices (e.g., CS2000 Field Survey Handbook; MASQ module for soils and pollution; ITE land classification papers).
- Key linked sources include Countryside Survey UK results from 2007 and foundational methodological documents (e.g., Bunce et al. on ITE land classification).

## Relevance for Monitoring Frameworks
- Provides a robust, longitudinal baseline of soil metal concentrations across GB at a landscape scale (1 km grid) suitable for policy evaluation and trend analysis.
- Metadata and QA details support data governance, reproducibility, and transparent data sharing.
- Geographic and land-class context enables integration with policy-relevant indicators (soil quality, pollution, land use).

## Practical Considerations for Policymakers
- Data gaps and standardization: older dataset with specific lab methods; some measurements below detection require careful treatment or imputation for trend analyses.
- Data provenance and transparency: strong QA framework and traceability facilitate confidence in assessments informing environmental health decisions.
- Data sharing: explicit requirement for acknowledgement; openness considerations addressed through metadata provenance.