# FADOE_yield.csv

## Overview
- Data describe post-flowering yield characteristics of Brassica nigra plants grown in Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Collected over two years (2018 and 2019) across eight rings (2 rings per treatment) under four pollution treatments: diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), and control (CON).
- Field locations shifted from 2018 to an adjacent field in 2019; rings house 24 plants each.
- Measurements include pod and seed counts and masses, plant dry mass, and derived metrics like pod development percentage and seeds per pod.

## Experimental Design and Collection
- Experimental unit: FADOE ring; each ring assigned to one of four treatments.
- Sampling details:
  - Two rings per treatment (eight rings total).
  - 24 plants per ring; plants selected and removed at end of flowering.
  - Maturation in an insect-mesh polytunnel before harvest.
- Measurements collected per plant/pod:
  - Developed and undeveloped pods; pod development percentage.
  - Pods bagged: count, mass of pods, mass of seeds in bagged pods, seeds per pod.
  - Seeds removed from pods, counted, and weighed.
  - Plant-level metrics: plant dry mass, seeds per plant, seed mass per plant.
  - Totals: total seeds (including seeds in pods) and total seed mass (including seeds in pods).

## Data Structure (Columns)
- Year
- Ring
- Treatment
- Plant no.
- No. developed pods
- No. undeveloped pods
- % pod development
- No. pods bagged
- Mass of pods
- Mass of seeds in bagged pods
- No. seeds (pods)
- No. seeds total (including seeds in pods)
- Seed mass total (including seeds in pods)
- Plant dry mass
- No. seeds (plant)
- Seed mass (plant)

## Spatial Context
- 2018 field location: field of wheat, lat 51.482853, lon -0.897749.
- 2019 field location: adjacent field, lat 51.482374, lon -0.895855.
- Ring data links yield measurements to specific field locations and years, enabling spatial analysis of treatment effects.

## Data Processing and Workflow
- Harvest sequence: tage plants after flowering, mature in polytunnel, harvest by measuring pods and seeds, and compute derived metrics.
- Pod and seed data used to calculate:
  - Pod development percentage
  - Seeds per pod
  - Seed counts and masses at pod and plant levels
  - Total seeds and total seed mass (including pods)
- Measurements are combined to produce a comprehensive per-ring and per-plant dataset suitable for GIS visualization and spatial analysis.

## GIS Applications and Considerations
- Map-ready data enable visualizations by ring, treatment, and year:
  - Choropleth maps of pod development, seeds per pod, or total seed mass by ring.
  - Temporal maps showing changes from 2018 to 2019.
  - Spatial overlays with environmental or pollution-layer data for exposure-response analysis.
- Useful for communicating treatment effects across space (fields) and time.

## Data Quality, Gaps, and Challenges
- Multiyear, multi-field dataset requires careful joins by ring, year, and treatment.
- Potential data standardization needs across measurements (pods, seeds, masses) to ensure consistency in GIS workflows.
- Variation in data sources and resolutions across years may necessitate data cleaning prior to map production.

## Relevance to GIS Specialists
- Provides a rich, spatially anchored dataset with multiple yield metrics across rings and treatments.
- Suitable for creating insightful map-based data products that communicate spatial patterns and treatment effects to policy colleagues, clients, or the public.