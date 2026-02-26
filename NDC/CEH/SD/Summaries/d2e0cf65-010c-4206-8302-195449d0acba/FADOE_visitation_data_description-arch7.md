# FADOE_visitation.csv

## Overview
- Dataset of Brassica nigra flower visitation frequencies by pollinating insects for 2018 and 2019.
- Observations taken from FADOE rings subjected to pollution treatments: diesel exhaust (D), ozone (O3), diesel+ozone (D+O3), and control (CON).
- Each ring includes a focal patch of 6 adjacent plants with counts of insect visits and flower visits, plus flowers counted during observation.
- Data collected by an insect-identification trained observer for 5–10 minutes per observation period.
- Spatial component: rings located in two fields/locations across years, enabling spatial and treatment variation analyses.
- Rotation in 2019 swapped treatments among rings for one week to quantify spatial effects.

## Spatial and Temporal Coverage
- Years: 2018 and 2019.
- Locations: each ring has two locations (Location column C) corresponding to two field positions; fields were wheat fields at two coordinates:
  - 2018: latitude 51.482853, longitude -0.897749
  - 2019: latitude 51.482374, longitude -0.895855
- Ring-level layout: rings numbered (Ring column B) with fixed positions within a year; one-week rotation in 2019 changed treatments among rings.
- Observation timing: Year (A) and Date (F) indicate sampling periods; Start time (K), Finish time (L), and Duration (M) detail observation windows.

## Experimental Design and Treatments
- Treatments within each year: four pollution treatments
  - D (diesel exhaust), O3 (ozone), D+O3 (diesel exhaust + ozone), CON (natural air control)
- Replication: two rings per treatment per year (i.e., multiple rings per treatment/year).
- Rotation: in 2019, ring positions/treatments rotated for one week to assess spatial effects on pollinator foraging behavior.

## Data Collected (Key Variables)
- Observation unit details: 
  - Number of plants (No. of plants; Column I), Plant number (Plant no.; Column H)
  - Ring (Column B), Location (Column C), Treatment (Column E), Year (Column A), Date (Column F)
  - Observation timing: Start time (K), Finish time (L), Duration (M)
  - Flowers observed in the period (Number of flowers; Column N)
- Insect visitation data by pollinator group (counts):
  - Honey bee, solitary bee, bumblebee, hoverfly, other fly, butterfly, moth, total beetle, pollen beetle, ladybird, other beetle, hemiptera, parasitic wasp, unknown insect
  - Columns: O, R, U, X, AA, AB, AE, AH, AI, AJ, AK, AL, AM, AN
- Flower visitation by group (counts):
  - Honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth
  - Columns: P, S, V, Y, AC, AF
- Averages per insect group (per observation unit):
  - Columns: Q, T, W, Z, AD, AG
- Totals and derived metrics:
  - Total insect counts (AP), total flower visits (AQ), visits per insect (AR)
  - Insect counts per flower per hour and flower visits per hour (scaled by flowers and time) across additional columns up to BI
- Rotation indicator:
  - Rotation (Column D) notes when treatments/rings were swapped in 2019

## Derived Metrics and GIS Relevance
- Normalized visitation metrics:
  - insect counts per flower per hour
  - flower visits per flower per hour
- These enable spatial comparisons of pollinator activity by treatment and across the two field locations.
- Spatially-aware design allows assessment of treatment effects while accounting for location-based variation.

## Data Structure and Integration Considerations
- Data stored in a CSV with numerous per-observation fields and derived metrics.
- Spatial integration opportunities:
  - Use Ring ID, Year, and Location to link to GIS point features for ring positions.
  - Incorporate coordinates from Location fields to map rings in each year.
- Temporal integration opportunities:
  - Use Year, Date, Start/Finish times to create time-sliced maps or time series of visitation rates.
- Rotation complicates direct year-to-year comparisons; analyses should account for the 2019 treatment rotation.

## Potential GIS Analyses and Use Cases
- Map rings by location and visualize treatment distribution across the two years.
- Create choropleth or point maps of visitation rates by pollinator group, treatment, and year.
- Assess spatial variation in visitation due to pollution treatments while controlling for ring location.
- Analyze changes in visitation patterns over time, leveraging the rotation design to separate spatial vs. treatment effects.
- Combine with field polygons or habitat layers to study habitat context around rings.

## Notes and Data Quality Considerations
- Observations rely on a trained recorder, with standardized sampling durations.
- Two locations per ring across years require careful alignment when aggregating data by ring and year.
- One-week rotation in 2019 introduces a designed spatial swap; analyses should document this when interpreting treatment effects.