# Experimental design:

## Overview
- Describes an experiment using intact soil-turf monoliths from a long-term grassland nutrient manipulation study (established 1995, Wardlow, Peak District NP, UK).
- Two grassland soil types: limestone grassland (CG2d) and acidic grassland (U4e), with contrasting horizons and rooting depth.
- Mesocosms built from monoliths and subjected to factorial treatments of nutrients and CO2, enabling map-based visualization of spatial and treatment-driven patterns in soil properties.

## Spatial scope and sampling design
- Locations: Wardlow (field site) and Bradfield Environment Laboratory (research station), Peak District NP, UK (similar climate, closely located, altitude ~350–390 m).
- Experimental units: mesocosms derived from soil monoliths, replicated across treatments.
- Data layers implied: mesocosm IDs with grassland type, depth segments, treatments, and CO2 level for map-ready attributes.
- Depth resolution: soil profile divided into increments (0–10 cm, 10–20 cm; A and B horizons in acidic grassland).

## Experimental treatments and CO2 enrichment
- Nutrient treatments (per mesocosm): 
  - 0N (control, deionised water)
  - P (phosphorus, 3.5 g m^-2 y^-1)
  - LN (low nitrogen, 3.5 g m^-2 y^-1)
  - HN (high nitrogen, 14 g m^-2 y^-1)
- CO2 treatments: ambient (A) or elevated (E, ~600 ppm during daylight).
- CO2 enrichment implemented with miniFACE rings; each ring paired with a control, maintaining 8 mesocosms per combination across grasslands.

## Soil collection and processing
- Sampling: annually in September–October from each mesocosm.
- Procedure: triplicate 2 cm diameter cores per mesocosm; for acidic grassland, samples separated into A and B horizons.
- Preparation: soils sieved (10 mm then 2 mm), roots removed, moisture content determined by oven-drying at 105°C.

## Measurements and data methods
- Microbial phosphorus (MBP) determination: chloroform fumigation-extraction.
  - Fumigated vs. non-fumigated soil extracts using 0.5 M NaHCO3 (pH 8.5); analysis by ICP-OES.
  - MBP calculated as difference between fumigated and non-fumigated extracts, divided by 0.4 (Brookes et al. 1982; Vance et al. 1987).
- Soil chemistry and physicals: Soil_P (extractable phosphorus), bulk density, and other variables recorded.
- Data structure and units (key fields):
  - Location, Description: Mesocosm unique ID
  - Year, Description/Units: Numeric year
  - Depth, Description/Units: 0–10 cm, 10–20 cm; depth increments as strings
  - Grass, Description/Units: Acid (acidic grassland) or Calc (limestone grassland)
  - Treat, Description/Units: P, 0N, LN, HN
  - Pair, Description/Units: Experimental block
  - CO2, Description/Units: A (ambient) or E (eCO2)
  - Position, Description/Units: Position within FACE ring
  - Soil_P,MBP,Bulkdensity: mg kg^-1 or g cm^-3 as specified

## Data quality, limitations, and notes
- Missing data: one non-fumigated sample missing, preventing MBP calculation for that plot.
- Some MBP values were negative and removed from the dataset.
- Data provenance: methods align with established MBP measurement protocols (Vance et al., 1987; Brookes et al., 1982), enabling reproducible GIS mapping and cross-study comparisons.

## Potential GIS applications and map products
- Create point layers for each mesocosm with attributes: grassland type, CO2 level, nutrient treatment, depth interval, and year.
- Generate raster or polygon layers showing spatial patterns of:
  - Soil_P and MBP across depth and treatments
  - Bulk density variations by grassland type and depth
  - CO2 treatment effects by treatment combination and grassland
- Enable layered visualization to compare limestone vs. acidic grasslands under different nutrient and CO2 regimes, across sampling years.
- Facilitate time-slice analysis by linking annual soil samples to map features, supporting trend detection and spatial correlation analyses.