# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

## Overview
- The document maps Broad Habitats to LCM2000 Target Classes, Subclasses, and Variants, and links these to Suclasses used in map displays.
- It serves as a crosswalk between land cover classifications (LCM2000) and field-survey classifications (CS2000/FS), enabling comparisons and data translation across classification schemes.

## Data Sources and Classifications
- LCM2000: Land Cover Map 2000, statistics derived from a full count on a 25 m grid.
- FS / CS2000: Field survey data used to calibrate and compare against LCM2000 classifications (FS = field survey; CS2000 = crosswalk classification in CS2000 format).
- Footnotes clarify data sources and differences between LCM2000 and FS, including coastal coverage variability and population definitions for survey squares.

## Key Tables and Content

- Table 5: Coverage (km2)
  - Presents the area coverage of Subclasses from LCM2000 and Aggregate classes (bold) from LCM2000 and field survey (FS) across England, Wales, Scotland, Northern Ireland, and UK totals.
  - Includes major habitat groups such as broad-leaved/mixed woodland, coniferous woodland, arable & horticulture, improved grassland, neutral/calcareous/acid grasslands, bracken, bog, fen/marsh/swamp, dwarf shrub heath, montane habitats, inland bare ground, built up areas & gardens, littoral and supra-littoral categories, and coastal/oceanic classifications.
  - Notable totals: UK LCM2000 total = 246,688 km2; FS totals often not available (n/a) in this table. Regional totals are provided for each habitat category.

- Table 6: LCM2000 cover (uncalibrated) vs FS estimates (GB, England, Wales, Scotland, Northern Ireland)
  - Compares LCM2000 cover with Field Survey (FS) estimates at 95% confidence intervals (Low/High) for key habitat classes (e.g., broadleaved/mixed & yew woodland, coniferous woodland, arable & horticulture, improved grassland, neutral/calcareous/acid grasslands, bracken, fen/marsh/swamp, bog, montane habitats, inland rock, built up areas & gardens, supralittoral and littoral classifications, etc.).
  - Provides per-country and GB-wide comparison ranges to assess alignment and discrepancies between LCM2000 and FS.

- Table 8, 9, 10: Summary correspondence matrices (per 1000)
  - Table 8: GB-wide comparison of LCM2000 with CS2000 field squares; results expressed per 1000, weighted by 40 Land Classes; bootstrapped confidence intervals; includes broad habitats, urban generalisation considerations, target class, and aggregate class levels.
  - Table 9: England & Wales subset of the CS2000 comparison; same methodology and interpretation as Table 8.
  - Table 10: Scotland subset of the CS2000 comparison; same methodology and interpretation as Table 8.
  - These tables include crosswalk mappings showing how often a CS2000 category aligns with each LCM2000 target class, subclass, or aggregate, along with confidence bounds.

## Regional Coverage and Totals
- The document provides regional (England, Wales, Scotland, Northern Ireland) and UK-wide tallies for each habitat class and cross-classification.
- It also documents where FS data are incomplete or not available (n/a) and notes differences in total coverage definitions between FS and LCM2000.

## Data Quality, Uncertainty, and Methodology
- Uncertainty is addressed via 95% confidence intervals for FS estimates and bootstrapped confidence intervals for correspondence matrices.
- Differences between LCM2000 statistics and FS statistics are acknowledged and explained in the text.
- Coastal coverage is variable due to tidal state and offshore area inclusion/exclusion.
- FS populations in Northern Ireland and some UK-wide totals may exclude certain BHs; footnotes specify these definitional nuances.
- The data enable calibration but require careful interpretation when applying the crosswalk across regions or scales.

## Implications for Data Support
- Provides a comprehensive crosswalk to translate between LCM2000 classes and field survey classifications, aiding data integration and product development.
- Highlights where data alignment is robust and where discrepancies exist, guiding quality assurance and refinement of data products.
- Shows the need for consistent definitions of habitat totals and survey coverage when aggregating across regions.

## Potential Data Products and Uses for a Data Support Archetype
- Self-serve dashboards and reports:
  - Interactive crosswalk maps showing LCM2000 vs CS2000/FS classifications by region and habitat type.
  - Region-specific summaries with uncertainty bounds for key habitat classes.
- Data quality dashboards:
  - Visualizations of discrepancies between LCM2000 and FS (e.g., over/underestimation by habitat type) with confidence intervals.
  - Coastal coverage indicators and their impact on regional totals.
- Data transformation pipelines:
  - Automated translation of LCM2000 target classes, sub-classes, and variants to CS2000/FS equivalents for reporting and visualization.
  - Calibration routines using Table 6 style comparisons to adjust LCM2000-based products to field-survey baselines.
- Documentation and metadata artifacts:
  - Clear metadata describing sources (LCM2000, CS2000, FS), grid resolution (25 m), and differences in survey population definitions.
  - footnote-driven annotations to explain regional and methodological nuances to end-users.