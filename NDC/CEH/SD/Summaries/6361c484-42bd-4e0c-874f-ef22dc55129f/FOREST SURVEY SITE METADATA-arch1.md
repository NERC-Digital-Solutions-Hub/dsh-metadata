# Dataset of Planting Records with Spatial Coordinates and Planting History

## Overview
- A large, detail-rich dataset of planting histories for numerous plots labeled with codes such as A1, A2, A7, A8, etc., plus B-, C-, D-, E- prefixes.
- Each plot includes spatial coordinates (Easting, Northing) and a record of its planting history: first planting year, tree species, soil type, year felled (or status such as Standing crop), and year of any second planting with corresponding species.
- Temporal details are encoded with Start date and End date fields (day, month, year), using formats like Day, Month, Year where Year is often two digits (e.g., 95 = 1995, 97 = 1997).
- Many plots show second-planting information (year and species), while others have NA (not applicable) for second planting.
- The dataset includes a mix of species (e.g., Sitka spruce, Norway spruce, Western hemlock, Japanese larch, Lodgepole pine, Scots pine, Douglas fir, Noble fir) and soil types (e.g., Gley, Podzol, Bog, Brown earth).

## Data structure and variables
- Spatial: Easting, Northing coordinates for each plot.
- Temporal and planting history:
  - First planting year
  - Year felled or standing crop status
  - Second planting year (if any) and second planting species
  - Start date and End date for each planting cycle (day, month, year, often with two- or three-part encoding)
- Biological: Tree species for first and second plantings (when applicable)
- Edaphic: Soil type
- Status indicators: End date may reflect felled year or indicate ongoing status as “Standing crop”; NA entries reflect missing data or inapplicable fields

## Key patterns and observations
- Sitka spruce is the most frequent species across many plots; numerous other species appear, including Norway spruce, Western hemlock, Japanese larch, Lodgepole pine, Scots pine, Douglas fir, Noble fir, and more.
- Planting activity spans primarily mid-20th century to the late 20th century, with felled or standing crop statuses commonly noted around 1990s (e.g., felled around 1994, end dates 97 corresponding to 1997).
- Second planting events occur in numerous plots, often within the 1990s (e.g., 1994–1996) and sometimes with different species than the first planting.
- Soil types show modest diversity (Gley variants, Podzol, Bog, Brown earth), suggesting exploration of species–soils relationships.
- Some plots remain as Standing crop, indicating not yet harvested, while others have explicit felled years or end dates.
- Spatial distribution features diverse Easting/Northing values, indicating a wide geographic coverage within the grid system.

## Data quality and limitations
- Date fields use mixed encodings (Day/Month/Year separated, two-digit year shorthand), requiring normalization for precise temporal analyses.
- Several fields contain NA values, especially for second planting data or End date in some records.
- Inconsistencies such as “Standing crop” used in the Year felled field rather than a numeric year, and variations in capitalization or wording, may require standardization.
- The dataset appears to be a raw export with variable completeness and potential duplicates or multi-line per-plot entries that need consolidation for analysis.

## Potential analyses and use cases
- Analyze rotation lengths by species and soil type (first planting vs. second planting timelines).
- Explore spatial patterns in species deployment and soil suitability across the study area.
- Assess harvest timing and remaining stands (Standing crop) to model timber yield and rotations.
- Compare second-planting choices across sites with similar edaphic and geographic characteristics.
- Build predictive models for likely second-planting species or rotation intervals given soil type, initial species, and location.

## Recommendations for analysts
- Clean and normalize date fields: convert Day/Month/Year triplets into a consistent date format; translate two-digit years to four-digit years.
- Standardize categorical values: unify species and soil type terminology (e.g., Sitka spruce vs Sitka Spruce; Gley variants; Podzol types).
- Reconcile Year felled vs Standing crop: ensure consistent representation of harvest status and numeric years where applicable.
- Create a unique plot key by combining plot code (e.g., A1) with coordinates to support robust joins and avoidance of duplicates.
- Consider converting Easting/Northing to a common projection or enabling mapping in a GIS for spatial analyses.
- Document data limitations and gaps alongside any analyses to reflect NA fields and potential biases due to incomplete second-planting records.