# Saturated hydraulic conductivity, bulk density and soil organic carbon content from three paired upland woodland and grassland sites in northern England, July 2019-April 2021

## Overview
- Dataset compares woodland vs pasture soil properties to assess potential impacts of upland tree planting as part of natural flood management.
- Covers three paired sites in northern England, sampled between July 2019 and April 2021 (COVID-19 disruptions noted).
- Supported by the Natural Environment Research Council's NFM research programme.
- Key soil measures included: saturated hydraulic conductivity (Ksat), bulk density, and soil organic carbon (SOC).

## Key measures and units
- Saturated hydraulic conductivity (K) in metres per day
- Bulk density (BD) in grams per cubic centimetre
- Soil organic carbon (SOC) as a percentage of dry soil mass
- Mid-point soil depths in centimetres (5, 10, 15, 25, 35, 45 cm)

## Experimental design
- Three sites with woodland and adjacent grassland: 
  - JF (Jerusalem Farm): old mature deciduous woodland
  - MW (Midgelden woods): deciduous woodland ~15 years since planting
  - IF (Inchfield): newly planted deciduous woodland (<5 years)
- At each site: 10 sample points in woodland and 10 in grassland (60 points total)
- Random sampling within woodland and grassland; 20 m buffer from edges; adjacent grazing grassland (P) and woodland (T) areas
- Purpose: compare soil properties between woodland and pasture as an indicator of upland tree planting impacts

## Data collection and processing methods
- Bulk density rings (5.3 cm diameter) used to collect 5 cm long samples; depths: 2.5–7.5 cm, 12.5–17.5 cm, 22.5–27.5 cm, 32.5–37.5 cm, 42.5–47.5 cm
- Depth bin midpoints: 5, 10, 15, 25, 35, 45 cm
- Ksat measured with Eijkelkamp permeameter; samples saturated and readings taken for known hydraulic gradient
- Bulk density determined by gravimetric oven-drying at 105°C for 24 hours
- SOC determined by loss on ignition at 450°C for 5 hours; conversion factor 0.58 used (assuming 58% carbon in organic matter)
- Descriptive soil context provided (e.g., texture)
- Upper two depth levels’ SOC reported; dataset notes that SOC values can be converted back to organic matter if needed

## Quality control
- Adherence to Eijkelkamp permeameter manual for Ksat measurements
- Bulk density mass recorded to two decimal places
- SOC: random replicates for 10% of samples; if replicates within 10% agreement, mean used; otherwise a third replicate used and mean of three values recorded

## Data structure and contents
- Site codes: IF = Inchfield, MW = Midgelden, JF = Jerusalem Farm
- Depths: mid-point depth for each 5 cm bin
- Trees/Pasture: T = woodland, P = grassland
- Soil type: descriptive terms
- Variables recorded: Bulk density, Ksat, SOC% (and mid-point depth)
- Data units and precision: BD and SOC to two decimal places; Ksat in metres per day

## Temporal coverage and provenance
- Sampling conducted between July 2019 and April 2021
- COVID-19 disruptions affected processing timeline
- Data linked to NERC NFM programme and laboratory procedures at University of Leeds

## Relevance for monitoring frameworks
- Provides standardized soil health indicators (Ksat, BD, SOC) across woodland vs pasture, enabling policy evaluation of upland tree planting for flood management
- Clear metadata and data structure facilitates integration into monitoring dashboards and governance processes
- Demonstrates robust QA procedures and transparent measurement protocols essential for data governance and reproducibility
- Highlights practical challenges for monitoring efforts (gaps by depth, edge effects, data completeness) relevant to designing resilient monitoring frameworks

## Limitations and considerations for users
- Some depths lack data for certain sample points due to shallow soils
- SOC values rely on a single burning-temperature method with a standard conversion; users may apply alternative SOC/OC conversions if needed
- COVID-19 disruptions may affect the completeness and timing of data processing and release
- Metadata completeness is present, but users may still need to verify site-specific context when aggregating across sites