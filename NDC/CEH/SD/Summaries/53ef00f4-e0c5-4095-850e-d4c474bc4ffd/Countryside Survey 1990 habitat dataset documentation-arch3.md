# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Baseline estimates of Broad Habitat stock for Great Britain for the year 1990.
- Uses the 2007 ITE Land Classification to derive national totals for Habitats 1–17.
- Provides both total areas (in 000s hectares) with 95% confidence intervals and per-land-class breakdowns.
- Note: freshwater habitats were modeled separately; there was no Montane (BH15) class in 1990.

## What is Included
- CSV dataset: CS1990_Broad_Habitat_Stock.csv
  - National estimates of Broad Habitat stock by Land Class and Broad Habitat code.
  - Fields include YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
  - MEAN_ESTIMATE may contain negative values due to the statistical model (recommended handling: treat as 0).
- Raster dataset: cs1990_stock.tif
  - 1 km pixel resolution; each pixel holds a mean percentage estimate for a Broad Habitat within a Land Class stratum.
  - Bands correspond to Broad Habitat classes; mapping details provided (e.g., Band 2 corresponds to Broad Habitat 2 and 1 in certain cases; Montane BH15 not present in 1990).
  - Note: No Montane class in 1990; Band/ BH mappings adjust accordingly (e.g., Band 15 = BH16, Band 16 = BH17).

## Data Structure and Fields
- CSV columns:
  - YEAR: survey year
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: total area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: mean area of Broad Habitat for the Land Class (000s ha)
  - LOWER_ESTIMATE: lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE: upper 95% confidence limit (000s ha)
- TIFF bands: each band represents a Broad Habitat class as mapped to 1 km grid cells across Great Britain.
- Spatial reference:
  - Pixel size: 1 km
  - Coordinate system: British National Grid (OSGB1936)
  - Projection: Transverse Mercator
  - Extent: Great Britain

## Data Provenance, Methods, and References
- Source: Countryside Survey 1990
- Land Classification: Derived using the 2007 ITE Land Classification (Bunce et al., 1996; Bunce et al., 1981; Bunce et al., 2007)
- Key references:
  - Scott, W.A. (2007) CS Technical Report No.4/07 (Statistical Report) – explains national estimate derivation from 1 km survey squares
  - Bunce et al. (various years) – ITE Land Classification
  - Jackson (2000) – Guidance on interpretation of Biodiversity Broad Habitat Classification
  - Carey et al. (2008) – Countryside Survey UK Results from 2007 (context and background)
- Supporting materials include field handbooks, methodology documents, and related CR/Reports.

## Data Use, Governance, and Access
- Acknowledgement required: Countryside Survey data are owned by NERC - Centre for Ecology & Hydrology.
- Usage constraints and attribution must accompany copies, publications, presentations, and reports that rely on these data.

## Practical Considerations for Monitoring Frameworks
- Baseline utility: Provides a quantitative 1990 reference point for Broad Habitat stock by Land Class, enabling policy scrutiny and trend assessment when combined with later surveys.
- Policy evaluation: Supports assessment of land-use and habitat change under environmental policies, with both national totals and spatially explicit raster data.
- Data quality and governance:
  - Be aware of potential data gaps and the need for robust metadata to verify suitability for specific uses.
  - MEAN_ESTIMATE can be negative; apply a zero-truncation approach for analyses as recommended.
  - Differences in freshwater modeling and the absence of a Montane class in 1990 require careful cross-walks when comparing with other years or classifications.
  - Data sharing and metadata completeness can be barriers; ensure proper data governance and originator contact if reusing raw datasets.

## Limitations and Cautions
- 1990 baseline uses the 2007 ITE Land Classification framework, which may affect comparability with other years unless consistent cross-walking is applied.
- No Montane habitat (BH15) in 1990; related bands adjust accordingly in the raster.
- Some MEAN_ESTIMATE values may be negative due to the statistical model; treat as zero in analyses.
- Freshwater habitats were modeled separately from other habitats, potentially affecting direct comparability.

## References and Further Reading
- Countryside Survey website and technical reports (general background and methodology)
- Scott, W.A. (2007) CS Technical Report No.4/07 – Statistical methods for national estimates
- Bunce et al. (1996, 2007) – ITE Land Classification documentation
- Jackson, D.L. (2000) – Guidance on Biodiversity Broad Habitat Classification interpretation
- Carey et al. (2008) – Countryside Survey: UK Results from 2007
- Field handbooks and related datasets referenced within the dataset documentation