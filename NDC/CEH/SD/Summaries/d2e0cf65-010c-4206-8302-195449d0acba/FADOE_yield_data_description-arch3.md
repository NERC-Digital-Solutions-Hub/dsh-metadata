# FADOE_yield.csv

## Overview
- Dataset of post-flowering yield characteristics for Brassica nigra under Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Collected over two years (2018 and 2019) across four pollution treatments: diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control (CON).
- Experimental design: two rings per treatment (8 rings total); plants sampled per ring (24 plants).

## Experimental design and sampling
- Rings placed in a wheat field in 2018; moved to an adjacent field in 2019 (coordinates provided for each year).
- Harvest workflow: when plants stopped flowering, moved to an insect mesh-covered polytunnel to mature before harvest.
- Measurements per plant: number of developed pods and undeveloped pods on the third raceme; percent pod development calculated.
- Pod sampling: ten random pods per ring bagged, dried at 70 °C, weighed; pod mass and seeds per pod calculated.
- Seed sampling: seeds removed from pods, counted and weighed; seeds per pod derived.
- Whole-plant measurements: aboveground dry mass measured; plants threshed to separate seeds; seeds counted and weighed.
- Derived totals: total seeds and total seed mass including pods.

## Data columns and metrics
- Core identifiers: Year, Ring, Treatment, Plant no.
- Pod development: No. developed pods, No. undeveloped pods, % pod development.
- Pod-level measurements: No. pods bagged, Mass of pods, Individual pod mass, No. seeds (pods), Seed mass in bagged pods.
- Plant-level measurements: Plant dry mass, No. seeds (plant), Seed mass (plant).
- Totals: No. seeds total (including seeds in pods), Seed mass total (including seeds in pods).

## Location, timing, and management
- 2018 field: field of wheat at lat/long 51.482853, -0.897749.
- 2019 field: adjacent field at lat/long 51.482374, -0.895855.
- Maturation step to limit insect damage via polytunnel.

## Relevance for monitoring frameworks
- Demonstrates end-to-end data capture from field exposure to multiple yield and reproductive metrics.
- Provides a structured set of variables (counts, masses, percentages) suitable for policy-relevant assessments of environmental pollutant impacts on crop yield and reproduction.
- Highlights the importance of metadata (treatment, year, ring, plant-level identifiers, measurement methods, units, and processing steps) for data reuse and governance.

## Data governance and usability considerations
- Clear documentation of measurement methods and units aids transparency and reproducibility.
- Public sharing of underlying data is facilitated by explicit metadata; attention needed to metadata completeness and provenance.
- Design supports comparison across treatments and years, informing future monitoring and decision-making on pollutant exposure effects.