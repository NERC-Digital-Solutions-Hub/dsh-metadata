# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

- Describes how broad habitat types map to LCM2000 Target classes, Subclasses, and Variants, with map display colors for Subclasses and Variants.

## Key content and data products

- Mapping framework for map-based data visuals:
  - Broad Habitats linked to LCM2000 Target Class, Subclass, and Variant (color-coded for display).
- Table 5 provides extensive area (km2) data:
  - Coverage of Subclasses from LCM2000 and aggregates (bold) from LCM2000 and field survey (FS) across the UK and constituent countries.
  - Examples include Broad-leaved woodland, Coniferous woodland, Arable cereals, Arable horticulture, Improved grassland, Neutral/Calcareous/Acid grasslands, Bracken, Fen/marsh/swamp, Bog, Built up areas, Urban/rural developments, and various coastal/bathymetric categories.
  - Shows totals by country (England, Wales, Scotland, NI) and UK-wide totals, with both LCM2000 and FS figures.
- Table 6 (uncalibrated LCM2000 cover vs FS field survey):
  - Presents LCM2000 estimates for Broad Habitats (BHs) alongside field survey (FS) lower and upper bounds (Low/High) for England, Wales, Scotland, and GB, plus NI.
  - Enables assessment of calibration needs and uncertainties between LCM2000 and FS estimates.
- Tables 8–10 (summary correspondence matrices):
  - Cross-wold comparisons between LCM2000 and CS2000 field survey squares in GB, England & Wales, and Scotland.
  - Express results per 1000 (or per 1000s) and include bootstrapped confidence intervals.
  - Show how CS2000 broad habitats map to LCM2000 target classes, subs, and variants, including multiple harmonized cross-walk rows (e.g., Broad Habitats, Target Class, Aggregate Class, and various habitat pairings).
- Table footnotes:
  - Explain methodology: LCM2000 statistics derived from a full count of cover on a 25 m grid; FS statistics from Haines-Young et al. 2000.
  - Clarify definitions: BH = Broad Habitats; FS population definitions (1 km squares) and regional exclusions (notably NI survey exclusions).
  - Note coastal coverage variability due to tidal states and offshore areas; some data are not available (n/a); and differences explained in the text.
  - Indicate the use of 40 Land Classes for bootstrapping and the generalisation of urban areas in some matrices.

## Data sources and resolution

- LCM2000:
  - Full cover count on a 25 m grid (high-resolution raster-based dataset).
  - Used to derive Subclasses and Aggregates for UK-wide habitat mapping.
- CS2000/FS:
  - Field survey data (CS2000) used for cross-walks and validation against LCM2000.
  - FS (field survey) statistics come from Haines-Young et al. 2000.
- Cross-walks and comparisons:
  - Tables 8–10 provide correspondences between LCM2000 and CS2000/FS classifications across Broad Habitats, Target Classes, and Aggregates.

## Practical implications for GIS specialists

- Map product development:
  - Use Table 1’s mapping to symbolize habitats consistently across map products (Target Class, Subclass, Variant with color codes).
- Data integration and harmonization:
  - Employ the crosswalk matrices (Tables 8–10) to align LCM2000 classifications with CS2000/FS classifications when assembling multi-source GIS layers.
- Quality assessment and uncertainty:
  - Leverage Table 6 to understand uncalibrated LCM2000 vs FS estimates and incorporate confidence ranges into map metadata or uncertainty layers.
- Regional and coastal considerations:
  - Be aware of coastal coverage variability and offshore inter-tidal inclusions when calculating extents or performing analyses near coastlines.
- Handling data scale and complexity:
  - Tables 5 and 6 illustrate the large, detailed datasets by habitat type and country; plan for data management and processing to handle numerous categories, empty values (n/a), and potential inconsistencies.
- Data challenges aligned with GIS Specialities:
  - Data are spread across multiple sources with differing resolutions and standards; significant cleaning, transformation, and validation are required.
  - Teams may need specialized skills to manage calibration, cross-walk implementation, and uncertainty visualization.

## Beginning, middle, and end narrative alignment

- Beginning: Establishes the purpose of linking broad habitats to LCM2000 classes for map-based data visualization and interpretation.
- Middle: Provides detailed, country-level extents and cross-walks (Tables 5, 6, 8–10) and discusses calibration and validation against field surveys (FS/CS2000), including uncertainties and methodological notes.
- End: Includes footnotes clarifying data origins, definitions, limitations, and specific caveats for coastal coverage and NA values, highlighting considerations for GIS implementation and data quality management.