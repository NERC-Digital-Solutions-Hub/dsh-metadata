# Soil_samples_NWT_Yukon2019-2020.csv

## Overview
- Data on carbon (C) and nitrogen (N) content in permafrost soil samples from the Northwest Territories and Yukon, Canada, collected in 2019 and 2020.
- Collected by Julian Murton, Thomas Opel, and Steve Kokelj; CN analysis conducted by Nina L. Friggens with support from Joana ZaragozaCastells.

## Dataset Structure
- A single CSV file: Soil_samples_NWT_Yukon2019-2020.csv.
- Contains 14 columns describing CN content and related metadata for each soil sample.
- A companion Word document provides detailed descriptions of sampling locations, environments, procedures, and per-profile metadata.

## Sampling and Locations
- 14 soil profiles spanning three regions: East Channel (EC), Tuktoyaktuk (T), and Klondike (K).
- Four soil profile types represented: non-lake orthels, drained thermokarst-lake sediments, turbels, and yedoma deposits.
- Profiles numbered 1–14, with region codes (EC, T, K) and qualifiers HUS (Husky Slump) and CRB_S (CRB Slump) used for certain profiles.
- Locations include multiple riverbank and coastal bluff sites with precise coordinates provided for each profile.
- Sampling methods included soil pits, coring, and horizontal drill holes into thaw slumps.

## Sample Measurements and Content
- Each sample has associated depth below ground surface, collection date, and total sample mass.
- Carbon content (C) and nitrogen content (N) analyzed; results reported as percentages.
- Samples processed and CN measured in 2021, after freezing and storage at field stations prior to analysis.
- Descriptive notes accompanying samples indicate soil type, organic/mineral soil characteristics, ALT (active-layer thickness) values, and presence/absence of ground ice where observed.

## Analytical Methods and Quality Control
- CN analysis performed with a Thermo Scientific Flash 2000 Elemental Analyser.
- Sample preparation: thawed, homogenised; a ~10 g subsample oven-dried to constant weight; CN analysis performed on ground material.
- Quality control using EDTA standards at the start and as check standards every ten samples:
  - EDTA standard: ~9.59% N (±3% acceptable), ~41.1% C (±1% acceptable).

## Data Fields and Units (Nature and Units of Recorded Values)
- Sample identifiers (long form: year, sample number, location code, profile number).
- Geolocation: Latitude and Longitude (degrees, minutes, seconds).
- Depth below ground surface (meters).
- Date collected (dd/mm/yyyy).
- Total mass of sample (kg).
- Short description and interpretation of soil sample.
- Sampling method (e.g., pit, core, drill).
- Storage during fieldwork (e.g., frozen).
- C content (%)
- N content (%)
- Soil type and formation (e.g., orthel, turbels, HUS, CRB_S, loessal deposits).
- Active-layer status: AL, Pc (permafrost cryoturbated), Pnc (permafrost non-cryoturbated), with notes on cryoturbation or ground-ice features.
- ALT values where reported (in cm) from probing in the active layer or related horizons.

## GIS and Map-Data Implications
- The dataset provides precise geolocations and depth-resolved CN measurements suitable for:
  - Mapping spatial distribution of soil C and N across permafrost regions.
  - Visualizing relationships between CN content and soil type, permafrost status, and active-layer thickness.
  - Overlaying sampling sites with permafrost features, ground ice indicators, and geomorphic contexts (orthels, turbels, yedoma, thermokarst deposits).
- Useful for creating map-based data products to support policy, client, or public audiences interested in Arctic soil carbon and nutrient stocks.
- Note: dataset covers 14 profiles, a limited but detailed subset of broader regional variability; consider augmenting with additional sites for broader GIS analyses.

## Access and Documentation
- CN results are reported for each sample after laboratory processing (Exeter, 2021).
- A Word document accompanies the dataset with detailed site-level environmental context, sampling procedures, and per-profile metadata.
- For GIS projects, reference both the CSV and the accompanying documentation to interpret sampling context, units, and per-profile designations.