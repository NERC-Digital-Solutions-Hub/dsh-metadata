# FADOE_yield.csv

## Overview
- Dataset of post-flowering yield characteristics for Brassica nigra under Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Collected over two years (2018 and 2019) in fields near coordinates provided for each year; fields moved from 2018 to an adjacent field in 2019.
- Experimental design: 4 treatments (diesel exhaust D; ozone O3; diesel exhaust + ozone D+O3; control CON) with two rings per treatment (total 8 rings).
- Each ring contained 24 plants. Plants were harvested after flowering, matured in a protective polytunnel, and yield components were measured, including pod development, seed counts, and biomass.

## Experimental design and collection
- Rings allocated to treatments (2 rings per treatment).
- Field locations changed between years (2018 field then moved to adjacent field in 2019).
- Post-flowering harvesting with maturation in an insect mesh-polytunnel to prevent additional damage.
- Measurements include pod development, seed counts/weights, and plant biomass, with pod-level and plant-level data collected.

## Data structure and key variables
- Year: 2018 or 2019.
- Ring: ring identifier (per treatment).
- Treatment: D, O3, D+O3, CON.
- Plant no.: 1–24 per ring.
- No. developed pods: count per plant.
- No. undeveloped pods: count per plant.
- % pod development: derived metric per plant.
- No. pods bagged: number of pods sampled for pod/seed analyses (ten random pods noted per plant/task).
- Mass of pods: total mass of bagged pods (processing details include oven-drying at 70 °C).
- Mass of seeds in bagged pods: mass of seeds from the bagged pods.
- No. seeds (pods): seeds counted from pod samples.
- Mass of seeds in bagged pods: weight of seeds from bagged pods.
- Plant dry mass: above-ground dry weight of the whole plant.
- No. seeds (plant): seeds counted from the plant after threshing.
- Seed mass (plant): seed mass from the plant.
- No. seeds total (including seeds in pods): total seeds per plant (pods + plant).
- Seed mass total (including seeds in pods): total seed mass per plant (pods + plant).
- Mass of seeds in bagged pods, Mass of pods, Mass of individual pod: additional mass-related measurements relevant to yield components.
- No. seeds (pods) and No. seeds per pod: pod-level seed counts and average seeds per pod.

Note: Some mass-related fields do not have explicitly stated units in the description; typical practice would be grams, but units are not specified in the provided text.

## Processing and measurements
- Pods: ten random pods per plant were bagged from adjacent racemes for measurement.
- Pods and seeds: oven-dried (pods) and weighed; seeds counted and weighed.
- Whole plant: dried and threshed to separate and count seeds; seeds weighed to obtain plant-level seed mass.
- Derived metrics include percent pod development, seeds per pod, and total seed counts/masses.

## Spatial and temporal context
- Two-field arrangement across years with explicit coordinates for each year.
- Yearly field relocation indicates cross-year experimental consistency and potential spatial effects to consider.

## Data quality and governance considerations
- Metadata provides definitions for columns and the measurement protocol, supporting data lineage.
- Potential gaps to address for robust governance:
  - Confirm and standardize units for all mass measurements.
  - Ensure complete metadata on data provenance and any data preprocessing steps.
  - Document any missing values or exceptions in measurements.

## Implications and uses for Data Leaders
- System-wide data perspective: multi-year, ring- and treatment-level yield components enable cross-field and cross-year analyses.
- User needs alignment: supports researchers and policy-facing colleagues interested in environmental treatment effects on crop yield components.
- Data stewardship opportunities:
  - Preserve and link to detailed metadata (units, processing steps, field coordinates).
  - Maintain data discoverability and versioning; integrate with broader data ecosystems for cross-network reuse.
  - Establish data standards for mass and count fields to facilitate integration with other datasets.

## Potential analyses and applications
- Evaluate treatment effects (D, O3, D+O3, CON) on pod development, seed yield, and overall plant productivity.
- Decompose yield into components (pods vs seeds, pod development rate, seed mass) across years and fields.
- Inform agronomic models and policy-related assessments of environmental pollutant exposure on crop performance.