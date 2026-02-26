# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2015.

## Overview
- Captures first-breeding dates for Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus) as an indicator of spring phenology and climate warming.
- Timing is linked to ambient temperature and the phenology of primary prey (tree-dwelling caterpillars) influenced by temperature and bud burst.
- Data contribute to a broader long-term study on habitat, landscape factors, and breeding success of woodland birds in English lowland deciduous woodland.

## Study components
- Species
  - Great Tit Parus major (code: 1)
  - Blue Tit Cyanistes caeruleus (code: 2)
- Study Woods (Cambridgeshire, eastern England)
  - Monks Wood National Nature Reserve (Site 1)
  - Brampton Wood Wildlife Trust Nature Reserve (Site 2)
  - Wennington Wood (Site 3)
- Box and occupancy details
  - Boxes located at 1–2 m height; hole sizes determine species access
  - Dormouse boxes added in Brampton Wood since the mid-1990s, potentially increasing Blue Tit occupancy there
  - Box counts vary by site and period; some boxes are not present in certain sites/years

## Data collection and scope
- Inspection frequency: approximately weekly during the laying period (late March onward)
- First egg dates: calculated from observed eggs assuming one egg per day; dates preceding April 1 appear as negative values
- Inclusion: only active nests at observation time (at least one more egg laid); only first breeding attempts (no replacement clutches or second broods)
- Temporal coverage: 1993–2015 (23 years)

## Data structure (CSV schema)
- File: GTBTfirsteggdates.CSV (Unicode), 42 KB
- Columns
  - Column 1: Species code (1 = Great Tit; 2 = Blue Tit)
  - Column 2: Site (1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood)
  - Column 3: Year number (Year 1 = 1993 to Year 23 = 2015)
  - Column 4: Nest box identifier (note: Monks Wood boxes 23–30 do not exist)
  - Column 5: First egg date (April 1 = 1; March dates negative; only 3 negative values observed in Year 5)
  - Column 6: Sample size (N) for the number of clutches per year

## Quality control and data integrity
- Collected by trained personnel; egg dates checked against original paper records
- Data lines and values checked for outliers
- Egg-date values validated against yearly means per site

## Geospatial and GIS considerations
- Spatial context: three defined study woods with box locations within deciduous woodland habitats
- Data enable mapping of first-egg phenology across sites and years; can be linked to habitat, landscape, and climate datasets
- Box identifiers provide a site-based spatial reference, though explicit coordinates are not included in the dataset itself

## Potential uses for GIS specialists
- Visualize spatial–temporal patterns of breeding phenology across sites and years
- Integrate with environmental layers (temperature, bud burst timing, canopy structure) to model drivers of breeding timing
- Assess relationships between habitat features and breeding phenology at multiple resolutions
- Support data cleaning, transformation, and integration with other long-term avian datasets for landscape-scale analyses

## Limitations and notes
- Data are tied to three specific woods and nest-box-based sampling; box availability varies by site and year
- First-egg dates may be influenced by local management (e.g., dormouse boxes in Brampton Wood)
- March-first dates appear as negative values; only three occurrences were March dates in the dataset's period

## Access and format
- Data available as a single CSV file with a fixed column schema
- Prepared for analysis with Minitab (Release 16) origins, but CSV ensures broad compatibility for GIS workflows