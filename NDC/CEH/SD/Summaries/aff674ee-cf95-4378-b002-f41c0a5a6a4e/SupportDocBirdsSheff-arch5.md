# Experimental design/sampling regime

## Overview
- Dataset records bird species and counts across 10 green spaces in the Sheffield City Region.
- Data collected to assess whether exposure to nature/biodiversity influences mental well-being (NERC IWUN Project).
- 2775 observations in total, spanning three surveys in 2018, with standardized methods to support comparability and reuse.

## Sampling design and data collection
- Green spaces: 10 parks listed with precise coordinates.
- Transects: 6 pre-designated line transects per site, each 60 meters long; transects did not overlap.
- Surveys: 3 occasions per site (rep1: 6–22 Jun 2018; rep2: 27 Jun–10 Jul 2018; rep3: 11–18 Jul 2018).
- Timing: surveys conducted in the early morning (05:30–09:30).
- Observer protocol: single experienced ecologist walked transects, noting birds on either side within distance bands; binoculars used for distant sightings to validate identifications.
- Recording details: includes date, time, and site-specific data; all birds observed were recorded rather than a sample.

## Observations and data attributes
- Birds recorded by common name and BTOCode (British Trust for Ornithology code).
- Activity/behavior: ActivityCode (C = calling, F = in flight, P = present, S = singing) and a descriptive Activity.
- Location and transect: Site name and Transect number (1–6).
- Counts and timing: Date (DD/MM/YYYY), Time (HH:MM - HH:MM), No.Birds (count).
- Distance bands: 0–25 m, 26–50 m, 51–100 m for observations.

## Data structure and contents
- File: BirdsSheffAllReps2018.csv
- Columns (11 total):
  - VisitNo (1, 2, or 3)
  - BTOCode
  - BirdName
  - ActivityCode
  - Activity
  - Site
  - Transect (1–6)
  - Date (DD/MM/YYYY)
  - No.Birds
  - DistanceBand (0–25 m, 26–50 m, 51–100 m)
  - Time (HH:MM - HH:MM)

## Quality control and limitations
- Data checked for logical consistency by Ross Cameron.
- Potential for double-counting cannot be ruled out, though methodology is systematic; error potential considered constant across the dataset.
- No data exclusions; all observations included to preserve completeness.
- Data are derived from a single observer per survey, which aids consistency but may limit inter-observer variability assessment.

## Context, provenance, and usage considerations
- Context: Part of a broader project linking urban nature exposure to well-being, using accompanying social science and medical datasets for correlations.
- Provenance: Collected by Ms Riley (bird data) with interpretation by Drs Cameron and Brindley.
- Use considerations for data stewards:
  - Ensure metadata clearly documents the field methods, survey timings, and transect design to support reproducibility.
  - Confirm coordinate reference system for site coordinates and consider providing GIS-friendly formats if needed.
  - Maintain definitions for ActivityCode and DistanceBand to avoid ambiguity in downstream analyses.
  - Acknowledge limitations around potential double-counting and single-observer design when publishing derived metrics.