# Methane fluxes from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Overview
- Longitudinal dataset of methane flux measurements collected during two summers (2013 and 2014) across peatland plateaus, thawing peatland features, and burnt/unburnt forests in subarctic Canada.
- Aims to compare methane fluxes between plateau vs thawing features and between burnt vs unburnt forest sites (burnt/unburnt data collected only in 2013; 2014 lacks burn-related forest measurements).
- Includes site-level structuring codes, replicate design, and comprehensive environmental context to enable data integration and comparison.

## Study design and sites
- 2013 measurements near Teslin (Yukon) and ~100 km north of Whitehorse (Yukon), plus adjacent forest sites (FireFox): 
  - Peatland plateau: TPP (Teslin Peatland Plateau) with five replicates/collars (TPP1–TPP5).
  - Thawing peatland plateau: three locations within thawing feature (TWM, T5M, TMID) each with three replicates (e.g., TWM1–TWM3, T5M1–T5M3, TMID1–TMID3).
  - Forest sites: FFU (FireFox Unburnt) and FFB (FireFox Burnt) with five replicates each.
- 2014 measurements near Yellowknife (Northwest Territories) at White Truck site:
  - Peatland plateau: WTP (White Truck Plateau) with five replicates (WTP1–WTP5).
  - Within-plateau thawing features: WTM (Moss), WTS (Sedge), WTW (Wetland); each feature had three replicates, except WTW with a single feature and three replicates.
  - No burn vs. unburnt forest measurements in 2014.
- Data collection access methods:
  - Boardwalks constructed to access thawing features and minimize disturbance.
  - Location coordinates referenced for flux and soil data (GPS coordinates provided in the dataset files).

## Data collection methods and instruments
- Flux measurement setup:
  - Ground collars made of PVC (160 mm diameter for plateau/forest; 315 mm for thawing features).
  - Chambers (15–35 cm high, matching collar diameter) placed on collars; inner tube used to seal and prevent leakage.
  - Methane concentration measured in chamber headspace with a Detecto Pak-Infrared (DP-IR) analyser; connected via two Tygon tubing lines with shut-off connectors.
  - Calibration and QA:
    - DP-IR includes automatic self-test; certified gas standard (100 ppm CH4) used to verify performance (within 2 ppm of standard).
  - Data collection:
    - CH4 concentration tracked over up to 4 hours at regular intervals; time-stamped measurements recorded.
    - Chamber collar ground distance measured to compute headspace volume.
- Flux calculation:
  - Flux estimated from the slope of CH4 concentration versus time (linear regression); intercept and R² also reported.
  - Flux rates expressed as:
    - mg CH4 per day per m²
    - mg CH4-C per day per m²
- Environmental and site context measurements:
  - Air temperature measured on site.
  - Soil temperature recorded at 5 cm and 10 cm inside the collar after removing the chamber.
  - Volumetric soil moisture measured at the surface (upper 6 cm) using an ML3 ThetaKit with default calibration.
  - Thaw depth measured with a metal rod (depth until resistance encountered).
  - Water table depth measured within thawing features relative to a datum established at season start using a long rod.
- Data notes:
  - All measured variables include units in their respective columns.
  - The dataset coding for methane fluxes aligns with the soil profiles dataset; however, soil core and flux data originate from different locations (GPS coordinates provided in the file).

## Data structure, coding, and variables
- Coding schemes:
  - Peatland plateau: TPP (Teslin Peatland Plateau), WTP (White Truck Plateau).
  - Thawing features: TWM, T5M, TMID (2013) and WTM, WTS, WTW (2014 within White Truck).
  - Forest sites: FFU (FireFox Unburnt), FFB (FireFox Burnt) – 2013 only.
- Replicate structure:
  - 2013: TPP1–TPP5; TWM1–TWM3, T5M1–T5M3, TMID1–TMID3; FFU1–FFU5, FFB1–FFB5.
  - 2014: WTP1–WTP5; WTM1–WTM3, WTS1–WTS3; WTW1–WTW3.
- Data alignment and notes:
  - Methane flux data codes are designed to be consistent with the soil profiles dataset, enabling cross-dataset integration.
  - Location and dataset-specific GPS coordinates are provided in the data files; temporal coverage is limited to summers 2013 and 2014.

## Quality, limitations, and considerations for reuse
- Measurement duration variability:
  - Flux calculations rely on linear regression over measurement periods; maximum duration up to 4 hours, potentially impacting slope stability for highly variable fluxes.
- Burned vs. unburned forest data:
  - Burn-related comparisons are available only for 2013; 2014 lacks burn status data, which may affect cross-year comparisons for forest conditions.
- Data integration notes:
  - Soil core data and methane flux data come from different locations within the same sites; refer to GPS coordinates in the dataset to align records accurately.
  - All measurements include on-site environmental context to support covariate analyses and reproducibility of flux calculations.