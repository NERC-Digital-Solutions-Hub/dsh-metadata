# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 2007, calculated using the 2007 ITE Land Classification. Based on Countryside Survey data (CS007_Broad_Habitat_Stock.csv) and 1 km resolution habitat maps (CS2007_Stock.tif). Version: 1.0, dated 23-01-2014. Data compiled by C.M. Wood, CEH Lancaster; Countryside Survey data © NERC - Centre for Ecology & Hydrology.
- Estimates expressed as total area (000s ha) per Broad Habitat and Land Class, with lower and upper 95% confidence intervals. Freshwater habitats were modelled using a different statistical approach than other habitats.
- Acknowledgement and copyright requirements apply to all use and publication.

## Data Sets

- CS007_Broad_Habitat_Stock.csv
  - Purpose: National estimates of Broad Habitat stock (Habitats 1–17) for 2007, by Land Class.
  - Key columns:
    - YEAR: Year of survey
    - LAND_CLASS: ITE Land Class (Bunce et al. referenced)
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha); may be negative due to the statistical model (treat negative values as 0)
    - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
    - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)

- CS2007_Stock.tif
  - Purpose: Spatially explicit estimates of Broad Habitat areas across Great Britain at 1 km resolution.
  - Details:
    - Each 1 km pixel contains a mean percentage estimate of the habitat for a Broad Habitat class, derived from means of 1 km survey squares sampled within each Land Class strata.
    - Band/Mapping: Each band corresponds to a Broad Habitat class; e.g.,
      - Broad Habitat 1 and Broad Habitat 2 combinations define Coniferous/Woodland classes; other bands map similarly to Boundary/Linear Features, Arable/Horticulture, Various Grassland types, Wetlands, Rivers/Streams, Montane, Inland Rock, Urban, etc.
    - The document lists the specific band-to-habitat mappings for interpretation.

## Variables, Units, and Modelling Notes

- Units:
  - CSV: AREA in 000s hectares; MEAN_ESTIMATE and confidence bounds in 000s ha.
  - TIFF: Pixel-level mean percentage habitat per 1 km pixel.
- Special considerations:
  - MEAN_ESTIMATE may be negative due to the statistical model; treat as 0.
  - Freshwater Broad Habitats used a distinct statistical approach from other habitats.
  - Data are a 2007 snapshot and may require careful temporal interpretation for change analyses.

## Spatial and Technical Details

- Spatial resolution: 1 km (pixel size 1000 m)
- Coordinate system: British National Grid OSGB36 (Transverse Mercator)
- Extent: Great Britain
- Data source: Countryside Survey (CS) data; 2007 results and associated technical documentation

## Data Usage, Access, and Acknowledgement

- All CS data must be acknowledged:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Copyright: Countryside Survey © NERC-Centre for Ecology & Hydrology
- References for methodology and context include:
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - CS Technical Report No.4/07: Statistical methods for national estimates (Scott, 2007)
  - ITE Merlewood Land Classification (Bunce et al., 1996; 1981)
  - Countryside Survey Field Mapping Handbook (CS Technical Report No.1/07)
  - Guidance on Biodiversity Broad Habitat Classification (Jackson, 2000)

## Potential Analyses and Applications for Data Analysts

- Quantify national Broad Habitat stock by Land Class for 2007 and assess distribution across land-use classes.
- Use CS2007_Stock.tif as a baseline for spatial analyses, change detection, and habitat prioritisation at 1 km resolution.
- Cross-tabulate MEAN_ESTIMATE with LAND_CLASS to identify dominant habitat types within each land class and regions.
- Incorporate confidence intervals (LOWER_ESTIMATE, UPPER_ESTIMATE) to assess uncertainty around area estimates.
- Integrate with other datasets (e.g., administrative boundaries, local authority data) to address scale-access challenges and support local-level planning.
- Validate or calibrate predictive models of habitat change by comparing 2007 baselines with subsequent surveys, while accounting for the different modelling approach used for freshwater habitats.
- Be mindful of data access, provenance, and licensing constraints; ensure proper attribution in all analyses, reports, and publications.