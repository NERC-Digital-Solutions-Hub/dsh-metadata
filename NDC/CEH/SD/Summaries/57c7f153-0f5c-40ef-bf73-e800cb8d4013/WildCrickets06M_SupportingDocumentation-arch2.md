# SUPPORTING DOCUMENTATION:
Trade-off between reproduction and body maintenance in a wild field cricket ( Gryllus campestris ) population

## Overview
- A long-term field study (12 consecutive years) monitoring a Gryllus campestris population to understand trade-offs between reproduction and body maintenance.
- Data collected through standardized, high-volume observational methods (video, direct observations) and physiological sampling to enable comparative analyses over time.

## Study site and population
- Location: Asturias, North Spain; meadow on the northwest slope near an operational railway.
- Habitat: ~20,000 m2 meadow with adjacent meadows; mixed land use including meadows, orchards, eucalyptus, chestnut and oak patches.
- Population area: about 800 m2 within the meadow; crickets avoid shaded areas and areas with less solar gain.
- Monitoring period and management: 12-year continuity; mowing in mid-March and July-August; additional mowing between August and March; weekly burrow searches February–July.
- Species life cycle: Gryllus campestris is flightless, univoltine; overwinter as late instar nymphs; adults emerge in spring; eggs laid from early May; continuous activity through mid-summer; nymphal diapause and overwintering follow.

## Sampling regime
- Individuals trapped shortly after adult emergence; weighed (±0.01 g), photographed, and marked with a PVC tag for identification.
- Biological samples per individual: cuticular hydrocarbons, tiny haemolymph sample, and a small hind-leg tip.
- Monitoring infrastructure: 64–140 infrared cameras installed around burrow entrances from late April (pre-emergence) onward; cameras cover burrow vicinity and are rotated to maximize data coverage as crickets move between burrows.
- Recording period: cameras operate 24/7 from first adult eclosion until two consecutive inactive days; weather and environmental data collected continuously.

## Fieldwork and instrumentation
- Burrow tagging: each burrow assigned a unique identifier; direct observations supplement video data for burrows without cameras.
- Video storage and processing: DVR-based system with motion-triggered recording; software upgrades over time (Diginet to i-Catcher); video stored locally; data extracted and logged in spreadsheets and/or databases.
- Weather data: central meadow weather station with ten-minute intervals and seven buried surface sensors for microhabitat temperatures; all instruments factory-calibrated.

## Calibration and data quality
- Instrument calibration: all devices factory-calibrated; consistency checks performed during data processing.
- Quality control: post-processing queries (e.g., in MS Access) detect inconsistencies (e.g., same cricket appearing to use two burrows simultaneously); data not used until cleaned and validated.

## Analytical framework and data processing
- Data extraction occurs in two steps per day:
  - Step 1: identify burrow-usage vs. non-usage across multiple cameras (high-level pass).
  - Step 2: detailed review of selected cameras to log events; manual linking of events to a spreadsheet and subsequently to a database for downstream analysis.
- Per-year data assembly and quality checks precede analyses to ensure dataset integrity.

## Methodology specifics for key behavioral metrics
- Emergence date
  - Observation: adult emergence is highly synchronized; ~95% of males emerge within a two-week window each year.
  - Importance: marks transition from growth to reproduction; earlier emergence confers mating opportunities and offspring development time.

- Calling activity (male singing)
  - Measurement: per hour, for a 10-minute window, record whether a male is singing at least once.
  - Inclusion criteria: only days with five or more samples per male and with at least 24 samples per male overall are analyzed.
  - Purpose: quantify reproductive signaling effort.

- Searching activity
  - Measurement: assess burrow-visit durations as a proxy for mate-search intensity.
  - Transformation: binary classification of visits as short (≤ 77 minutes) or long (> 77 minutes) based on the population median; only solitary visits are included to avoid confounding by presence of others.
  - Interpretation: shorter visits indicate higher search frequency between burrows.

- Dominance in fights
  - Measurement: fights at burrows; assign win/lose status to both participants; each fight yields two data points (1 for the winner, 0 for the loser) tagged with the male’s age.
  - Importance: burrow occupation influences mating opportunities; dominance reflected in combat outcomes.

- Mating promptness
  - Measurement: latency from initial encounter to copulation; most matings occur quickly, but some exceed 40 hours.
  - Transformation: binary variable where ≤ 50 minutes is scored as fast mating (1) and > 50 minutes as slow (0).
  - Rationale: 50-minute threshold corresponds to time required to produce a new spermatophore and aligns with refractory periods observed in related species.

## Outputs and data stewardship
- Datasets and descriptive documentation are produced to enable cross-year comparisons and policy-relevant environmental analyses.
- Standardized data collection and processing pipelines support reproducibility and data sharing across research groups and monitoring programs.