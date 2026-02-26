# Vegetation data from the South Fork McKenzie River in Oregon, USA.

- Purpose and scope
  - Monitoring dataset to assess vegetation response to wildfire in restored and unrestored sites.
  - Collected June 2021 across treatments: restored.burned, unrestored.burned, unrestored.unburned (reference site).

- Data files and structure
  - Four CSV files:
    - SFMR_Veg_Coordinates: Transect, Quad, Lat, Long.
    - SFMR_Veg_Species: Transect, Site, Quad, Treatment, Initials, Species.name, Cover.Class, Cover.2, Comments, Category, Family, Duration, Growth_Habit, Native_Status. Includes taxonomy, native status, and cover data (Braun-Blanquet scale and percentage conversion).
    - SFMR_Veg_Ground: Transect, Quad, Type, Cover_Class, Cover_class_pct.
    - SFMR_Veg_Canopy: Transect, Quad, Measurement, Densiom (canopy openness).
  - Dataset captures 69 total taxonomic units (40 identified to genus/unclear; 29 to species).

- Sampling design and methodology
  - 20 quadrats total, using Braun-Blanquet abundance estimates (% cover).
  - 8 quadrats along transects 1 and 2 in restored/burned treatment; 4 paired quadrats with soil data; 4 quadrats paired with soils sampling locations in unrestored/degraded/burned; 3 quadrats in unburned/non-degraded treatment.
  - Ground cover and canopy measurements per quadrat; canopy measurements recorded in cardinal directions (North/East/South/West).

- Data quality and collection practices
  - Collected by trained fieldworkers following standardised procedures.
  - Data digitised from field sheets and double-checked prior to upload.

- Taxonomy and data details
  - Species-level data includes species name, growth form, life duration, and native status.
  - Coverage data includes Cover.Class (Braun-Blanquet scale) and converted percent cover (Cover_class_pct).

- Considerations for use and governance
  - Rich, multi-file structure supports integration with broader data systems and cross-site analyses (e.g., linking coordinates with treatment metadata and soil data).
  - Clear documentation of treatments and sampling design aids reproducibility and co-ownership of data products.
  - Metadata completeness at the level of classification, growth habit, native status, and canopy measurements enhances discoverability and reusability.

- Limitations and caveats
  - Relatively small spatial scope with 20 quadrats; caution in extrapolating beyond study sites.
  - Some taxa identified only to genus/unclear rather than species level.