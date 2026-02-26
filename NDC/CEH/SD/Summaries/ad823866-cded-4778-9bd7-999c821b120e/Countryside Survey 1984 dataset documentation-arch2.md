# Broad Habitat Area Estimates by Land Class for Great Britain 1984

## Purpose and Scope
- Provides national estimates of Broad Habitat stock (Habitats 1–17) for Great Britain in 1984.
- Estimates are calculated using the 1998 ITE Land Classification and presented as total areas in thousands of hectares per Land Class, including lower and upper 95% confidence limits.
- Two data products accompany the dataset: a CSV stock file and a 1 km pixel raster (TIFF) with mean habitat percentages.

## Datasets and File Details
- CS1984_Broad_Habitat_Stock.csv
  - Columns include: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA (000s ha), MEAN_ESTIMATE (000s ha), LOWER_ESTIMATE (000s ha), UPPER_ESTIMATE (000s ha).
  - National estimates are provided per Land Class and Broad Habitat combination.
- cs1984_stock.tif
  - A 1 km resolution raster where each band represents a Broad Habitat class within the Land Class strata.
  - Bands map Broad Habitat 2 with Broad Habitat 1 as Band 2, Broad Habitat 2 with Broadleaved Mixed and Yew Woodland as Band 2, etc., effectively producing per-pixel mean percentages of habitat presence.
  - Spatial reference: British National Grid (OSGB36), Transverse Mercator; extent covers Great Britain.

## Land Classification and Habitat Coding
- Broad Habitats are defined using the ITE Land Classification (Merlewood system) cross-walked to the Broad Habitat Classification (Jackson, 2000).
- The mapping supports interpretation of habitat extent across land classes and over time for monitoring and policy evaluation.

## Methods and Quality Context
- National estimates are derived from Countryside Survey methodology with 1 km survey squares sampled within Land Class strata.
- Related references include:
  - Scott (2007) and Bunce et al. (1998) for the ITE Land Classification baseline.
  - Carey et al. (2008) Countryside Survey UK Results (2007) and associated technical reports.
- Pixel and area estimates are provided with standard confidence intervals to convey uncertainty.

## Data Usage, Outputs, and Accessibility
- Outputs are designed for standardised monitoring of environmental health and policy performance over time.
- Data are intended to be stored and uploaded to appropriate portals, supporting broad accessibility for stakeholders.
- Suitable for reporting, mapping, and trend analysis at national and land-class levels.

## Acknowledgement and Licensing
- Countryside Survey data are owned by NERC – Centre for Ecology & Hydrology.
- All CS data usage requires explicit acknowledgement.
- Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright statements apply.

## References and Further Reading
- Includes links and citations to Countryside Survey project documentation, technical reports, and Land Classification sources (ITE 1996–1998, Jackson 2000, Bunce et al., Scott 2007, Carey et al., etc.) for methodology, classifications, and data provenance.

## Challenges and Opportunities for Analysts
- Increasing the value of these 1984 datasets by integrating with other relevant environmental data to avoid single-use outputs.
- Enhancing access to underlying data used to create final outputs to support transparency, reproducibility, and broader analytical use.