# Riparian woodland coverage in Great Britain (1km raster)

## Overview
- Provides a 1km resolution raster (geotiff) showing the proportion of wooded riparian areas across Great Britain.
- Outputs a grid where each 1km cell contains the percentage of riparian woodland within that square kilometre.

## Data Scope and Definition
- Riparian areas are defined by applying a 50-metre buffer to the CEH 1:50,000 watercourse network.
- Wooded areas within this buffer are identified as coniferous or deciduous woodland according to Land Cover Map 2007 (LCM2007).
- The final dataset expresses the proportion of wooded riparian area per 1km cell as a percentage.

## Data Processing Workflow
1. Buffer the CEH 1:50,000 watercourse network by 50 metres.
2. Dissolve buffered features into a single polygon.
3. Clip corresponding areas from the LCM2007 25m raster dataset using the dissolved polygon.
4. Extract woodland classifications (LCM07 classes 1 and 2) from the clipped raster.
5. Calculate total woodland area and express the proportion of riparian woodland per 1km cell as a percentage.

## Data Inputs and Provenance
- CEH 1:50,000 watercourse network (derived from UK digital river centerline dataset; linked to Moore, Morris & Flavin, 1994; OS maps).
- Land Cover Map 2007 (LCM2007; 25m raster; Morton et al., 2014; data centre DOI provided).
- References for data sources:
  - ESRI ArcGIS Desktop 10.3
  - Moore, V. R., Morris, D. G., & Flavin, R. W. (1994)
  - Morton, R. D. et al. (2014)

## Data Structure and Format
- Output format: 1km resolution GeoTIFF (.tif).
- Spatial Reference System: OSGB 1936 / British National Grid.
- Each cell value: percentage of the cell’s area that is wooded riparian woodland.

## Implications for Monitoring Frameworks
- Provides a standardized, policy-relevant metric of riparian woodland coverage across GB to monitor changes over time.
- Uses well-established, authoritative input datasets; supports transparency and repeatability in monitoring.
- Facilitates integration into dashboards or reports for environmental health assessments and policy evaluation.

## Considerations and Limitations
- Based on LCM2007 data (dated 2011 release), which may affect timeliness of woodland classifications.
- Requires careful metadata management and provenance tracking to ensure reproducibility and data governance.
- Spatial resolution (1km) aggregates finer-scale variability, which may influence sensitivity for localized policy decisions.
- Data quality depends on the upstream accuracy of the watercourse network and land cover classifications.

## References
- ESRI (2016) ArcGIS Desktop: Release 10.3.
- Moore, R.V., Morris, D.G., and Flavin, R.W. (1994). Sub-set of UK digital 1:50,000 scale river centreline network. NERC, Institute of Hydrology, Wallingford.
- Morton, R.D.; Rowland, C.S.; Wood, C.M.; Meek, L.; Marston, C.G.; Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC Environmental Information Data Centre.