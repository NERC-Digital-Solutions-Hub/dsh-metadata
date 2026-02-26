# Macroinvertebrate data from the South Fork McKenzie River in Oregon, USA.

## Overview
- Purpose: Assess macroinvertebrate response to wildfire in restored and unrestored sites of the South Fork McKenzie River.
- Data type and size: Monitoring data (~140 KB) derived from BMI samples; density and biomass on a per-site basis; collected across multiple years/seasons.
- Data structure: Four separate CSV files (traits, coordinates, samples, species) that together describe organisms, sites, sampling events, and abundance metrics.
- Collection scope: 17 fall 2019 sites, 12 fall 2020 sites, and 10 winter 2021 sites, with 10 samples per site.

## Dataset structure and contents
- SFMR_Macro_Traits
  - Columns include: Insect, Origin, Classification, Order, Family, Subfamily_tribe, Genus_species, Lifestage, CodeUnique, FFG, Habit, Tolerance, Voltinism, Seasonal, Drift, Size, Rheophily, Thermal.
- SFMR_Macro_Coordinates
  - Columns include: ID, MasterSite, Trmt, Restoration, Width_Avg_ft, No_samples, GPS_bank, Lat_WGS84, Long_WGS84, Notes.
- SFMR_Macro_Samples
  - Columns include: River, OrigSite, Date, Transect, MasterSite, SiteYearSeason, Year, Season, Trmt, Post_mos, Post_Fire, Restoration, H_macro, H_micro, Cover_pct, Temp_C, Width_m, Depth_max_m, Depth_avg_m, SISA_pct, GR_pct, CO_pct, BO_pct, NonvascVeg_pct, EmergVeg_pct, AqVeg_pct, BMIwood_pct, Notes.
- SFMR_Macro_Species
  - Columns include: Year, Season, MasterSite, SiteYearSeason, Density, Biomass_mg, CodeUnique, Stage, Taxon_Wisseman.
- Trait definitions are provided for taxonomy, life stage, functional feeding groups, habitat preferences, tolerance, voltinism, seasonality, drift, size, rheophily, and thermal tolerance.

## Collection methodology
- Sampling: 1 ft net samples; 10 samples per site along a transect across the river channel, evenly spaced and selected by eye.
- Habitat notes: Filamentous algae not filtered from nonstock; BMI wood defined as samples within 1 ft of large woody objects.
- Pre/post restoration: Stakes used to mark transects pre-restoration; post-restoration sites identified primarily by GPS coordinates (3–4 m error).
- Taxonomy and traits: Robert (Bob) Wisseman identified macroinvertebrates to species/genus and assigned trait data from his database.
- Temperature data: USGS gage station near Cougar Dam used for temperature due to issues with handheld device measurements.

## Temporal and spatial coverage
- Sites and timing: 17 fall 2019 sites, 12 fall 2020 sites, 10 winter 2021 sites (each with 10 samples).
- Site layout: 10 samples per site; coordinates include MasterSite, bank position (LB/RB/Center), and transect details; additional site descriptors include restoration status, canopy cover, substrate type, and post-fire timing.

## Data quality, gaps, and governance considerations
- Data provenance and openness: Data organized in separate CSV files with consistent MasterSite naming and CodeUnique identifiers to link datasets; underlying data intended to be shared.
- Metadata and linkage: MasterSite and CodeUnique keys enable cross-dataset joins; coordinates and samples linked via MasterSite and time period.
- Uncertainties and limitations:
  - GPS-based site identification after restoration can have 3–4 m error due to faded stakes.
  - Temperature measurements inconsistent with handheld device; reliance on USGS gauge data for temperature.
  - Some metadata abbreviations and field definitions require reference to the trait definitions and dataset headers for full interpretation.
- Data governance: Emphasis on data quality assurance, transformation readiness, and clear presentation of findings; data sharing and metadata completeness are central to usability.

## Relevance for monitoring frameworks
- Policy and decision support: Provides site-level macroinvertebrate metrics (Density, Biomass) and trait-based data useful for evaluating wildfire impact, restoration effectiveness, and ecosystem recovery.
- Indicators and measures:
  - Community structure: species richness (via CodeUnique), density, biomass across sites and time periods.
  - Functional and trait-based insights: FFG, habitat preferences, tolerance, voltinism, and thermal sensitivity to inform resilience and vulnerability assessments.
- Data integration and governance: Demonstrates practical data management for monitoring frameworks, including data provenance, metadata standards, and sharing requirements across multiple datasets.

## Additional notes
- Data components are designed to be cross-referenced:
  - Traits provide taxonomic and ecological context.
  - Coordinates link site location and sampling design.
  - Samples capture temporal context, environmental covariates, and disturbance status.
  - Species records deliver abundance and biomass alongside life stage and taxon identity.