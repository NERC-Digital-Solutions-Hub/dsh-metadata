# Soil biochemical measurements from saltmarshes of different ages on the Essex coast, UK 2011..

## Overview
- A chronosequence study of salt marshes on the Essex coast, comparing natural, restored, and breached sites aged 16 to 114 years since tidal restoration or breach.
- Aims to quantify soil physical and biochemical properties to understand how restoration age affects marsh soil development.

## What is included
- Measurements from 30 cm soil cores across natural, restored, breached salt marshes and adjacent fields on former marsh.
- Variables measured: bulk density, moisture content, pH, electrical conductivity, ammonium (NH4+), total oxidised nitrogen (NO3-), organic matter (loss on ignition), below-ground biomass (to 30 cm), soil carbon and nitrogen content.
- Sites span three restored marshes, six breached sites, natural reference marshes, and adjacent former-marsh fields.
- Sampling years: October 2011 ( main dataset); Tollesbury field samples July 2010; Barrow Hill, Wallasey Island, Brandy Hole field samples April 2017. No planned repeat sampling.

## Sampling and methods
- Field sampling: four sampling locations per salt marsh; three soil cores per location (4 cm diameter, 30 cm depth). Fields on former marsh had 2–6 locations.
- Lab analyses (for each core or composite): 
  - Bulk density, moisture content, pH (1:2.5 water suspension), EC (mS cm-1).
  - Organic matter by LOI at 375°C (16 h).
  - NH4+ and NO3- by 1M KCl extraction with colorimetric analysis.
  - Total soil C and N by combustion (CN analyser).
  - Below-ground biomass to 30 cm depth by washing, drying and weighing.
- Calibration: equipment calibrated per CEH Bangor laboratory practices.
- Data quality: results entered into spreadsheets; outliers checked.

## Data structure and formats
- File formats: CSV (two related data files mentioned).
- Dataset fields include: SiteName, SiteCode, BulkDensity, MoistureContent, pH, Conductivity, NO3-N, NH4-N, OrganicMatter, BelowGround, Carbon, Nitrogen, plus metadata about missing data.
- Dataset field descriptions distinguish between numeric data and textual descriptors; notes on missing data indicate samples lost or not analyzed for certain variables.
- Restored/breached site metadata include grid references (easting/northing) and “years since breach” to 2011; natural marsh references also provided with grid references.
- Special note: Northey Natural used as the natural reference for both Northey and Northey Island restored/breached sites.

## Site information and chronology
- Restored and breached sites with coordinates and ages:
  - Tollesbury, Orplands, NortheyMR, Barrow Hill, Ferry Lane (B), Wallasea Island, Northey Island, North Fambridge, Brandy Hole. Years since breach to 2011 range from 16 to 114 years.
- Natural marsh sites (reference) with their grid references:
  - Tollesbury Natural, Orplands Natural, Northey Natural, Barrow Hill Natural, Ferry Lane (B) Natural, Wallasea Island Natural, North Fambridge Natural, Brandy Hole Natural.
- Fields on former marsh with grid references:
  - Barrow Hill Field, Wallasea Island Field, Brandy Hole Field, Tollesbury Field.
- Northey Natural is specifically used as the natural reference marsh for both Northey and Northey Island restored/breached sites.

## Notable references and context
- Methods and calibration references:
  - Avery & Bascombe (1974) Soil Survey Technical Monograph No.6.
  - Ball (1964) LOI as a measure of organic matter and carbon in soils.

## Potential uses for analysis
- Compare soil chemical and physical properties across a chronosequence to assess restoration trajectory.
- Examine relationships between age since restoration/breach and organic matter, carbon/nitrogen stocks, and nutrient pools.
- Assess how below-ground biomass and soil moisture, pH, and salinity-related factors evolve with marsh recovery.
- Use natural marsh references to benchmark restoration outcomes and quantify deviation from natural conditions over time.
- Enable meta-analyses of marsh restoration effects on soil biogeochemistry at a local scale with explicit metadata (grid references and sampling dates).

## Data quality and limitations
- Single time-point data for most sites, with some supplementary sampling years; no planned repeat sampling.
- Some variables may have missing data due to sample loss or non-analysis.
- Data are provided as CSV with detailed site and variable descriptions, but users should ensure proper alignment of site codes when merging with other datasets.