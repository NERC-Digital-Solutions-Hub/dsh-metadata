# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- National estimates of Broad Habitat stock (Habitats 1-17) for 1998, derived using the 2007 ITE Land Classification.
- Provides area estimates in thousands of hectares per Broad Habitat and Land Class, including 95% confidence intervals (lower and upper).
- Freshwater habitats were analyzed with a different statistical model.
- Field survey conducted in 1998 (with a few sites in 1999); often referred to as Countryside Survey 2000.

## Data Files Included
- CS1998_Broad_Habitat_Stock.csv: contains tabular estimates by Year, Land Class, and Broad Habitat (with area and confidence intervals).
- CS1998_stock.tif: raster data with 1 km pixel resolution; each band corresponds to a Broad Habitat class and provides mean percentage habitat cover within each 1 km square.

## Data Structure and Columns (CSV)
- YEAR: Year of survey.
- LAND_CLASS: ITE Land Class descriptor.
- BROAD_HABITAT: Broad Habitat code.
- BROAD_HABITAT_NAME: Broad Habitat description.
- LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha).
- MEAN_ESTIMATE: Mean area estimate of the Broad Habitat for the Land Class (000s ha). Note: may be negative due to the statistical model; treat as 0.
- LOWER_ESTIMATE: Lower 95% confidence limit (000s ha).
- UPPER_ESTIMATE: Upper 95% confidence limit (000s ha).

## Raster Data Details (TIFF)
- CS1998_stock.tif contains 17 bands.
- Each band corresponds to a Broad Habitat class as defined in the associated mapping (e.g., Band 2 relates to Broad Habitat 1/2 depending on the pairing; the documentation lists the band-to-habitat mappings).
- Pixel size: 1 km (1000 m); extent covers Great Britain.
- Spatial reference: British National Grid (OSGB36), Transverse Mercator projection.

## Spatial Reference and Coverage
- Extent: Great Britain.
- Projection/Coordinate System: British National Grid OSGB1936.
- Pixel size: 1 km for raster data; CSV provides national totals by Land Class and Broad Habitat.

## Data Use, Attribution, and Licensing
- All CS data must be acknowledged.
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey © NERC-CEH; all rights reserved.
- Publications and references supplied for methodological context and data provenance (see references section).

## Technical Notes and Caveats
- Some MEAN_ESTIMATE values may be negative due to the statistical model; these should be treated as 0 in analyses.
- The survey year is 1998 (with a few sites in 1999); datasets reflect that period and the 2007 Land Classification framework.
- Freshwater habitats were modeled separately from other habitats.
- The Countryside Survey outputs are linked to methodological reports and classifications (ITE Land Classification, 2007; related technical reports).

## Potential Uses for Data Support
- Facilitating data exploration and self-serve analysis of Broad Habitat distribution by Land Class at national scale.
- Enabling cross-walks between 1998 data and later classifications (e.g., 2007 ITE Land Classification) for change assessment.
- Supporting policy, planning, biodiversity assessments, and environmental reporting at regional/national levels.
- Creating derived products (e.g., area by habitat, habitat by land class, or maps at 1 km resolution) and accompanying uncertainty estimates.

## Helpful References and Resources
- Countryside Survey project background and methodologies.
- Carey et al. (2008) Countryside Survey: UK Results from 2007.
- Scott (2007) CS Technical Report No. 4/07: Statistical methods for national estimates.
- Bunce et al. (1996, 1981) ITE Merlewood Land Classification references.
- Jackson (2000) Guidance on the interpretation of the Biodiversity Broad Habitat Classification.