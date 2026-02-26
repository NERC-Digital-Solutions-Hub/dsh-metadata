# Methane fluxes from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Objective and timeframe
- Methane flux measurements conducted during summers in 2013 and 2014.
- Comparisons among peatland plateau, thawing peatland features, and burnt vs unburnt forests in subarctic Canada.
- Site codes indicate locations, features, and replicates (e.g., TPP, TWM, T5M, TMID, FFU, FFB, WTP, WTM, WTS, WTW).

## Study areas and coding
- 2013 near Teslin (Yukon, Canada):
  - Peatland plateau: TPP (Teslin Peatland Plateau) with five replicates (TPP1–TPP5).
  - Thawing peatland plateau: TWM, T5M, TMID (each with three replicates: TWM1–TWM3, T5M1–T5M3, TMID1–TMID3).
  - Forest sites: FFU (FireFox Unburnt) and FFB (FireFox Burnt), each with five replicates.
- 2014 near Yellowknife (Northwest Territories, Canada):
  - Peatland plateau: WTP (White Truck Plateau) with five replicates.
  - Thawing features within White Truck: WTM (White Truck Moss), WTS (White Truck Sedge), WTW (White Truck Wetland).
    - WTM and WTS each with three replicates (WTM1–WTM3, WTS1–WTS3).
    - WTW: one feature with three replicates (WTW1–WTW3).
  - Boardwalks constructed to access thawing features and minimize disturbance.
- Spatial emphasis: coordinates referenced in file; data types include flux measurements and soil cores (different locations, GPS coordinates also provided).

## Sampling design and equipment
- Ground collars:
  - Diameter: 160 mm for peatland plateau and forest sites; 315 mm for thawing features.
- Chambers:
  - Height: 15–35 cm, PVC construction, matched to collar diameter.
  - Sealing and leakage prevention via inner tube.
- Gas measurement:
  - Methane determined with a Detecto Pak-Infrared (DP-IR) gas analyzer.
  - Tubing with shut-off connectors connected to the DP-IR; measurements taken over up to 4 hours at regular intervals.
  - Calibration: certified 100 ppm CH4 standard (Praxair); on-site DP-IR self-test checks; measurements within 2 ppm of standard.
- Headspace calculations:
  - Distance from collar edge to ground measured to compute headspace volume.
- On-site environmental data:
  - Air temperature (on-site weather station).
  - Soil temperature at 5 cm and 10 cm inside the collar.
  - Volumetric soil moisture at the surface (0–6 cm) using a ML3 ThetaKit with default calibration.
  - Thaw depth measured with a metal rod.
  - Water table depth measured relative to a datum using a long rod.
- Protocols:
  - Slopes of methane concentration vs. time used to estimate flux.
  - Intercept and R^2 of linear regression are reported.

## Data collected and variables
- Flux rates expressed as:
  - mg CH4 per day per m2.
  - mg CH4-C per day per m2.
- All measured variable units are provided in each column.
- Dataset links:
  - Flux data coded to match soil profiles dataset (though soil cores and flux measurements originate from different locations; GPS coordinates provided in the file).

## Data processing and quality assurance
- Flux calculation:
  - Based on the slope of CH4 concentration versus time from chamber measurements.
  - Regression intercept and R^2 are reported to indicate fit quality.
- Instrument calibration and checks:
  - DP-IR self-test and 100 ppm CH4 standard checks; results within 2 ppm of standard.

## GIS and data integration considerations
- Multiyear and multi-site dataset enabling spatial comparisons of methane flux across peatland plateaus, thawing features, and forest burn conditions.
- Coding system (TPP, TWM, T5M, TMID, FFU, FFB, WTP, WTM, WTS, WTW) supports linking flux data with corresponding environmental features.
- Coordinate data available, but flux data and soil core data may come from different locations; georeferencing and careful alignment are required.
- Environmental context (temperature, soil moisture, thaw depth, and water table) enhances spatial analyses and modeling of flux drivers.

## Practical notes for GIS use
- Use the site-feature-replicate codes to join flux measurements with environmental rasters/layers (e.g., peatland vs thawing features, burnt vs unburnt forests, seasonal climate layers).
- Be mindful of mismatched locations between flux data and soil core data when integrating layers; rely on GPS coordinates provided.
- Ensure consistent units across the dataset when mapping or performing comparative analyses.