# Community antimicrobial resistance genes and concentrations of polycyclic aromatic hydrocarbons and metals in NE England soils

## Overview
- A dataset describing the relative abundance of antimicrobial resistance genes in DNA from soils around Newcastle upon Tyne, alongside metal concentration data.
- Fieldwork conducted in June 2016, with soil samples collected from the upper horizon (<15 cm) and refrigerated until processing.
- Sampling design based on preselected locations using metal concentrations and land-use, covering four treatments: low-metal/rural, low-metal/urban, high-metal/rural, high-metal/urban.

## Sampling design and fieldwork
- Locations chosen to reflect prior metal concentration profiles and land-use contexts.
- Four treatment categories representing combinations of metal exposure and urban/rural settings.
- Soils collected from the upper horizon and stored refrigerated prior to analysis.

## Analytical methods
- Soil pH measured according to ISO 10390:2005 on a soil-water slurry (1:5 v/v), measured with a pH meter.
- Total metal concentrations determined by ICP-MS after aqua regia digestion.
- Bioavailable metal fractions extracted using the modified BCR procedure:
  - Step 1: acetic acid extraction (0.11 M) with 16-hour contact; liquid extracts analyzed by ICP-MS.
  - Step 2: residual solids treated with 0.5 M hydroxylammonium chloride at pH 1.5 for 16 hours; liquid extracts analyzed by ICP-MS.
- Units:
  - Total metals: mg/kg
  - Bioavailable metals: ppm (mg/kg equivalent)

## Data structure and variables
- Core fields:
  - Rural/Urban (land-use category)
  - Location (common name)
  - Latitude (deg)
  - Longitude (deg)
  - pH (value)
  - Metals: Al, As, Be, Cd, Cr, Cu, Fe, Pb, Hg, Ni, P, Zn
- Measurement sets:
  - Total metals (aqua regia extractions) — columns F–Q
  - Bioavailable metals (Step 1 BCR extractions) — columns R–AD
  - Bioavailable metals (Step 2 BCR extractions) — columns AE–AQ
- Nature of data includes both concentration values and their assignment to specific extraction methods and data columns.

## Documentation, provenance, and governance
- Methods and references documented to support reproducibility:
  - ISO 10390:2005 for pH
  - Mossop & Davidson (2003) for modified BCR extraction
  - Quevauviller et al. (1997) for CRM-based validation
  - Rothwell & Cooke (2015) for background concentration context
- Clear linkage of data to standardized procedures enhances discoverability and interoperability.
- The record provides explicit data structure and measurement protocols, supporting data quality assurance and potential reuse.

## Data stewardship considerations
- Clear data standards: standardized units, defined extraction methods, and explicit column mappings facilitate reuse and integration with other datasets.
- Metadata sufficiency: location, land-use, sampling depth, methods, and unit definitions enable reproducibility and provenance tracing.
- Governance gaps to address for ongoing stewardship:
  - Clarify data access, licensing, and any embargo or update policies.
  - Maintain a data dictionary and lineage documentation to support long-term sustainability.
  - Ensure interoperability across systems, given multiple extraction methods and multi-column data organization.
- Potential use cases: environmental risk assessment, correlation analyses between resistance gene abundance and metal concentrations, land-use impact studies, and meta-analyses requiring standardized metal data.

## References
- ISO (2005) ISO 10390:2005(E) Soil Quality - Determination of pH
- Mossop KF, Davidson CM (2003) Comparison of original and modified BCR sequential extraction procedures for the fractionation of metals in soils and sediments
- Quevauviller P, et al. (1997) Certification trace metal extractable contents in a sediment reference material (CRM 601)
- Rothwell KA, Cooke MP (2015) A comparison of methods used to calculate normal background concentrations of potentially toxic elements for urban soil