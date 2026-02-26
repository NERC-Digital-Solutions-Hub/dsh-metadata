# Broad Habitat Area Estimates by Land Class for Great Britain 1984

- National estimates of Broad Habitat stock (Habitats 1-17) for 1984 calculated using the 1998 ITE Land Classification. Estimates are provided as total area (in thousands of hectares) per Land Class, with lower and upper 95% confidence limits.
- Spatially explicit raster data accompany the stock estimates.

## Data products

- cs1984_Broad_Habitat_Stock.csv
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the relevant Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% CI of the Broad Habitat area (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI of the Broad Habitat area (000s ha)

- cs1984_stock.tif
  - A 1 km resolution raster with 17 bands.
  - Each band represents a Broad Habitat class; mean percentage value of habitat within each 1 km pixel, derived from 1 km survey squares sampled within each Land Class strata.
  - Band-to-habitat mapping varies by Land Class (detailed in the document’s mapping section).

## Spatial reference and extent

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB1936), Transverse Mercator
- Extent: Great Britain

## Band mapping and interpretation

- The raster comprises 17 bands, each corresponding to a Broad Habitat class. The exact band-to-habitat mappings depend on the Land Class, with the document detailing the associations (e.g., how Broad Habitat 1–17 map to specific bands under different Land Class groupings). Pixel values represent the mean percentage of habitat in each 1 km pixel.

## Data provenance and references

- Data source: Countryside Survey 1984
- Classification basis: 1998 ITE Land Classification (Bunce et al., 1996; 1981; 1998)
- References and publications are provided for methodology, statistical treatment, and classification schemes (e.g., Scott 2007; Jackson 2000; Bunce et al. 1998; Carey et al. 2008).

## Usage in GIS

- Suitable for map-based data products and explorations of historical habitat stocks in Great Britain.
- Can be integrated with other GIS layers (e.g., current land cover, administrative boundaries) to support policy, planning, or public-facing visualization.
- Important considerations:
  - Align raster with other layers that may be at different resolutions; consider resampling or aggregation as appropriate.
  - Use the stock CSV for exact area estimates and confidence intervals by Land Class and Broad Habitat; use the raster for spatially explicit visualization of habitat percentages.
  - Acknowledge Countryside Survey data ownership and rights in all outputs.

## Data rights and attribution

- Data owned by NERC - Centre for Ecology & Hydrology
- All use requires acknowledgment: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
- Countryside Survey ©; All rights reserved

## Considerations for GIS work and quality

- Data are historical (1984) and use the 1998 ITE Land Classification; not current baseline
- Data are distributed across two formats (tabular estimates and a 1 km raster) to support both summary statistics and spatial visualization
- Data may require cleaning and transformation to align with local workflows and standards
- Data are held in multiple places and involve complex mapping between land classes and habitat bands; validate band mappings against documentation when performing analyses

## Acknowledgements and references

- Includes extensive bibliographic references to methodologies, classification schemes, and prior Countryside Survey outputs (e.g., Scott 2007; Carey et al. 2008; Bunce et al. 1998; Jackson 2000) to support interpretation and reproduction of results