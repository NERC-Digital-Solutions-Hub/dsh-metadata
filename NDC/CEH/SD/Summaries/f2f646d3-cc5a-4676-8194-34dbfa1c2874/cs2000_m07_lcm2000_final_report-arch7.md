# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

- Overview
  - Presents a crosswalk between broad habitat types and LCM2000 Target classes, Subclasses, and Variants, including Suclasses shown in map colors.
  - Demonstrates how LCM2000 categories align with habitat concepts used in CS2000 field survey and related classifications.

- Data sources and methodology
  - LCM2000 data derived on a 25 m grid; compared against field survey data (FS) from Haines-Young et al. 2000.
  - Tables footnoted to clarify differences between LCM2000 and FS, coastal coverage variability due to tidal state and inclusion/exclusion of offshore inter-tidal areas, and total coverage definitions.
  - Summary correspondences and crosswalks are presented at multiple aggregation levels, including Target Class, Aggregate Class, and Broad Habitats.
  - Tables 8–10 use weighted estimates and bootstrapping across 40 Land Classes to derive confidence intervals for CS2000 comparisons in GB and England/Wales.

- Key tables and what they show (highlights)
  - Table 5: The coverage (km2) of Subclasses from LCM2000 and of Aggregate classes from LCM2000 and FS in the UK and constituent countries.
    - Provides territory-wide totals by habitat type (England, Wales, Scotland, NI) and the UK total for major classes such as broadleaved/mixed woodland, coniferous woodland, arable cereals, arable & horticulture, improved grassland, neutral/calcareous/acid grasslands, bracken, fen/marsh/swamp, bog, standing open water, built-up areas, and urban/extensive coastal classes.
    - Includes detailed breakdowns for subcategories like inland water, urban/suburban development, coastal and supralittoral/lareral elements, and various littoral and offshore components.
    - Notable UK totals (LCM2000): total cover around 246,688 km2; country-level sums shown (England ~130,362 km2; Scotland ~77,898 km2; NI ~17,739 km2; Wales ~20,689 km2).
  - Table 6: LCM2000 cover (uncalibrated) for Broad Habitats (BHs) for England, Wales, Scotland, Northern Ireland, and GB, with field survey estimates at 95% confidence (low/high) for GB and subregions.
    - Enables quick assessment of how LCM2000 area estimates compare to field-derived expectations at coarse habitat levels.
  - Tables 8–10: Summary correspondence matrices (results expressed per 1000) comparing LCM2000 with CS2000 field survey squares in Great Britain (Table 8) and England & Wales (Table 9) and with Scotland (Table 10).
    - Provide weighted correspondences across levels: Broad Habitats (yellow), Target Class (pink), and Aggregate class (green) with urban generalisation adjustments (blue).
    - Show how often a CS2000 class is represented within a given LCM2000 class and vice versa, serving as a crosswalk for validation and data fusion.
    - Include notes on the directional mappings (e.g., CS2000 categories mapped to LCM2000 target classes, aggregates, and urban/generalisation effects).

- Practical implications for GIS work
  - Use the crosswalks to translate LCM2000 map layers into field-survey-compatible classifications (CS2000) for validation, reporting, or stakeholder communication.
  - Leverage the 25 m resolution and tabulated area estimates to quantify habitat extents, perform area-change analyses, or drive map-based products (themes, legends, color schemes) consistent with field-derived semantics.
  - Apply the confidence intervals from Table 6 and the bootstrapped correspondences from Tables 8–10 to assess uncertainty and to document reliability when blending LCM2000 with CS2000 data in map products.
  - Be mindful of documented caveats:
    - Coastal coverage variability due to tidal states and inclusion/exclusion of offshore areas.
    - Differences between calibrated vs uncalibrated LCM2000 figures and the need for potential calibration when precise area estimates are required.
    - Urban generalisation and the level of detail appropriate for map scale and user audience.

- End notes and caveats for interpretation
  - Footnotes explain that LCM2000 statistics come from a full count based on a 25 m grid and that FS statistics originate from Haines-Young et al. 2000; some data are not available (n/a) for certain UK regions.
  - Differences between LCM2000 and FS statistics are discussed in the accompanying text, including how coastal and urban areas are treated in map display and analysis.
  - The matrices are designed to support cross-language GIS workflows, crosswalking map themes, and validating broad habitat classifications against field-derived suitability categories.