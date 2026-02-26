# Autotrophic and heterotrophic soil respiration fluxes from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Overview
- Study of CO2 respiration fluxes conducted in summers of 2013 and 2014 in subarctic Canada.
- Comparisons: peatland plateau vs thawing peatland features; unburnt vs burnt black spruce forests; included additional sites.
- Distinguishes autotrophic+heterotrophic vs heterotrophic respiration using ground collars and trenching to minimize root effects.
- Flux data are paired with site-specific environmental measurements and detailed site codes.

## Study sites and sampling design
- Site codes and what they represent:
  - FFU - FireFox Unburnt; unburnt black spruce forest
  - FFB - FireFox Burnt; burnt black spruce forest (1998)
  - BLF - BlackFox; black spruce forest
  - WHF - WhiteFox; white spruce forest
  - TPP - Teslin Peatland Plateau
  - TWMID - Teslin Wetland Mid; center of thawed peatland plateau
  - TWM - Teslin Wetland Margin; margin of thawed plateau
  - MCU - Mosquito Creek Unburnt; unburnt black spruce forest
  - MCB - Mosquito Creek Burnt; burnt black spruce forest
  - WTP - White Truck Plateau; peatland plateau
  - WTM - White Truck Moss; recently thawed peatland plateau with moss
  - WTS - White Truck Sedge; recently thawed plateau with sedge/moss
  - WTW - White Truck Wetland; older thawed feature
  - BCB - Boundary Creek Birch; birch forest
  - BCS - Boundary Creek Spruce; black spruce forest
- Measurement apparatus and setup:
  - Ground collars installed to partition heterotrophic vs autotrophic+heterotrophic respiration.
  - Heterotrophic collars: PVC collars buried up to thaw depth (up to ~40 cm); trenching performed to minimize autotrophic influence in many sites; some sites trenching conducted in previous years (2012–2013) or during the measurement summer.
  - Autotrophic+heterotrophic collars: PVC collars placed on the surface; edge sealed with putty to reduce leakage.
  - Replicates: 3–5 collars per site per respiration type.
  - Collar dimensions: typically 160 mm diameter x 5 cm (autotrophic+heterotrophic) or 45 cm depth (heterotrophic) for FFU, FFB, BLF, WHF, TPP, MCU, MCB, WTP, BCB, BCS; larger collars (315 mm diameter x 10–15 cm) for TWMID, TWM, WTM, WTS with 45 cm depth for heterotrophic measurements.
- Access and disturbance minimization: boardwalks constructed at thawing features.

## Measurement protocol
- Instrumentation:
  - CO2 fluxes measured with an EGM-4 Infrared Gas Analyzer (PP Systems).
  - For most sites, CPY-4 chamber mounted on collar to ensure dark conditions and prevent photosynthesis.
  - For thawing features (TWMID, TWM, WTM, WTS): PVC inner enclosures of 15–35 cm height used atop collars to minimize leakage; enclosure times usually ≤ 3 minutes.
- Data collection:
  - Concentrations recorded at regular intervals (typically every 10 seconds) during enclosure.
  - Flux rates estimated from the slope of CO2 concentration vs. time; intercept and R^2 reported when regression used.
  - Initial and final flux values compared; if substantially different, measurement restarted.
  - Repeats conducted when time allowed within a day.
- Environmental measurements:
  - Air temperature recorded on site.
  - Soil temperature measured at 5 cm and 10 cm inside collar after removing chamber.
  - Volumetric soil moisture determined at surface (0–6 cm) with ML3 ThetaKit.
  - Thaw depth measured with metal rod; distance to thaw front recorded.
  - Water table depth measured relative to a datum using a long rod inserted at season start.
- Flux reporting:
  - Flux rates reported as mg CO2 per day per m2 or mg CO2-C per day per m2.

## Data structure, coding, and integration notes
- Coding alignment:
  - Autotrophic and heterotrophic soil respiration flux codes align with the soil profiles dataset coding.
  - Flux data and soil core data originate from different GPS locations; coordinates are provided in the data files.
  - Example: soil profile information for core TPP1 does not spatially match the flux data for TPP1.

## Data quality, usability, and GIS considerations
- Data quality controls:
  - Repeated measurements when feasible; checks for instrument and enclosure integrity.
  - Disturbance-minimizing measures (boardwalks, trenching strategies) documented to aid spatial interpretation.
- GIS usability notes:
  - Rich, site-based spatial context with detailed environment variables (temperature, moisture, thaw depth, water table).
  - Critical to align flux measurement locations with corresponding spatial records, especially given the distinct locations for flux vs soil-core data.
  - Useful for map-based visualization of spatial patterns across peatland plateaus, thaw features, and forest types, with explicit metadata on measurement methods and site configurations.