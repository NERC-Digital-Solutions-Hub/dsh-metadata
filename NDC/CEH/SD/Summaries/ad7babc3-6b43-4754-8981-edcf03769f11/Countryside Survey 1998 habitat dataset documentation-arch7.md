# Broad Habitat Area Estimates by Land Class for Great Britain 1998

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 1998, calculated using the 2007 ITE Land Classification.
- Estimates provided as total area (in thousands of hectares) per Broad Habitat per Land Class, including lower and upper 95% confidence intervals.
- Freshwater habitats were analysed with a different statistical model than other habitats.
- Field survey conducted in 1998 (with a few sites in 1999); commonly referred to as Countryside Survey 2000.

## Data products
- CS1998_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE
  - MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as 0.
- CS1998_stock.tif
  - A 1 km resolution raster with 1 band per grid cell per Broad Habitat class; each band provides the mean percentage of habitat value for that square.
  - Each band corresponds to a Broad Habitat class (band-to-habitat mapping provided in the dataset’s documentation).

## Spatial and technical details
- Spatial reference: British National Grid (OSGB36), projection: Transverse Mercator.
- Pixel size: 1 km (1000 m); Extent: Great Britain.
- Data formats: CSV (national estimates) and TIFF raster (1 km, multi-band).

## Data usage notes
- Acknowledgement required on all copies and outputs:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey ©" rights holder; all rights reserved.
- The dataset is part of Countryside Survey 1998 materials; widely referenced as part of Countryside Survey outputs.

## Data sources and references
- Countryside Survey project methodologies and outputs (e.g., Scott 2007 statistical report; Bunce et al. 1996/2007 ITE Land Classification).
- Relevant sources and links associated with Countryside Survey and ITE Land Classification are provided in the documentation.

## GIS workflow considerations
- Combine the CSV stock estimates with the raster bands to create comprehensive habitat maps by Land Class and Broad Habitat.
- Handle negative MEAN_ESTIMATE values by converting to zero before analysis or visualization.
- Ensure all layers use OSGB36 / British National Grid for alignment; convert to other projections only if necessary for downstream workflows.
- Be mindful of the 1 km resolution when integrating with higher-resolution layers; reconciling scale differences may require resampling or aggregation.
- The 1998 survey data provide historical baselines; compare cautiously with later Countryside Survey datasets due to methodological changes over time.