# BirdsSheffAllReps2018.csv

## Overview
- A CSV dataset of bird species and counts recorded across 10 green spaces in the Sheffield City Region.
- Part of the NERC IWUN project examining links between urban nature and well-being.
- Contains 2775 observations; data linked to emotions/feelings collected via a mobile app.

## Experimental design and sampling regime
- Sites: 10 parks/green spaces (listed with coordinates in the data documentation).
- Temporal structure: three survey repetitions (rep 1: 6–22 June 2018; rep 2: 27 June–10 July 2018; rep 3: 11–18 July 2018).
- Daily timing: surveys conducted in the early morning (05:30–09:30).
- Sampling design: 6 pre-designated line transects per site (transects 1–6), each 60 meters long; transects within a site are non-overlapping and cover different habitats (stratified sampling).
- Observers: a single experienced ecologist conducted all surveys; binoculars used to verify distant sightings.

## Data collection and recorded variables
- Observations: birds recorded by common name and British Trust for Ornithology (BTO) code.
- For each observation: date, time, site, transect, distance band, activity context, and count.
- Distance bands: 0–25 m, 26–50 m, 51–100 m.
- Activities recorded: coded (C = calling, F = in flight, P = present, S = singing) and described in an Activity field.
- Data source: part of the IWUN project; data used alongside social science/medical datasets for correlations with well-being outcomes.
- Data quality: one ecologist ensured consistency; potential for double-counting acknowledged but considered consistent due to systematic methodology.

## Collection/Generation/Transformation methods
- Locations (with coordinates) for each surveyed green space are provided in the dataset.
- Data file: BirdsSheffAllReps2018.csv.
- Structure: 11 columns capturing visit, taxonomy, behavior, site, transect, date, counts, distance band, and time.

## Quality control
- Data sheet checked by Ross Cameron to ensure logical consistency.
- No explicit deduplication; the methodology is systematic, so any potential counting overlap is presumed uniform across the dataset.

## Data structure and contents
- File: BirdsSheffAllReps2018.csv
- Columns (11):
  - VisitNo: visit number (1, 2, or 3)
  - BTOCode: BTO code for the species
  - BirdName: common name
  - ActivityCode: activity code (e.g., C, F, P, S)
  - Activity: described activity
  - Site: park/site name
  - Transect: transect number (1–6)
  - Date: observation date (DD/MM/YYYY)
  - No.Birds: number observed
  - DistanceBand: observation distance band (0–25 m, 26–50 m, 51–100 m)
  - Time: observation time window (HH:MM–HH:MM)
- Each row represents an individual species observation with associated metadata.