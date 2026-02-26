# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- Version 1, dated 23-1-2014, by C.M. Wood (CEH Lancaster) using Countryside Survey data.
- Purpose: national estimates of Broad Habitat stock (Habitats 1–17) for 2007, calculated with the 2007 ITE Land Classification.
- Outputs include total areas by Land Class and Broad Habitat with 95% confidence intervals, and corresponding raster estimates for spatial distribution.
- Freshwater habitats were analyzed using a different statistical model than terrestrial habitats.

## Data Content and Structure

- CS007_Broad_Habitat_Stock.csv
  - Columns:
    - YEAR: survey year
    - LAND_CLASS: ITE Land Class
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description
    - LAND_CLASS_AREA: total area of the relevant Land Class (000s ha)
    - MEAN_ESTIMATE: mean area of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: lower bound (95% CI) (000s ha)
    - UPPER_ESTIMATE: upper bound (95% CI) (000s ha)
  - Notes:
    - MEAN_ESTIMATE values may be negative due to the statistical model; treat as zero.
    - Freshwater habitats use a different statistical model from other habitats.

- CS2007_Stock.tif
  - Raster representation: 1 km pixel resolution; each band corresponds to a Broad Habitat class.
  - Per-pixel values represent mean percentage of habitat within each Land Class stratum, derived from 1 km survey squares.
  - Habitat-band mappings indicate how Broad Habitat class codes align with raster bands (e.g., Broad Habitat 1/2 correspond to Coniferous/Deciduous woodland in band designations; various bands map to other habitat types).

## Spatial Information

- Spatial resolution: 1 km (pixel size 1000 m).
- Coordinate system: British National Grid (OSGB36), Transverse Mercator projection.
- Extent: Great Britain (GB).

## Data Quality, Metadata, and Use Notes

- Data use and publication must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; copyright restrictions apply.
- Data interpretation notes:
  - Some MEAN_ESTIMATE values may be negative due to the statistical model; treat as zero in analysis.
  - The 2007 results provide a baseline for monitoring habitat extent by land class and habitat type.
  - Freshwater habitats are modeled differently from terrestrial habitats; consider this when comparing across habitat groups.
- Metadata and references are provided to support methodological understanding and reproducibility (e.g., Scott 2007 statistical methodology, Bunce et al. land classification, Jackson 2000 guidance on broad habitat classification).

## How This Supports Monitoring Frameworks

- Provides a structured, policy-relevant set of environmental health measures:
  - National-scale estimates of Broad Habitat stock by Land Class (Habitat extent and distribution).
  - Spatial maps at 1 km resolution to identify geographic patterns and hotspots.
  - Quantified uncertainty through 95% confidence intervals alongside point estimates.
- Facilitates monitoring, evaluation, and decision-making:
  - Baseline (2007) for trend analysis and policy impact assessment.
  - Ability to communicate findings via tables and maps (CSV and TIFF formats).
  - Data governance and provenance are explicit, aiding transparency and reproducibility in monitoring reports.
- Supports data integration:
  - Compatible with GIS workflows for visualization and dashboarding.
  - Links between Land Class and Broad Habitat enable cross-walks with other land-use or biodiversity datasets.

## Provenance and References

- Core dataset from Countryside Survey 2007; associated publications include:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No.4/07: Statistical methods for deriving national estimates
  - Bunce et al. (1996, 1981) ITE Merlewood Land Classification
  - Jackson (2000) Guidance on Biodiversity Broad Habitat Classification
- Additional CS resources and methodology documents available via Countryside Survey website.