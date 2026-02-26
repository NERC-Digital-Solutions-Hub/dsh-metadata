# Macroinvertebrate data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Purpose: Monitor macroinvertebrate response to wildfire in restored and unrestored sites.
- Location: South Fork McKenzie River, Oregon.
- Data type: Monitoring; generated as four separate CSV files covering traits, coordinates, samples, and species.
- Use context: Structured for analysis of community responses to restoration and fire, with linkages across site and species levels.

## Dataset structure and contents
- SFMR_Macro_Traits
  - Contains trait definitions and taxon-level attributes: Insect, Origin, Classification, Order, Family, Subfamily_tribe, Genus_species, Lifestage, CodeUnique, FFG, Habit, Tolerance, Voltinism, Seasonal, Drift, Size, Rheophily, Thermal.
- SFMR_Macro_Coordinates
  - Master keys and site metadata: ID, MasterSite, Trmt, Restoration, Width_Avg_ft, No_samples, GPS_bank, Lat_WGS84, Long_WGS84, Notes.
- SFMR_Macro_Samples
  - Temporal and environmental context per sample: River, OrigSite, Date, Transect, MasterSite, SiteYearSeason, Year, Season, Trmt, Post_mos, Post_Fire, Restoration, H_macro, H_micro, Cover_pct, Temp_C, Width_m, Depth_max_m, Depth_avg_m, SISA_pct, GR_pct, CO_pct, BO_pct, NonvascVeg_pct, EmergVeg_pct, AqVeg_pct, BMIwood_pct, Notes.
- SFMR_Macro_Species
  - Taxon- and abundance-level data: Year, Season, MasterSite, SiteYearSeason, Density, Biomass_mg, CodeUnique, Stage, Taxon_Wisseman.

## Sampling design and methodology
- Sites and samples
  - 17 sites (fall 2019), 12 sites (fall 2020), 10 sites (winter 2021); each site with 10 samples.
- Sampling protocol
  - 1 ft net samples along a transect across the river channel; ten samples per site, evenly spaced.
  - Pre-restoration transects marked; post-restoration sites identified via GPS due to stakes washing away (3–4 m error).
- Taxonomy and trait data
  - Macroinvertebrates identified to species or genus by Robert Wisseman; taxa traits drawn from an expert database.
  - Trait definitions provided in a dedicated traits file (SFMR_Macro_Traits).
- Measurements and processing
  - BMI samples standardized to 1 m2 of bethos; samples sorted and individuals measured (body length).
  - Temperature measurements: inconsistent USGS handheld readings; preferred temperature from USGS gauge near Cougar Dam upstream.
- Data structure and linking
  - Separate files for traits, coordinates, samples, and species; MasterSite and CodeUnique serve as linking keys.

## Data provenance and quality considerations
- Data quality notes
  - Temperature data inconsistently collected; cross-checked with USGS gauge data.
  - Post-restoration site identification affected by stake loss; GPS-based positioning introduces minor spatial error.
- Metadata and documentation
  - Clear definitions for column headers and units are provided across the four CSV files.
  - Dates for sampling are recorded in the SFMR_Macro_Samples dataset.

## Variables, units, and taxonomic traits
- Taxonomic scope
  - Insects and related aquatic taxa; recognition of origin (aquatic/terrestrial) and higher taxonomic classifications.
- Functional and ecological traits (SFMR_Macro_Traits)
  - Functional feeding groups (FFG), habit, tolerance, voltinism, seasonality, drift tendency, size, rheophily, and thermal tolerance.
- Measurement units
  - Density and Biomass reported per site per m2; Biomass in mg per m2; environmental covariates in percentages (e.g., cover_pct, substrate percentages).

## Restoration context and environmental covariates
- Restoration metadata
  - Restoration type and timing captured (Restoration, Post_mos, Post_Fire, restoration stage 0 activities).
- Environmental covariates
  - Canopy cover (Cover_pct), substrate composition (SISA_pct, GR_pct, CO_pct, BO_pct), vegetation cover (NonvascVeg_pct, EmergVeg_pct, AqVeg_pct), presence of BMIwood, and temperature (Temp_C).
- Site-scale context
  - 10 samples per site; includes spatial context (Width_ft, GPS_bank) and transect placement.

## Practical implications for data leadership and reuse
- Data interoperability
  - Well-structured, linked dataset with four CSVs and a dedicated trait definitions file; designed for cross-dataset integration via MasterSite and CodeUnique.
- User needs and governance
  - Provides comprehensive metadata for assessment of data quality, provenance, and applicability to wildfire/restoration impact studies.
- Limitations to consider in reuse
  - GPS positional uncertainty post-restoration and temperature data inconsistencies; users should account for these in analyses and document data provenance when sharing results.