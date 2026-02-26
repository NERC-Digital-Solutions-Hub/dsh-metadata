# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- National estimates of Broad Habitat stock (Habitats 1-17) for 1998, calculated using the 2007 ITE Land Classification.
- Outputs include total area by Broad Habitat per Land Class with mean estimates and 95% confidence intervals (lower and upper bounds).
- Freshwater habitats were analyzed with a different statistical model from terrestrial habitats.
- Survey conducted in 1998 (with a few sites in 1999); commonly referred to as Countryside Survey 2000.

## Data Files and Content
- CS1998_Broad_Habitat_Stock.csv
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: Total Area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
  - LOWER_ESTIMATE: Lower 95% CI (000s ha)
  - UPPER_ESTIMATE: Upper 95% CI (000s ha)
  - Notes: MEAN_ESTIMATE may be negative due to the statistical model; treat as 0.
- CS1998_stock.tif
  - 1km pixel raster; each pixel contains a mean percentage estimate of habitat presence for a Broad Habitat class.
  - Bands by Broad Habitat (e.g., Band 2 = Broad Habitat 2/Coniferous Woodland depending on land class; Band 3 = Broad Habitat 3/Boundary and Linear Features, etc.).
  - Pixel resolution: 1 km; extent: Great Britain; coordinate system: British National Grid (OSGB36), TM projection.

## Methodology and Classifications
- Uses the ITE Land Classification of Great Britain (Bunce et al. 1996; 1981; 2007) to assign Land Classes.
- Broad Habitat mapping and abundance estimates derived from Countryside Survey sampling (1 km square framework) and statistical models linking 1 km samples to national totals.
- Freshwater habitats differ in statistical treatment from terrestrial habitats.
- CS data and national estimates are anchored to published methodological and statistical reports (details in references).

## Spatial and Temporal Details
- Spatial reference: British National Grid (OSGB1936), Transverse Mercator.
- Resolution: 1 km pixels for the raster dataset (CS1998_stock.tif).
- Extent: Great Britain.
- Temporal focus: 1998 survey year (with some sites surveyed in 1999).

## Data Quality, Interpretation, and caveats
- Some MEAN_ESTIMATE values may be negative due to modeling; interpret as zero.
- Includes 95% confidence intervals (Lower and Upper estimates) to convey uncertainty.
- Freshwater habitat estimates use a different statistical model than terrestrial habitats.
- The dataset aligns with Countryside Survey 1998 methodology and classification frameworks.

## Data Availability, Access, and Acknowledgements
- All Countryside Survey data require acknowledgement.
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © CEH; All rights reserved.
- Data should be stored and uploaded to appropriate portals as part of ongoing data management practices.

## References and Related Resources
- Countryside Survey project context and UK results publications (e.g., Carey et al. 2008; Countryside Survey 2007 results).
- Key methodological and classification references:
  - ITE Land Classification of Great Britain (Bunce et al. 1996; 1981; 2007)
  - Countryside Survey technical and statistical reports (e.g., Scott 2007)
  - Jackson (2000) guidance on Broad Habitat interpretation
- External links and resources provided for further methodology and data descriptions.