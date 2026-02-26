# Summary Experimental Design/Sampling Regime

- Study context and sites
  - Multiple fields across sites: Little Langton (LL), Hutton Wandesley (HW), Overton (OV), Whenby (WH).
  - Land use categories: organic arable (A1, A2), conventional arable, organic ley (B1, B2).
  - Each site features a single transect per field, oriented from hedge into the field; hedges used as reference boundaries.
  - Paired comparisons described (e.g., margins vs. hedge-adjacent areas) to assess edge effects.

- Sampling design and field methods
  - Transect direction: perpendicular to the hedge, positioned mid-field where possible.
  - Sampling points along transects: at hedge, field margin, then at 2 m, 4 m, 8 m, 16 m, 32 m, and 64 m into the field.
  - Soil pits: 18 x 18 x 15 cm excavations at each distance point.
  - Earthworm extraction: Mustard solution (dilute allyl isothiocyanate) released into pits; worms collected, preserved in ethanol, identified with Sims and Gerard field studies key.
  - Additional measurements at each pit: soil moisture (three readings in mV) at 5 cm and 10 cm depths, soil temperature (5 cm and 10 cm), and bulk density (5 cm and 15 cm depth).
  - Samples labeled by location context: Hedge (H) vs Margin (M); depth context: Mustard (P) vs Topsoil (S).

- Measured variables and units
  - Earthworms: counts (abundance) and biomass (grams) per sample.
  - Distance from hedge: meters (position along transect).
  - Sample type: A = abundance/count, B = biomass (grams).
  - Functional groups and codes: Endogeic, Epigeic, Anecic classifications; species-level codes provided.
  - Soil properties (for integration with biological data): moisture (mV readings at 5 cm and 10 cm; separate sets), soil temperature (°C at 5 cm and 10 cm), bulk density (g/cm³ at 5 cm and 15 cm).
  - Data capture context: Date, Field ID, Transect ID, Distance, Depth indicator, Sample type, and species-specific counts/biomass.

- Data structure and files
  - Landscape data files (9 datasets): HWA1_EW_landscape.csv, HWB_EW_landscape.csv, LLA1_EW_landscape.csv, LLA2_EW_landscape.csv, LLB1_EW_landscape.csv, LLBS_EW_landscape.csv, OV7_EW_landscape.csv, WHA_EW_landscape.csv, WHB_EW_landscape.csv.
    - Each file contains ~30 columns with: Date, Field, Transect, Distance, Hedge/Margin indicator, Depth (Mustard or Topsoil), Sample type (A or B), plus columns for counts/biomass per earthworm species.
    - Species list includes Allolobophora chlorotica, Allolobophoridella eiseni, Aporrectodea caliginosa (and nocturna), Aporrectodea limicola, Aporrectodea longa, Aporrectodea rosea, Dendrodrilus rubidus, Eisenia fetida, Eiseniella tetraedra, Lumbricus castaneus, L. festivus, L. rubellus, L. terrestris, Murchieona muldali, Octolasion cyaneum, Octolasion tyrtaeum, Satchellius mammalis, plus placeholder/damaged categories.
  - Soil data file (Landscape2016_soil_data.csv): 14 columns with Date, field name, distance, Hedge/Margin flag, moisture readings (three per depth and site), soil temperature (5 cm and 10 cm), and bulk density (5 cm and 15 cm).
  - Miscellaneous/functional groups included to classify earthworm data into Endogeic, Epigeic, and Anecic groups and to map species to these functional categories.

- Data interpretation and potential analyses
  - Primary aims: characterize earthworm communities across distance from hedge and across land-use types; identify edge effects and habitat associations.
  - Analyses enabled by dataset:
    - Species-level abundance and biomass gradients with distance from hedge and by habitat (hedge vs margin).
    - Functional group distribution (Endogeic, Epigeic, Anecic) across distances and land-use types.
    - Relationships between earthworm metrics and soil properties (moisture, temperature, bulk density).
    - Multivariate analyses of community composition using species-level data.
  - Data provenance and references: identification keys based on Sims & Gerard (1999).

- Important notes on data quality and structure
  - Some samples include blank cells where data are not available.
  - Data are collected from a limited number of transects per field (one per field), primarily for comparative edge effects.
  - The dataset documents explicit field contexts (hedge type, margin status, depth, and distance), enabling replicability and meta-analysis when combined with soil data.