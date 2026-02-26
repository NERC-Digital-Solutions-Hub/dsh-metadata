# HF_NW_herbage_yield.csv

## Overview
- This document supplements the data series documentation for CINAg experiments and details the HF_NW_herbage_yield.csv dataset.
- Contains 7 columns and 96 rows of herbage yield data from grassland fertiliser trials conducted in 2016 at two research stations: Henfaes (HF) and North Wyke (NW).
- Data origin: grassland fertiliser trials conducted at Henfaes Research Station (Bangor University) and North Wyke Research Station (Rothamsted Research).

## Dataset contents
- 7 columns representing field measurements and experimental factors.
- 96 rows corresponding to individual plot harvest observations.

## Experimental design and sites
- Sites:
  - HF: Henfaes Research Station
  - NW: North Wyke Research Station
- Trial design: randomized block design with blocks 1–4.
- Plot structure: plots 1–16 per site, each plot measuring 2 × 6 meters.
- Study year: 2016.
- Treatments compare different nitrogen fertilisers and a no-nitrogen control.

## Column definitions and units
- Date: Date of grass cut.
- Site: HF or NW indicating the trial location.
- N_app: Fertiliser application number (1, 2, or 3). 
  - 1st and 2nd applications each 90 kg N ha⁻¹; 3rd application 60 kg N ha⁻¹.
- Block: Blocking factor (1–4) of the randomised block design.
- Plot: Plot number harvested (1–16).
- Treatment: Fertiliser type
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (Agrotain)
  - C = 0 N control
- Dry_tonnes_ha: Yield in tonnes per hectare on a dry weight basis.

## Data provenance and purpose
- Dataset is intended to support environmental monitoring analyses by providing standardized yield responses to different nitrogen fertiliser treatments across two research sites.
- Serves as a structured data source for assessing environmental health and agricultural management performance over time when integrated with other data.

## Data handling and quality considerations for analysts
- Data should be verified, quality assured, cleaned, and transformed as part of standard monitoring workflows.
- Outputs likely to include reports, maps, and charts that compare yield responses by site, treatment, and date.
- Datasets should be stored and uploaded to appropriate data portals to facilitate long-term accessibility and reuse.

## Relevance to environmental monitoring challenges
- Facilitates cross-dataset value by enabling combination with other environmental data (e.g., soil, climate, or management data) rather than being used in isolation.
- Supports transparency and accessibility by providing underlying data that underpins final outputs.