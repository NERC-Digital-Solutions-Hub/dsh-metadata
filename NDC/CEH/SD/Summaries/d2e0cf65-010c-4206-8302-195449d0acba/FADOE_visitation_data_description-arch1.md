# FADOE_visitation.csv

- Overview
  - Dataset documents Brassica nigra flower visitation frequencies by pollinating insects in 2018 and 2019 under Free-Air Diesel and Ozone Enrichment (FADOE) treatments.
  - Aims to enable analysis of how pollution treatments affect pollinator visitation rates and behaviors, with data suitable for correlation, model-based predictions, and interpretation within ecological contexts.

- Experimental design
  - Field setup: Brassica nigra grown in a wheat field; two field locations across years (2018 and 2019) for each ring.
  - Experimental units: rings (identified by Ring number) containing 6 adjacent plants as the observation unit.
  - Locations: each ring assigned to a location per year; rings moved to an adjacent field in 2019 (two locations per ring across years).
  - Treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and a control (CON; natural air).
  - Spatial rotation: for one week in 2019, rings rotated so control rings became diesel-polluted and ozone rings became combined treatment rings (and vice versa) to quantify spatial variation in pollinator foraging behavior.

- Observations and measurements
  - Observation unit details: 6 adjacent plants per ring; recorded plant count (No. of plants) and plant number (Plant no.).
  - Data collection: observer trained in insect identification recorded visits per observation unit for 5–10 minutes (start time, finish time, duration).
  - Flower counts: number of flowers present during observation.
  - Sampling schedule: Year and Date indicate sampling periodicity.

- Insect and visitation data
  - Insect counts: total counts and counts for specific pollinator groups (e.g., honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth) and additional groups (e.g., other fly, beetles, hemiptera, parasitic wasp, etc.).
  - Flower visitation data: number of flowers visited by each pollinator group (honey bee, solitary bee, bumblebee, hoverfly, butterfly, moth) and the corresponding average number of visits per insect.
  - Derived metrics: total insect counts, total flower visits, and visits per insect; insect counts per flower per hour and flower visits per flower per hour.
  - Time normalization: scaling of visitation data to account for number of flowers and sampling duration.

- Columns and data structure (high-level)
  - Core identifiers: Year, Date, Ring, Location, Treatment, Rotation, Recorder.
  - Temporal: Start time, Finish time, Duration.
  - Plant/flower context: Number of flowers.
  - Insect data: Counts by pollinator group; total counts; per-group visit counts.
  - Visitation metrics: Visits per insect; visits per flower; rates scaled per hour and per flower per hour.
  - Rotation indicator and spatial metadata to support spatial variation analyses.

- Temporal and spatial scope
  - Years covered: 2018 and 2019.
  - Field arrangement: rings with fixed positions within each year, moved between fields in 2019; one week of rotation implemented to assess spatial effects on foraging behavior.

- Analytical considerations for analysts
  - Assess effect of pollution treatments on visitation rates by pollinator group, using per-hour and per-flower rate metrics.
  - Compare responses across years and locations, accounting for the rotation design to separate treatment effects from spatial variation.
  - Use mixed-effects models or other appropriate statistical approaches to handle ring-level replication, year effects, and spatial structure.
  - Data preparation steps likely include cleaning, joining observation-level data to ring/location/treatment metadata, and computing derived rates (insect counts per flower per hour, etc.).

- Data quality, provenance, and limitations
  - Collected by trained insect observers with explicit observation durations and per-unit records.
  - Use of standardized observation unit and clear definitions of visits (landing or feeding attempt).
  - Potential limitations: limited temporal windows (5–10 minutes per observation), ring-based design with only two locations per year, and possible variability in field conditions across years and sites.
  - Rotation design partially mitigates spatial confounding, but cross-year comparability requires careful alignment of rings, locations, and treatments.