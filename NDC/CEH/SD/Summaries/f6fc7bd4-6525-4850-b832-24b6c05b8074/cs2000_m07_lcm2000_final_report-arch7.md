# Table 1. Broad Habitats and their relation to LCM2000 Target classes, Subclasses and Variants (the Suclasses are shown in their map display colours).

- Provides a crosswalk between LCM2000 broad habitat groupings and CS2000-style target classes, subclasses, and variants.
- Covers a wide range of habitats (inshore sublittoral, standing water, littoral and supra-littoral rock/sediment, montane habitats, woodlands, arable/horticulture, improved and neutral grasslands, bracken, bog, fen, urban/ Built up areas, etc.).
- Indicates that Subclasses and Variants are used for map display and detailed classification within each target class.

# Table 5. The coverage (km2) of Subclasses from Land Cover Map 2000 (LCM2000) and of Aggregate classes (bold) from LCM2000 and field survey (FS) in the UK and constituent countries.

- Presents area statistics (km2) for LCM2000 subclasses and for aggregate classes from both LCM2000 and field survey (FS) across England, Wales, Scotland, Northern Ireland, and the UK.
- Highlights large contributions from Arable & Horticultural, Improved Grassland, and Built up areas/gardens, among others; totals are given at UK and country levels.
- Shows that FS data are incomplete for many categories (n/a in several cells) and that coastal coverage varies with tidal state and inclusion/exclusion of offshore inter-tidal areas.

# Table 6. LCM2000 cover (km2) for BHs (uncalibrated) for England, Wales, Scotland, Northern Ireland and GB, compared with field survey estimates at 95% confidence (i.e. +/- 2 standard errors).

- Compares uncalibrated LCM2000 area with field survey (FS) estimates (low and high) for major broad habitats across GB and its countries.
- Provides 95% confidence ranges for FS, illustrating calibration needs and potential discrepancies between map-based estimates and field observations.
- Demonstrates substantial variation in agreement across habitat types (e.g., woodland, arable, grasslands, fen/bog, standing water) and highlights where calibration is most needed.

# Table 8. Summary correspondence matrix (results expressed per 1000) comparing LCM2000 with CS2000 field survey squares in Great Britain.

- Summarizes how often LCM2000 broad habitats and target/class levels correspond to CS2000 field survey classifications across GB, using 40 Land Classes and bootstrapped confidence.
- Indicates general patterns of correspondence (yellow = Broad Habitats, pink = Target Class, blue = urban generalisation, green = Aggregate class levels).
- Shows that some categories (e.g., Broadleaved/mixed and yew woodland; Coniferous woodland; Improved grassland) have relatively measurable correspondences, while urban/linear features and coastal categories often require generalisation or exhibit more variability.
- Notes that results are weighted and derive from stratified bootstrapping.

# Table 9. Summary correspondence matrix (results expressed per 1000) comparing LCM2000 with CS2000 field survey squares in England and Wales.

- Similar to Table 8 but focused on England and Wales.
- Confirms pattern of varying correspondence by habitat type; some categories align closely, others show lower alignment or require urban generalisation.

# Table 10. Summary correspondence matrix (results expressed per 1000) comparing LCM2000 with CS2000 field survey squares in Scotland.

- Mirrors Tables 8 and 9 for Scotland.
- Highlights differences in correspondence by habitat category across Scotland, including coastal and inland classes.
- Indicates bootstrapped, strata-based estimates and BHlevel considerations.

# Footnotes and Methodology (embedded context from Tables)

- LCM2000 statistics derive from a full count of cover on a 25 m grid; FS statistics from Haines-Young et al. 2000.
- Differences between LCM2000 and FS are discussed; coastal coverage is variable due to tidal states and offshore area inclusion.
- FS totals are sometimes not available for certain categories or regions (noted as n/a).
- Tables 8–10 use bootstrapping across 40 Land Classes to produce confidence intervals; results exclude linear features at BHlevel in some analyses.
- CS2000 is used as the field-survey reference framework for cross-walks with LCM2000.

# Implications for GIS Specialists

- The Table 1 crosswalk enables map-makers to label and symbolize LCM2000-derived layers consistently with CS2000-inspired habitats, aiding audience comprehension.
- Table 5 and Table 6 provide essential context for planning map extents and for understanding potential biases between map-derived cover and field observations; incorporate confidence ranges when communicating uncertainties.
- Tables 8–10 offer a quantitative basis to assess and communicate the degree of agreement between LCM2000 map classes and CS2000 field classifications; useful for validating data products and for informing users about data quality.
- Coastal and urban classifications require careful handling (generalisation and tidal state considerations); document these in metadata and legends.
- Calibration and region-specific differences (England, Wales, Scotland, NI) should be reflected in product legends, attribution, and any differential styling or filtering.

# Practical Takeaways for Data Product Creation

- Use the LCM2000 crosswalk (Table 1) to design map symbology and layer labeling that aligns with CS2000 logic.
- When reporting area, rely on Table 5-style summaries but note that FS data may be incomplete; include notes on data completeness and coastal tide state effects.
- For accuracy reporting, reference Table 6-style comparisons to communicate where LCM2000 maps align with field observations and where calibration is needed.
- When validating across regions (GB, England & Wales, Scotland, NI), use Tables 8–10 as a basis for region-specific quality statements and for planning targeted improvements.
- Ensure metadata captures methodology (25 m grid, bootstrapping, 40 Land Classes, BHlevel vs regions) and clearly states limitations (n/a entries, coastal variability, urban generalisation).