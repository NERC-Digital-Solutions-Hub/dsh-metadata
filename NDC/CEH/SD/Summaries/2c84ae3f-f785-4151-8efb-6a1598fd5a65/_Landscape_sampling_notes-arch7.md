# Summary Experimental Design/Sampling Regime

- Purpose and scope
  - Documents field-scale sampling of earthworms and associated soil properties across multiple farms to enable spatial analysis and map-based visualization of earthworm distribution relative to hedges and field margins.

- Study sites and design
  - Locations: Little Langton (LL), Hutton Wandesley (HW), Overton (OV), Whenby (WH).
  - Landuse categories: organic arable (A1), conventional arable (A2), organic ley (B1), organic arable (B2), conventional ley.
  - Sampling structure: 1 transect per site (some paired transects for comparison); transects run perpendicular from hedge into the field.
  - Distances and sampling sequence: soil pits at hedge, margin, then at 2, 4, 8, 16, 32, and 64 metres from hedge.
  - Sampling dates: 12–26 May 2016.
  - Hedge-related sampling: hedge condition used to locate transects; margins and hedges sampled separately (H = hedge, M = margin).

- Field collection methods and instrumentation
  - Soil pits: 18 x 18 x 15 cm excavated along transect at specified positions.
  - Earthworm extraction: mustard solution (dilute allyl isothiocyanate) used to elicit earthworms, which were collected and preserved for identification.
  - Identification: earthworms identified with Sims and Gerard field studies key; specimens preserved in ethanol.
  - Additional measurements at each pit/transect: soil moisture readings (three measurements in mV at 5 and 10 cm depths), soil temperature at 5 and 10 cm, soil bulk density (5 and 15 cm depth) using standard rings; data collected per pit and depth.

- Data types and structure
  - Earthworm data (landscape CSV files)
    - Files: HWA1_EW_landscape.csv, HWB_EW_landscape.csv, LLA1_EW_landscape.csv, LLA2_EW_landscape.csv, LLB1_EW_landscape.csv, LLBS_EW_landscape.csv, OV7_EW_landscape.csv, WHA_EW_landscape.csv, WHB_EW_landscape.csv.
    - Structure: 30 columns with headings including Date, Field, Transect, Distance (from hedge; H = hedge sample, M = margin sample), Depth (Mustard = P; Topsoil = S), Sample type (A = abundance/count, B = biomass in grams), plus a column for each species code and its count/biomass.
    - Species and codes: list of endogeic, epigeic, and anecic species with corresponding codes (e.g., Allolobophora chlorotica, Aporrectodea caliginosa, Eisenia fetida, Lumbricus terrestris, etc.), plus categories END-dm, EPI-dm, ANE-dm, END-im, EPI-im, ANE-im to indicate damaged or immature states.
  - Soil data (landscape 2016)
    - File: Landscape2016_soil_data.csv
    - Structure: 14 columns including Date, Field, distance_m (from hedge), Hedge/Margin indicator, Depth designation, Moisture (multiple columns for 5 cm and 10 cm depths), Soil Temp (5 cm and 10 cm), Soil Bulk Density (5 cm and 15 cm).
    - Additional context: units in millivolts for moisture readings, degrees Celsius for temperature, and g/cm^3 for bulk density.
  - Miscellaneous
    - Earthworm functional groups: Endogeic (soil-living, horizontal burrows), Epigeic (litter-living), Anecic (soil-living, deep vertical burrows).

- Data content and coding notes
  - Abundance vs biomass: coded via Sample type A (abundance) or B (biomass in grams).
  - Distance descriptors: Distance values are from hedge; Hedge (H) and Margin (M) indicate sample location relative to hedges.
  - Species coding: explicit mapping of species names to codes; includes both standard taxa and functional group labels.

- GIS and data integration implications
  - Enables map-based visualization of earthworm abundance/biomass and soil properties across transects and fields.
  - Distance-from-hedge as a key spatial variable for spatial analyses and interpolation.
  - Potential to join with site-level polygon data (field boundaries, hedge lines) to produce habitat-landscape maps.
  - Data can be used to compare soil moisture, temperature, and bulk density alongside biological metrics along hedgerows and margins.

- Data quality considerations and challenges
  - Data are spread across multiple files and formats; careful data integration and standardization required for GIS workflows.
  - Some cells may be blank (no data) for certain species or measurements; handle missing data appropriately in analyses.
  - Consistency of depth descriptors and depth-specific measurements across files should be verified before mapping.

- Reference
  - Sims & Gerard (1999) as cited in the dataset documentation.