# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Data product from Countryside Survey 1990 providing national estimates of Broad Habitat stock (Habitats 1–17) for 1990.
- Estimates derived using the 2007 ITE Land Classification; totals reported in 000s hectares per Land Class and Broad Habitat, with lower and upper 95% confidence intervals.
- Note: Freshwater habitats analysed with a different model; no Montane (BH15) class in 1990.

## Data products and content
- cs1990_stock.csv
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha) — may contain negative values (treat as 0)
    - LOWER_ESTIMATE: Lower 95% CI (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI (000s ha)
- cs1990_stock.tif
  - Raster representation with 1 km pixel resolution; each band corresponds to a Broad Habitat class.
  - Based on means from 1 km survey squares within each Land Class strata.
  - Note: No Montane class in 1990; Band 15 corresponds to BH16 and Band 16 to BH17.

## Data model, semantics, and caveats
- Broad Habitat codes map as follows (examples): 
  - BH1 with BH2 mapping depending on land class (e.g., Coniferous Woodland vs. Broadleaved Mixed and Yew Woodland per band definitions).
  - BH16 and BH17 correspond to Inland Rock and Urban in specific bands.
- Units are 000s hectares for the CSV; raster values are percent estimates per 1 km pixel.
- Data limitations to consider:
  - Negative MEAN_ESTIMATE values can occur due to the statistical model; treat as zero.
  - 1990 data reflect the 2007 ITE Land Classification framework, which may require careful crosswalks to other classification schemes.
  - No Montane (BH15) class in 1990; ensures band/class mapping adjustments.
  - 1 km resolution; aggregated totals are subject to sampling design and model assumptions.

## Provenance and references
- Primary source: Countryside Survey 1990 data for Broad Habitat estimates (CS1990_Broad_Habitat_Stock.csv and associated raster).
- Related documentation and methodology references include:
  - Scott et al. 2007; Bunce et al. 2007 (ITE Land Classification references)
  - Bunce et al. 1996, 1981; Jackson 2000 (definitions and interpretation guidance)
  - Countryside Survey main and technical reports (1990 and 2007 outputs)
- Useful links and publications are provided in the dataset metadata for methodological context and reproducibility.

## Access, usage, and licensing
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © (Database Right/Copyright NERC-CEH). All rights reserved.
- All copies of data, publications, reports, or presentations must include the specified acknowledgement.
- Data is intended for reuse within governance and data sharing frameworks that respect the provenance and licensing.

## Data governance and stewardship considerations
- Metadata completeness: ensure fields for YEAR, LAND_CLASS, BH codes/names, units, and CI ranges are clearly documented; include method notes about the 1990+2007 ITE classification linkage.
- Provenance tracking: maintain explicit record that 1990 estimates are derived using the 2007 ITE Land Classification and note the absence of BH15 in 1990.
- Interoperability: provide crosswalks between BH codes and land classes to support integration with other datasets; document band-to-habitat mappings for the raster product.
- Quality Assurance: implement checks for negative MEAN_ESTIMATE values (automatically reset to zero) and verify consistency between CSV totals and raster band distributions where applicable.
- Access and reuse: preserve licensing terms and ensure all downstream users apply the same acknowledgement language.
- Update/versioning: track versions if reprocessing or reclassifying datasets; record any methodological changes (e.g., updates to Land Classification mappings).

## Practical notes for data users
- Use the CSV for numerical analyses and aggregations; use the TIFF raster for spatially explicit analyses at 1 km resolution.
- When aggregating across Land Classes or Broad Habitats, apply the 95% CI where uncertainty estimates are required.
- Align spatial references to OSGB36 / British National Grid when integrating with other GB-wide geospatial layers.