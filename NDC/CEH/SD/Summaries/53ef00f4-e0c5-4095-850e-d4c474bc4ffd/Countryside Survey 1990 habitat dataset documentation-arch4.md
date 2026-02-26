# Broad Habitat Area Estimates by Land Class for Great Britain 1990

## Overview
- Countryside Survey 1990 provides national estimates of Broad Habitat stock (Habitats 1–17) for Great Britain, derived using the 2007 ITE Land Classification.
- Data products include a CSV stock table with area estimates (in 000s ha) and a 1 km pixel raster (cs1990_stock.tif) with mean habitat percentage values per square.
- Freshwater habitats were modeled differently; there was no Montane (BH15) class in 1990.

## Data Products and Structure
- CS1990_Broad_Habitat_Stock.csv
  - Columns: YEAR, LAND_CLASS, BROAD_HABITAT, BROAD_HABITAT_NAME, LAND_CLASS_AREA, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE
  - MEAN_ESTIMATE may be negative due to the statistical model; treat negative values as 0.
  - Provides total area by land class and Broad Habitat with 95% confidence intervals.
- cs1990_stock.tif
  - Raster with 1 km pixel resolution (British National Grid, OSGB36, Transverse Mercator).
  - Each pixel band represents a Broad Habitat class; bands are mapped to habitat types (see band-to-habitat mappings in the dataset notes).
  - 1 km survey squares inform mean habitat percentage within each land class stratum.
  - Note: No Montane habitat in 1990; Band 15 corresponds to BH16 and Band 16 to BH17.

## Spatial and Temporal Scope
- Temporal coverage: Year 1990 (Countryside Survey).
- Spatial coverage: Great Britain.
- Spatial reference: 1 km pixels, OSGB 1936 (British National Grid), Transverse Mercator.

## Classification and Methodology
- Land Classification: 2007 ITE Land Classification (grounded in Bunce et al. and related publications) used to categorize land classes and associated Broad Habitats.
- Broad Habitat codes and names correspond to standard definitions (BH1–BH17, with BH15 absent in 1990).
- Freshwater habitats were modeled separately; explicit notes on model differences for these classes.

## Data Quality, Limitations, and caveats
- Possible negative MEAN_ESTIMATE values; users should treat as 0.
- 1990 dataset lacks the Montane Broad Habitat (BH15); band mappings reflect this absence.
- Data quality depends on the model used to derive national estimates from 1 km squares; see referenced statistical reports for methodology.
- Metadata and provenance are essential for correct interpretation and cross-walks to later datasets (e.g., 2007 results).

## Access, Usage Rights, and Provenance
- Data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey attribution required on all copies, publications, and presentations.
- References and methodological context are provided (publications and links) to support reproducibility and proper usage.

## Key References and Context
- Core Countryside Survey outputs and technical reports (links included in the dataset notes) outlining:
  - Statistical methodology for national estimates from 1 km squares (Scott 2007).
  - ITE Land Classification framework (Bunce et al. 1996; 1981; 2007).
  - Guidance on interpretation of Biodiversity Broad Habitat classifications (Jackson 2000).

## Relevance for Data Leadership and Strategy
- Demonstrates end-to-end data lifecycle management: defining classifications, linking field survey data to national estimates, and producing both tabular and raster products.
- Highlights data discovery and accessibility considerations (two formats: CSV stock table and 1 km raster), with explicit metadata, provenance, and usage rights.
- Illustrates challenges in cross-compatibility across time (e.g., changes in classification systems, absence of certain habitats) and the importance of clear band/habitat mappings.
- Emphasizes the need for robust metadata, clear handling of anomalous values, and acknowledgement requirements to enable reuse across networks and by policy/analytical teams.
- Provides a practical example of leveraging a data asset for informing land-management decisions, spatial planning, and trend analyses across partner organizations.