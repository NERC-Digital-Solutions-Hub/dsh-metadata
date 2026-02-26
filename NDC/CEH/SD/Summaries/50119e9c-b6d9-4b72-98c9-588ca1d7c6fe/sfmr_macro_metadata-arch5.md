# Macroinvertebrate data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Data type: Monitoring
- Size: 140KB
- Interpreted by: All authors
- Collection purpose: Assess macroinvertebrate response to wildfire in restored and unrestored sites of the South Fork McKenzie River
- Data description: Biomonitoring data including BMI samples collected in fall or winter; density or biomass per site, standardized to 1 m2; sorting, identification, and body length measurements performed by Robert (Bob) Wisseman; includes site and sample metadata, with site-specific MasterSite naming and CodeUnique keys.

## Dataset structure and files
- Four CSV files:
  - SFMR_Macro_Traits: taxonomic and trait data (e.g., Insect, Origin, Classification, Order, Family, Genus_species, Lifestage, CodeUnique, FFG, Habit, Tolerance, Voltinism, Seasonal, Drift, Size, Rheophily, Thermal)
  - SFMR_Macro_Coordinates: site coordinates and context (ID, MasterSite, Trmt, Restoration, Width_Avg_ft, No_samples, GPS_bank, Lat_WGS84, Long_WGS84, Notes)
  - SFMR_Macro_Samples: sample-level data (River, OrigSite, Date, Transect, MasterSite, SiteYearSeason, Year, Season, Trmt, Post_mos, Post_Fire, Restoration, H_macro, H_micro, Cover_pct, Temp_C, Width_m, Depth_max_m, Depth_avg_m, SISA_pct, GR_pct, CO_pct, BO_pct, NonvascVeg_pct, EmergVeg_pct, AqVeg_pct, BMIwood_pct, Notes)
  - SFMR_Macro_Species: species-level data (Year, Season, MasterSite, SiteYearSeason, Density, Biomass_mg, CodeUnique, Stage, Taxon_Wisseman)
- Trait definitions (SFMR_Macro_Traits) cover taxonomic levels, life stage, functional feeding group (FFG), habitat preferences (Rheophily), size classes, and thermal tolerances.
- Key identifiers:
  - MasterSite provides consistent site naming across spreadsheets
  - CodeUnique provides a unique taxon code; used to link trait and species data
  - Samples per site and time period are organized with Post_mos (months since restoration) and Post_Fire (pre/post wildfire)

## Collection methodology and data quality
- Sampling method: 1 ft net, 10 samples per site along a transect across the river channel; samples collected irrespective of transect length
- Special notes:
  - Filamentous algae not filtered; defined as floating/rooted within water identified visually
  - BMI wood defined as a sample within 1 ft of a large woody object
  - Pre-restoration transects marked with stakes; post-restoration stakes largely washed away; site identification relied on GPS with 3–4 m error
  - Macroinvertebrates identified to species or genus by Robert Wisseman; taxa traits drawn from his database
  - Temperature: USGS gauge near Cougar Dam used due to inconsistent handheld thermometer data
- Collection dates and sites:
  - 17 sites from fall 2019 (10 samples per site)
  - 12 sites from fall 2020 (10 samples per site)
  - 10 sites from winter 2021 (10 samples per site)

## Data content and units
- Data are organized as:
  - Density and Biomass measurements (Density in individuals per m2; Biomass in mg per m2) with standardization to 1 m2
  - Sample-level metadata includes: date, transect, restoration/testing condition (pre/post restoration or reference unburned site), canopy cover, substrate composition (SISA, GR, CO, BO), vegetation, water temperature, and physical dimensions
  - Species-level data provide Density and Biomass per MasterSite and time period, using CodeUnique and Stage for life stage

## Metadata and governance considerations for Data Stewards
- Data provenance and lineage:
  - Data collected across multiple years/sites with restoration context; includes before/after restoration and post-wildfire conditions
  - MasterSite and CodeUnique keys enable cross-file joins and consistent attribution
- Data quality considerations:
  - Temperature data quality is limited due to instrument issues; temperature field relies on USGS gauge
  - GPS positioning has a 3–4 m error margin after stakes were washed away
- Data consistency and interoperability:
  - Trait and species definitions are standardized in dedicated CSVs; ensure ongoing alignment between SFMR_Macro_Traits and SFMR_Macro_Species
  - Units are specified (Density per m2, Biomass in mg per m2; canopy cover and substrate percentages in percent)
- Documentation and reuse:
  - Include the four CSV files and the trait definitions CSV together when sharing
  - Preserve MasterSite, Trmt, Restoration, and CodeUnique fields to maintain relational integrity
  - Clearly document data collection context (pre/post restoration, Post_mos, Post_Fire)

## Practical considerations for end users
- Suitable for analyses of macroinvertebrate responses to wildfire and restoration across multiple sites
- Useful for assessing community structure via taxon-level traits (e.g., FFG, Size, Tolerance) and for linking to environmental/contextual variables (canopy cover, substrate, temperature)
- Ensure proper data handling of time-series and site-level linking using MasterSite and CodeUnique
- Verify date formats and seasonal coding in SFMR_Macro_Samples for temporal analyses
- Be aware of potential spatial limitations due to GPS uncertainty and reliance on historical stakes for site identification

## Access, reuse, and attribution notes
- Dataset components are provided as separate CSV files with explicit column definitions
- Attribution should reflect all authors who interpreted the data and the primary data collector (Robert Wisseman) for taxon identifications and trait assignments
- If distributing or publishing analyses, reference the four CSV files and the trait definitions CSV as a consolidated data package