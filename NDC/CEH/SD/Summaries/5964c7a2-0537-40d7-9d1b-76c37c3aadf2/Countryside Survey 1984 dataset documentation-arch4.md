# Broad Habitat Area Estimates by Land Class for Great Britain 1984

## Overview
- National estimates of Broad Habitat stock (Habitats 1–17) for 1984, derived using the 1998 ITE Land Classification.
- Estimates are provided as total area (000s ha) per Broad Habitat for each Land Class, including lower and upper 95% confidence intervals.
- Two data products are provided: a stock csv with numerical estimates and a 1 km raster with per-band habitat estimates.

## Data files and content
- cs1984_Broad_Habitat_Stock.csv
  - Contains: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE.
- cs1984_stock.tif
  - Raster with 1 km pixels; each band corresponds to a Broad Habitat class, mapping as described (e.g., Broad Habitat 1 and 2 combinations for Woodland types, etc.).

## Data structure details
- Columns in stock file:
  - YEAR: Survey year
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Habitat description
  - LAND_CLASS_AREA: Total area of the relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for the Land Class (000s ha)
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)

## Spatial and technical details
- Spatial resolution: 1 km pixels
- Coordinate system: British National Grid (OSGB1936)
- Extent: Great Britain
- Projection: Transverse Mercator

## Methodology and provenance
- Based on the Countryside Survey 1984 data.
- Broad Habitat stock estimates calculated using the 1998 ITE Land Classification (Bunce et al., 1996; 1998).
- References and related documentation include Scott (2007), Jackson (2000), and various Bunce et al. publications.
- Data and publications are associated with the Countryside Survey project.

## Data quality and uncertainty
- Each estimate includes a 95% confidence interval (LOWER_ESTIMATE and UPPER_ESTIMATE) around the MEAN_ESTIMATE.
- Raster bands provide mean habitat percentages per 1 km pixel within Land Class strata, derived from sampling.

## Access, licensing, and attribution
- All Countryside Survey data must be acknowledged.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © NERC-CEH; all rights reserved.
- Primary access points: Countryside Survey website and publications; CEH data and metadata; Environmental Information Data Centre (EIDC).
- Numerous publications and links provided for methodological context and data usage.

## Relevance for Data Leaders
- Demonstrates a consolidated, standardized data product derived from a national survey, supporting data strategy through:
  - System-wide view of habitat data across Land Classes.
  - Clear metadata and documentation enabling discoverability and reuse.
  - Explicit uncertainty quantification (confidence intervals) to inform decision-making.
  - Alignment to a common classification (ITE Land Classification) to facilitate cross-organizational data sharing and integration.

## Governance and coordination considerations
- The dataset exemplifies standardized data production and licensing, aiding coordination across organizations by providing a traceable data lineage, formal attribution, and accessible methodological references.
- Highlights importance of harmonized classifications, metadata richness, and licensing clarity to reduce data fragmentation and barriers to access.