# Macroinvertebrate data from the South Fork McKenzie River in Oregon, USA

## Overview
- Purpose: Monitor macroinvertebrate response to wildfire across restored and unrestored sites.
- Data type: Monitoring; size ~140 KB.
- Structure: Four CSV files containing traits, coordinates, samples, and species data. Identified and collated by Bob Wisseman (Aquatic Biology Associates, Inc.).

## Dataset structure and files
- SFMR_Macro_Traits
  - Columns include: Insect, Origin, Classification, Order, Family, Subfamily_tribe, Genus_species, Lifestage, CodeUnique, FFG, Habit, Tolerance, Voltinism, Seasonal, Drift, Size, Rheophily, Thermal.
- SFMR_Macro_Coordinates
  - Columns: ID, MasterSite, Trmt, Restoration, Width_Avg_ft, No_samples, GPS_bank, Lat_WGS84, Long_WGS84, Notes.
- SFMR_Macro_Samples
  - Columns: River, OrigSite, Date, Transect, MasterSite, SiteYearSeason, Year, Season, Trmt, Post_mos, Post_Fire, Restoration, H_macro, H_micro, Cover_pct, Temp_C, Width_m, Depth_max_m, Depth_avg_m, SISA_pct, GR_pct, CO_pct, BO_pct, NonvascVeg_pct, EmergVeg_pct, AqVeg_pct, BMIwood_pct, Notes.
- SFMR_Macro_Species
  - Columns: Year, Season, MasterSite, SiteYearSeason, Density, Biomass_mg, CodeUnique, Stage, Taxon_Wisseman.

## Sampling and collection methodology
- Sampling approach: 1 ft net samples, 10 samples per site along transects across the river channel; samples equidistant, independent of transect length.
- Identifications: Macroinvertebrates identified to species or genus level; body length measured; taxa traits assigned from expert database.
- Special notes: 
  - Transects pre-restoration marked with stakes; post-restoration locations determined via GPS (3–4 m error expected after stakes washed away).
  - Temperature: USGS gauge temperature used due to handheld thermometer inconsistencies.

## Temporal and spatial coverage
- Sites and dates:
  - Fall 2019: 17 sites × 10 samples each.
  - Fall 2020: 12 sites × 10 samples each.
  - Winter 2021: 10 sites × 10 samples each.
- Spatial layout:
  - MasterSite labels include LB (left bank), RB (right bank), and Canter (center) of the site transect.
  - Coordinates include Lat_WGS84 and Long_WGS84 per MasterSite.

## Measurements and units
- Density: # per m2 (samples standardized to 1 m2 of benthic area).
- Biomass: mg per m2 (dry mass).
- Site- and time-specific fields include restoration type, post-restoration months (Post_mos), canopy cover (Cover_pct), substrate composition (SISA_pct, GR_pct, CO_pct, BO_pct), and various vegetative metrics.

## Data quality, limitations, and caveats
- Spatial precision limited by GPS errors after stake loss (3–4 m variance).
- Temperature data may be inconsistent due to measurement method; preferred data from USGS gauge near Cougar Dam upstream.
- Data integration spans multiple CSVs with domain-specific codes (e.g., MasterSite, Trmt, Restoration); ensure consistent joins across datasets.

## GIS use and integration guidance
- Core key for linking datasets: MasterSite (and SiteYearSeason for temporal joins).
- Spatial mapping:
  - Use SFMR_Macro_Coordinates for point locations (Lat_WGS84, Long_WGS84).
  - Map canopy and substrate context using Cover_pct, SISA_pct, GR_pct, CO_pct, BO_pct from SFMR_Macro_Samples.
  - Display post-fire/restoration context via Restoration, Post_mos, and Trmt fields.
- Trait-informed analyses:
  - Use SFMR_Macro_Traits to interpret functional ecology (FFG, Habit, Tolerance, Voltinism, Thermal) at the species level in SFMR_Macro_Species.
- Temporal analyses:
  - Track changes across pre/post restoration and wildfire events using Post_mos, Trmt, and Date (from SFMR_Macro_Samples).
- Output opportunities:
  - Map-based dashboards showing site-level densities/biomass by year/season.
  - Spatial comparisons of restored vs unrestored sites in relation to substrate and canopy cover.
  - Trait-enabled ecosystem function insights (e.g., sensitivity to warming, life histories).

## Potential applications
- Assess macroinvertebrate community responses to wildfire and restoration within the South Fork McKenzie River.
- Support policy discussions and public-facing GIS products with map-ready indicators of ecological change.
- Integrate with other spatial data (habitat, land use, climate) to analyze drivers of macroinvertebrate patterns.