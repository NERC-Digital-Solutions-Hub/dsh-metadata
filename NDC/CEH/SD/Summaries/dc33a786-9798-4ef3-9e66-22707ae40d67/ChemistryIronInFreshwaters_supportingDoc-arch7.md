# IRONCHEMISTRYDATA1-4.csv

- Purpose and contents
  - A multi-file iron chemistry dataset intended for GIS-based visualization and analysis of site-based water chemistry and dialysate fractions.
  - Data across four CSV files (IRONCHEMISTRYDATA1.csv to IRONCHEMISTRYDATA4.csv) plus notes and location metadata.
  - Each file includes a SampleSite and SampleDate for temporal and spatial context.

- Data schema by file
  - IRONCHEMISTRYDATA1.csv
    - SampleSite: Name of site
    - SampleDate: Date sample was collected
    - pHfield: pH in the field
    - pHfinal: pH retested in the laboratory
    - DOC: dissolved organic carbon (mg dm3)
    - Na, Mg, Ca: sodium, magnesium, calcium (µeq dm3)
    - Cl: chloride (µeq dm3)
    - NO3: nitrate (µeq dm3)
    - SO4: sulphate (µeq dm3)
    - alklinity: alkalinity (µeq dm3) [note: spelling in dataset]
    - total_Fe, total_Fe_II: total iron and iron(II) (µg dm3)
    - filtered_Fe, filtered_Fe_II: filtered iron and iron(II) (µg dm3)
    - total_monomeric_Al, total_acid_reactive_Al: aluminium species (µg dm3)
  - IRONCHEMISTRYDATA2.csv
    - SampleSite, SampleDate
    - 3_5kDa_dialysates_Fe: iron in 3.5 kDa dialysate (µg dm3)
    - 3_5kDa_dialysates_Fe_II: iron(II) in 3.5 kDa dialysate (µg dm3)
    - 3_5kDa_dialysates_DOC: dissolved organic carbon in dialysate (mg dm3)
    - 3_5kDa_dialysates_monomeric_Al: monomeric aluminium in dialysate (µg dm3)
  - IRONCHEMISTRYDATA3.csv
    - SampleSite, SampleDate
    - 10kDa_dialysates: iron in 10 kDa dialysate (µg dm3)
    - 10kDa_dialysates_Fe, 10kDa_dialysates_Fe_II: iron and iron(II) in 10 kDa dialysate (µg dm3)
    - 10kDa_dialysates_DOC: DOC in 10 kDa dialysate (mg dm3)
    - 10kDa_dialysates_monomeric_Al: monomeric aluminium in 10 kDa dialysate (µg dm3)
  - IRONCHEMISTRYDATA4.csv
    - SampleSite, SampleDate
    - 15kDa_dialysates_Fe: iron in 15 kDa dialysate (µg dm3)
    - 15kDa_dialysates_Fe_II: iron(II) in 15 kDa dialysate (µg dm3)
    - 15kDa_dialysates_DOC: DOC in 15 kDa dialysate (mg dm3)
    - 15kDa_dialysates_monomeric_Al: monomeric aluminium in 15 kDa dialysate (µg dm3)

- Notes on data quality and interpretation
  - Some entries indicate not measured or insufficient sample for analysis.
  - A placeholder "<" is used to denote results below the stated limit of detection in some fields.
  - Dataset spelling irregularities (e.g., "alklinity") should be standardized during data cleaning.

- Location metadata for GIS integration
  - Spatial references provided as Easting/Northing coordinates for multiple sites (e.g., Pool X, Pool Y, Roudsea Wood, River Hodder, River Lune, River Ribble, River Tees, Gais Gill, River Eden, Black Burn, Wad Hazel Sike).
  - Example sites include Roudsea Wood, River Hodder, River Lune, River Ribble, River Tees, and others with precise coordinates.
  - Use these coordinates to create point layers representing sampling sites and to join chemical measurements from the IRONCHEMISTRYDATA files.

- How this supports GIS work
  - Enables map-based visualization of:
    - Field vs. lab pH differences across sites and over time.
    - Concentrations of major ions (DOC, Na, Mg, Ca, Cl, NO3, SO4, alkalinity) and iron species (total and iron(II), both dissolved and filtered).
    - Aluminium speciation (total monomeric Al and total acid-reactive Al).
    - Dialysate fractions at multiple molecular weight cut-offs (3.5, 10, and 15 kDa) for comparative spatial analysis.
  - Facilitates data merging across resolutions and datasets to produce comprehensive GIS layers by site and date.
  - Supports quality assurance workflows: identify missing data, below-detection results, and outliers across datasets before visualization.

- Practical integration notes for GIS specialists
  - Ensure consistent site naming when joining across the four IRONCHEMISTRYDATA*.csv files.
  - Standardize units where necessary (µg dm3, mg dm3, µeq dm3) to maintain compatibility in maps and analyses.
  - Use SampleDate to create time-enabled maps or animations of chemical parameters.
  - Leverage location metadata to build accurate point geometries and explore spatial patterns among rivers, woodlands, and pool locations.