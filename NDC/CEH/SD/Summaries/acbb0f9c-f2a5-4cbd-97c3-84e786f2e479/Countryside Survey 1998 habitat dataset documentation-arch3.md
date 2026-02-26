# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- Provides national estimates of Broad Habitat stock (Habitats 1–17) for 1998, derived using the 2007 ITE Land Classification.
- Outputs include a CSV (CS1998_Broad_Habitat_Stock.csv) with area estimates in 000s ha by Land Class and Broad Habitat, plus a 1 km resolution TIFF (CS1998_stock.tif) raster of mean habitat percentages within each 1 km grid cell.
- Field survey conducted in 1998 (a few sites in 1999); often cited as Countryside Survey 2000.
- Freshwater habitats were modeled using a different statistical approach from terrestrial habitats.

## Data Content and Structure
- CS1998_Broad_Habitat_Stock.csv
  - YEAR: Survey year
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Description
  - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha); may include negative values (treat as 0)
  - LOWER_ESTIMATE: Lower bound of 95% CI (000s ha)
  - UPPER_ESTIMATE: Upper bound of 95% CI (000s ha)
- CS1998_stock.tif
  - 1 km pixel resolution; each pixel holds mean percentage habitat value for a Broad Habitat class within the corresponding Land Class strata
  - Bands map to Broad Habitats (e.g., Band 2 for Coniferous Woodland; other mappings for Broadleaved Mixed and Yew Woodland, etc.)
  - Spatial Reference: British National Grid (OSGB36), Transverse Mercator, extent across Great Britain

## Methods and Interpretation
- Habitat estimates are scaled to 000s ha per Land Class using the ITE Land Classification framework.
- Mean estimates may be negative due to the statistical model; interpret negatives as zero.
- Confidence intervals (Lower/Upper) accompany each mean estimate, reflecting uncertainty.
- Freshwater habitats used a distinct statistical approach from terrestrial habitats.

## Usage for Monitoring Frameworks
- Establishes a 1998 baseline for Broad Habitat stock by Land Class across Great Britain.
- Enables monitoring of changes in habitat extent by Land Class and Broad Habitat over time.
- The raster data (CS1998_stock.tif) supports spatial analyses and visualization at 1 km resolution.
- Useful for comparing with later Countryside Survey results and integrating with the 2007 ITE Land Classification framework.

## Data Quality, Metadata, and Governance
- Documentation notes the need to acknowledge Countryside Survey data (NERC-CEH) and © data rights.
- Metadata gaps can hinder reuse; the dataset includes explicit field definitions and spatial metadata.
- Transparency requires sharing underlying data responsibly and establishing data governance practices.
- Some barriers mentioned for monitoring frameworks: data access delays, siloed data, the burden of publicly sharing datasets, and ensuring metadata quality.

## Access, Reuse, and Restrictions
- Data must be acknowledged when used: Countryside Survey data owned by NERC-CEH; Countryside Survey ©.
- Public sharing of underlying data is encouraged but may pose barriers; ensure compliance with data governance and rights.

## Limitations and Considerations
- Based on 1998 field data; applicability to current conditions requires careful temporal contextualization.
- The 1998 dataset uses the 2007 ITE Land Classification for categorization; crosswalks are required for comparisons with newer classifications.
- Some habitat estimates may be at the edge of model reliability due to negative values or CI width.

## Spatial and Technical Details
- Pixel size: 1 km; grid aligns with Great Britain extent.
- Coordinate system: British National Grid (OSGB36); projection: Transverse Mercator.
- Extent: Great Britain; suitable for national-scale monitoring and regional analyses.

## Publications and References
- Core Countryside Survey outputs and methodologies (UK results 2007; technical reports on statistical methods and land classification).
- Key classifications and guidance documents (ITE Land Classification of Great Britain 2007; Biodiversity Broad Habitat Classification guidance).
- Related field handbooks and methodological papers detailing mapping, sampling, and habitat definitions.

## Practical Guidance for Monitoring Framework Authors
- Use as a baseline for 1998 Broad Habitat stock by Land Class to calibrate longitudinal monitoring.
- Integrate MEAN_ESTIMATE with LOWER/UPPER_ESTIMATE for uncertainty-aware reporting.
- For spatial analyses, utilize CS1998_stock.tif with the corresponding land-class and broad-habitat mappings; ensure alignment with current classifications if making temporal comparisons.
- Address metadata gaps by documenting data provenance, methods, and governance requirements in your monitoring framework.
- Plan data sharing and governance from the outset to minimize barriers to reuse and ensure consistent quality assurance.