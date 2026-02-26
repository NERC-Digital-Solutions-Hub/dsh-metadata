# Macroinvertebrate data from the South Fork McKenzie River in Oregon, USA. Lat/Long: 44.17, -122.30.

## Overview
- Monitoring dataset (size: 140KB) collected to assess macroinvertebrate responses to wildfire in restored and unrestored sites.
- Geographic context: South Fork McKenzie River, Oregon (latitude 44.17, longitude -122.30).
- Outputs: counts (density) per square meter and biomass (dry mass, mg/m2) for macroinvertebrates; specimens identified to species or genus; body length measured.
- Sampling timeline: fall (Sep/Oct) and winter (Feb); 17 sites in fall 2019, 12 sites in fall 2020, 10 sites in winter 2021; 10 samples per site.

## Data files and structure
- Four CSV files:
  - SFMR_Macro_Traits: taxa-level trait metadata (taxonomy, life stage, functional feeding group, habitat preferences, tolerance, voltinism, seasonal strategy, size, Rheophily, Thermal).
  - SFMR_Macro_Coordinates: site coordinates and contextual metadata (MasterSite, Trmt, Restoration, Width_ft, GPS_bank, Lat_WGS84, Long_WGS84, Notes).
  - SFMR_Macro_Samples: per-sample site data (River, OrigSite, Date, Transect, MasterSite, SiteYearSeason, Year, Season, Trmt, Post_mos, Post_Fire, Restoration, canopy/cover, Temp_C, depths, habitat percent cover, substrate categories, BMIwood_pct, Notes).
  - SFMR_Macro_Species: species-level results per MasterSite (Year, Season, MasterSite, SiteYearSeason, Density, Biomass_mg, CodeUnique, Stage, Taxon_Wisseman).
- Trait definitions included to interpret columns (e.g., Insect vs Non-insect; Origin; FFG; Habit; Tolerance; Voltinism; Seasonal strategy; Size; Rheophily; Thermal).

## Collection methodology
- Sampling method: 1-foot net, 10 samples per site along a transect across the river channel, evenly spaced by eye.
- Pre-restoration transects were stake-marked; post-restoration sites identified primarily by GPS coordinates (3–4 m error).
- Macroinvertebrates identified to species or genus by Robert Wisseman and given traits from the trait database.
- Temperature data: USGS gauge station near Cougar Dam used due to inconsistent handheld thermometer readings.

## Temporal and spatial coverage
- Sites and timing:
  - Fall 2019: 17 sites, 10 samples per site.
  - Fall 2020: 12 sites, 10 samples per site.
  - Winter 2021: 10 sites, 10 samples per site.
- Samples per site: 10; each sample associated with MasterSite, transect position (LB, RB, Center), and timing relative to restoration.

## Key variables and metadata
- Traits file includes: Insect, Origin (Aquatic, Terrestrial), Classification, FFG (functional feeding group), Habit, Tolerance levels (TolHigh, TolMod, IntHigh, IntMod), Voltinism (SV, UV, MV), Seasonal (fast/slow/nonseasonal), Drift characteristics, Size (sm, med, lg), Rheophily (lentic/both/lotic), Thermal (cold/cool-warm/warm).
- Coordinates file: MasterSite, Trmt, Restoration, Width_Avg_ft, GPS_bank, Lat_WGS84, Long_WGS84.
- Samples file: fields covering River, OrigSite, Date, Transect, MasterSite, SiteYearSeason, Year, Season, Trmt, Post_mos, Restoration, canopy cover, temperature, depth metrics, substrata (SISA, GR, CO, BO), vegetation cover, BMIwood_pct, and notes.
- Species file: Year, Season, MasterSite, SiteYearSeason, Density, Biomass_mg, CodeUnique, Stage, Taxon_Wisseman.

## Data quality and caveats
- Temperature data: USGS source used due to inconsistencies with handheld device.
- Spatial precision: post-restoration site identification relied on GPS with 3–4 m error after stakes were washed away.
- Data integration: separate files require careful joining by MasterSite, Year/Season, Trmt, and post_fire/restoration indicators to analyze restoration effects.

## How to use and potential outputs
- Suitable for comparing macroinvertebrate density and biomass across sites and time windows, pre- and post-restoration, and post-wildfire contexts.
- Can create self-serve dashboards or reports by linking coordinates, samples, species, and trait data (e.g., group taxa by FFG, tolerance, size, or habitat).
- Enables trait-based analyses (e.g., shifts in functional feeding groups or tolerance) to interpret ecological responses to restoration and wildfire.
- Opportunities for visualization: site maps, time-series of density/biomass, trait-based aggregations, and restoration effect sizes.

## Access and context notes
- Dataset comprises four CSV files totaling 140KB, designed for cross-site macroinvertebrate analysis with detailed trait and habitat metadata.