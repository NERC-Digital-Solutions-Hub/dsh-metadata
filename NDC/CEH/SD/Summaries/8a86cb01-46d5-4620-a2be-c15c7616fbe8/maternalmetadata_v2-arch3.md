# Metadata for 'Long-term multisite Scots pine trial, Scotland: mother tree, cone and seed phenotypes, 2007'

## Overview
- Documents phenotypes of Scots pine mother trees and their cones/seed from 21 populations across Scotland, used to establish a long-term multisite common garden trial at three nurseries/field sites.
- Data are organized into two files (MotherTraits and ConeSeedTraits) and linked by PopulationCode; include geographic, ecological, and trait measurements.

## Sampling design and populations
- 21 populations selected to represent the species’ native Scottish range, with three populations from each of seven seed zones.
- Ten seed trees sampled per population using a spatial protocol: around a central tree within a circle (~1 km diameter).
- Sampling pattern: nine predetermined random-direction points from the central point; distance stratified in ratio 1:3:5 to avoid over-sampling near the center.
- For smaller fragments where only a few conifer trees were present, sampling directions were maintained to cover the area, with inter-tree distances never less than 50 m.

## Measurements and traits
- Mother trees:
  - Recorded height and diameter at breast height (DBH).
  - Ten cones collected per mother tree; cone width and length measured before drying; cone weight measured after drying.
  - Seed assessments per cone: total seed weight, seed count, and percentage viability (viable seeds defined as having both a wing and an obvious seed).
  - Mean values calculated per mother tree across the 10 cones to control for maternal effects in progeny analyses.
- Progeny/cone data:
  - For each cone: number of cones (Cone), cone width (Wi), cone length (Le), cone weight (We).
  - Seed viability metrics: total viable seeds (SN), viable seed percentage (SV), weight of viable seeds (SW).

## Data files and schema
- Two primary data files:
  - ConeSeedTraits.txt
  - MotherTraits.txt
- Key columns and relationships:
  - PopulationCode (population identifier), Family (mother tree ID; linked to maternal progeny), Population (full population name), SeedZone (EC, N, NC, NE, NW, SC, SW).
  - Geographic and environmental context: Latitude, Longitude, Altitude, Aspect, Slope, Regeneration, SoilDepth (cm), SoilMoisture, Competition, HA (height of mother tree), DA (diameter at breast height).
  - ConeSeedTraits.txt includes: Cone (cone number), Wi (width), Le (length), We (weight), SN (viable seeds per cone), SV (viable seed percentage), SW (weight of viable seeds).
- Metadata details:
  - Units and descriptions provided for each field (e.g., Altitude in meters, SoilDepth in cm, SV as percentage, coordinates in decimal degrees).

## Data quality, governance and sharing
- Measurements include quality-control features: maternal trait means computed across cones to reduce within-tree variation.
- Rich metadata supports traceability, reproducibility, and data governance for monitoring frameworks.
- Data structure enables linkage across populations, seed zones, and individual mother trees, facilitating transparent reporting and reuse in ecological monitoring and policy evaluation.

## Relevance for monitoring frameworks
- Exemplifies robust field sampling design and multi-site phenotypic data collection for environmental health monitoring.
- Demonstrates how to capture genetic/phenotypic variation across regions and connect maternal traits to progeny performance in a long-term experimental context.
- Provides a clear data schema and metadata approach to support transparency, data reuse, and governance in monitoring programs.

## Limitations and considerations
- Sampling date: March 2007; data reflect a historical snapshot used to establish a long-term trial, with potential changes over time not captured here.
- The design aims to minimize bias (no trait-based selection of seed trees), but applicability to current conditions should consider temporal and environmental changes.
- While metadata is comprehensive, any practical monitoring use should assess data currency and context relative to current management goals.

## Practical implications for policy and management
- Supports understanding regional genetic and phenotypic variation to inform seed transfer and restoration strategies.
- Facilitates long-term monitoring of environmental and climatic influences on pine phenotypes through a well-documented, comparable dataset.
- Provides a model for documenting complex monitoring data with robust metadata and cross-referenced traits suitable for policy evaluation and decision-making.