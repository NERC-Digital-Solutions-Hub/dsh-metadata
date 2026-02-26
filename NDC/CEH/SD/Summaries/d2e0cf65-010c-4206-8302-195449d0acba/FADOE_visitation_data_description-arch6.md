# FADOE_visitation.csv

## Overview
- A dataset of Brassica nigra flower visitation frequencies by pollinators in 2018 and 2019.
- Observations taken from pollinator visits to focal patches within FADOE rings across two locations.
- Includes counts by pollinator group, flower visitation, and derived rate metrics, with a rotation design to assess spatial effects.

## Experimental design and data collection
- Observation unit: a focal patch of 6 adjacent plants within a FADOE ring.
- Rings numbered (Ring) and observed in 2018 and 2019 at two locations (Location) per ring.
- Treatments (four): diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), and control (CON; natural air).
- Sampling details: observer trained in insect ID recorded over 5–10 minutes per unit (Start time, Finish time, Duration minutes).
- Flower counts recorded for each observation period.

## Locations and temporal structure
- 2018 field located at latitude 51.482853, longitude -0.897749; 2019 moved to adjacent field at latitude 51.482374, longitude -0.895855.
- Within each year, two rings per treatment (D, O3, D+O3, CON).
- Rotational design implemented for one week in 2019: control rings swapped with diesel rings and ozone rings swapped with D+O3 rings to quantify spatial variation in pollinator foraging behavior.

## Data collected and key variables
- Insect counts by pollinator group (e.g., honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth, etc.) across observation units.
- Flower visitation counts by selected pollinator groups.
- Derived metrics:
  - Visits per insect (per group)
  - Flower visits per insect
  - Total insect counts, total flower visits, and visits per unit time (scaled to insect counts per hour and flower visits per hour)
- Columns capture:
  - Ring, Location, Year, Date, Treatment, Rotation
  - Recorder, Start time, Finish time, Duration
  - Number of flowers, observation unit identifiers
  - Insect counts by group, flower visits by group
  - Aggregated metrics and scaled rates

## Pollinator groups and measures
- Groups tracked: honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth, plus several broader categories (e.g., total beetle, pollen beetle, ladybird, parasitic wasp, etc.).
- For six focal pollinator groups (honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth), per-unit flower visits and per-insect visit metrics are provided.

## Derived data products and potential analyses
- Per-ring, per-treatment, per-location, per-year summaries of:
  - Insect abundance by pollinator group
  - Flower visitation counts and rates
  - Insect counts and visitation rates scaled to time and flower abundance
- Self-service dashboards or reports enabling comparison across treatments, years, and locations.
- Data suitable for assessing effects of diesel exhaust and ozone on pollinator foraging behavior, including spatial variation via the rotation design.

## Data quality considerations
- Patchy data formats and multi-system access as part of the broader data environment.
- Rotational treatment and relocation introduce spatial variation that must be controlled for in analyses.
- Consistency in observation duration and accurate time records are essential for rate calculations.