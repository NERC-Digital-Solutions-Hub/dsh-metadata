# Broad Habitat Area Estimates by Land Class for Great Britain 1984

## Overview
- Countryside Survey 1984 provides national estimates of Broad Habitat stock (Habitats 1–17) for Great Britain, derived from the 1998 ITE Land Classification.
- Estimates are given as total area (in 000s hectares) per Land Class, with lower and upper 95% confidence intervals.
- Includes both tabular stock data and raster area estimates, reflecting habitat distribution across land classes and bands.

## Data assets and contents

- cs1984_Broad_Habitat_Stock.csv
  - Summary: National estimates of Broad Habitat area by Land Class for 1984.
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: Total Area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area estimate of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% CI for Broad Habitat area (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI for Broad Habitat area (000s ha)

- cs1984_stock.tif
  - Summary: Raster representation of Broad Habitat areas at 1 km resolution.
  - Structure: Each band corresponds to a Broad Habitat class; within each 1 km pixel, the band contains the mean percentage estimate of that habitat’s presence in that square.
  - Band mapping: Band associations follow the Broad Habitat vs. Land Class mapping (e.g., Broad Habitat 1 and 2 combinations correspond to specific bands as described in the dataset notes).

## Spatial information

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain

## Data rights, acknowledgement, and publication requirements

- Data ownership: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Rights: Countryside Survey ©; All rights reserved.
- Acknowledgement: Required in all copies, publications, reports, and presentations: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”

## Methods, references, and background

- Source methodology and classification
  - Based on Countryside Survey 1984 methodology and the ITE Land Classification (Bunce et al., 1996; 1998) and related guidance (Jackson, 2000).
  - National estimates are generated from 1 km survey squares and mapped to Broad Habitat categories.
- Key references and resources
  - Scott, 2007; Bunce et al., 1998; Bunce et al., 1981; Bunce et al., 1996
  - Jackson, D.L. 2000 (guidance on Broad Habitat interpretation)
  - Carey et al., 2008 (Countryside Survey UK results from 2007) and associated technical reports
  - Countryside Survey Technical Report No. 4/07 (Statistical methods)
- Related data products and access notes
  - Links and descriptions to CS methodology, data products, and related datasets are provided within the dataset documentation and references.

## Practical considerations for Data Leaders

- Data scope and currency
  - Historical dataset (1984) providing baseline habitat extents; not a current-year estimate.
  - Useful for trend analyses when combined with later Countryside Survey years.
- Data quality and metadata
  - Includes explicit confidence intervals (lower/upper estimates) for tabular data.
  - Raster data provides per-pixel mean percentage estimates by Broad Habitat band, requiring careful interpretation when aggregating by Land Class or region.
  - Spatial resolution (1 km) may limit detection of fine-scale habitat patterns.
- Data discoverability and governance
  - Formats: CSV (tabular) and TIFF (raster); clear field definitions and spatial metadata included.
  - Requires proper attribution in all uses; ensure metadata and provenance are preserved for discoverability.
  - Consider linking to broader Countryside Survey ecosystem datasets and standardizing on the ITE Land Classification framework for interoperability.
- Accessibility and barriers
  - Access constrained by licensing and rights; ensure compliance with acknowledgment requirements.
  - Potential data gaps or limitations tied to 1984 methodology and partial reproducibility of some band mappings; verify against cited references when re-using.
- Implications for data strategy
  - Establish a lineage and metadata strategy to capture survey year, classification scheme, and spatial transformations.
  - Use as a historical benchmark to inform current data strategies, data quality checks, and cross-organization data sharing across networks.

## How this data supports data strategy objectives

- Provides a well-documented historical baseline of Broad Habitat extents across Great Britain, enabling trend analyses and assessments of long-term habitat change.
- Demonstrates integration of tabular and raster data products, highlighting the need for coordinated data formats, metadata, and provenance tracking.
- Emphasizes the importance of clear licensing, attribution, and methodological references to ensure responsible data use and reproducibility.