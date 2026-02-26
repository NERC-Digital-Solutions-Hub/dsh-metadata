# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 1998, calculated using the 2007 ITE Land Classification.
- Based on field survey conducted in 1998 (with a few sites in 1999); often referred to as the Countryside Survey 2000.
- Freshwater habitats analysed with a different statistical model from other habitats.
- Data are used to inform Countryside Survey outputs and related research.

## Data Files and Structure
- CS1998_Broad_Habitat_Stock.csv
  - YEAR: Survey year.
  - LAND_CLASS: ITE Land Class code.
  - BROAD_HABITAT: Broad Habitat code.
  - BROAD_HABITAT_NAME: Description of Broad Habitat.
  - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha).
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the land class (000s ha). Negative values may occur due to the statistical model; treat as 0.
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha).
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha).

- CS1998_stock.tif
  - Raster with 1 km pixels; each band corresponds to a Broad Habitat class.
  - Band-to-habitat mappings provided (e.g., Band 2 = Broad Habitat 2, depending on land class).
  - Pixel size: 1 km (1000 m); Coordinate system: British National Grid (OSGB36); Projection: Transverse Mercator; Extent: Great Britain.

## Spatial and Temporal Coverage
- Geography: Great Britain.
- Time: 1998 field survey (some sites in 1999); dataset often cited as Countryside Survey 2000.

## Land Classification and Habitat Codes
- Uses ITE Merlewood Land Classification (Bunce et al. series) as the basis for Land Class (LAND_CLASS) coding.
- Broad Habitats coded 1–17 with corresponding descriptions; raster bands align with these Broad Habitat classifications.

## Data Quality, Limitations, and Notes
- MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as 0.
- Freshwater habitats were analyzed with a different model than terrestrial habitats.
- Includes 95% confidence intervals (LOWER_ESTIMATE and UPPER_ESTIMATE) for uncertainty.
- Acknowledgement required for all use of Countryside Survey data.

## Provenance, Access, and Acknowledgement
- Data ownership: Countryside Survey, NERC - Centre for Ecology & Hydrology (CEH).
- All uses must acknowledge Countryside Survey data ownership and copyright.
- Key references and publications provided to support methodology and interpretation.

## Usage, Citations, and References
- References include:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007 (background and outputs).
  - Scott (2007) CS Technical Report No. 4/07 (statistical methodology for national estimates).
  - Haines-Young et al. (2000, 2000) guidance on habitat classification and accounting for nature.
  - Bunce et al. (1996, 2007) ITE Land Classification and related descriptions.
  - Jackson (2000) guidance on interpretation of Biodiversity Broad Habitat Classification.
- Publications and the Countryside Survey website provide broader context and methodologies. Links and DOIs are provided in the references section.