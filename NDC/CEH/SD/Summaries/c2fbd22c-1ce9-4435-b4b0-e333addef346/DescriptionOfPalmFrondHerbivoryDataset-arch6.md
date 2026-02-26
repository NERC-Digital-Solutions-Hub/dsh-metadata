# Experimental design / sampling regime

## Overview
- Location: three oil palm estates in Riau Province, Sumatra, Indonesia (Pt Ivo Mas Tunggal): Ujung Tanjung (UTNE), Kandista (KNDE), Libo (LIBE).
- Experimental setup: 18 plots established in 2013 as part of the BEFTA project (Biodiversity and Ecosystem Function in Tropical Agriculture).
- Stand characteristics: UTNE and KNDE plots are mature/over-mature (planted 1987–1992); Libo plots replanted in 2014.
- Scale and design: each 50 x 50 m plot, with ~50 m from access tracks on three sides and ~1000 m from the fourth side; three sampling positions per plot at bearings 45°, 165°, and 285° from north.
- Sampling period: herbivory measured from 2013 to August 2017 (18 time points).
- Objective: quantify crown herbivory on oil palms and produce data suitable for analysis and visualization.

## Study area and plots
- Plots are arranged within estates in mature vs replanted configurations.
- Palm-level tracking: each palm is numbered; sampling positions are fixed at edge points around each plot.
- Data scope includes measurements from BEFTA core plots (2016–2017) and replanted plots.

## Sampling protocol
- For each plot, three palms were randomly selected for observation.
- Herbivory assessment process:
  - Visually estimate overall crown damage.
  - Chop down the 18th frond and collect it for analysis.
  - From the frond, collect 20 leaflets (in 10 pairs, evenly spaced) and photograph them consistently (same person, angle, board, and camera).
  - Rank leaflets by damage category (1 = no damage to 4 = heavy damage).
  - Record the number of leaflets per damage category.
- Image processing and damage calculation:
  - Photographs pre-processed to remove noise and converted to binary images using Fiji to measure total leaflet area.
  - Create a second image with all herbivory “filled in” to estimate consumed area.
  - Compute percent damage from photos (PercentDamagePhoto) as a proportion of the 20 leaflets’ total area.
- Observer consistency: a single observer performed photo work (A.D. Advento) to ensure consistency.

## Measurements and calculations
- Eye-based measures:
  - PercentTotalDamageEye: total crown herbivory as assessed by eye.
  - PercentFrondEye: herbivory on the 18th frond as assessed by eye.
- Photo-based measure:
  - PercentDamagePhoto: percent surface area of 20 leaflets consumed, derived from image analysis.
- Abundance data:
  - Abunclass: damage class for each line.
  - Count: number of leaflets in that damage class (out of 20).
- Proximity data (distance):
  - distance: recorded for palms within 20 m of focal palms at centers of ant-poison exclosures (July 2016–Aug 2017 inside 3 m radius and May 2017–Sept outside 2 m radius).
  - Note: data with a distance value should probably not be used for certain analyses due to exclosure effects.

## Data processing and quality control
- Basic data checks performed to identify impossible values.
- Validation: 50% of data entry cross-checked against original field sheets; error rate <1%.
- Corrections were recorded and retained with the dataset.

## Data structure and storage
- Format: three separate CSV files (comma-separated).
- Format type: thin/long format; each line represents a single observation; percentage data may be repeated across rows to represent different damage classes.
- Core fields (examples):
  - Estate_abbrev, Triplet, Plot, Treatment, Period
  - PalmNumber, Date
  - PercentTotalDamageEye, PercentFrondEye, PercentDamagePhoto
  - Abunclass, Count
  - distance
- Data separation:
  - BEFTA core plots: data from 2016–2017.
  - Replanted plots: separate dataset.
- Plot identifiers:
  - Mature stands: examples include plots with codes like C10, C11, D28, etc., and associated coordinates.
  - Replanted stands: examples include E, with corresponding plot numbers and designations.

## Data fields and units (key variables)
- Estate_abbrev: estate code (e.g., KNDE, UTNE, LIBE)
- Triplet: plot triplet identifier
- Plot: three-character plot ID (e.g., C01)
- Treatment: management since February 2014 (reduced, normal, enhanced)
- Period: discrete sampling period
- PalmNumber: palm identifier
- Date: observation date
- PercentTotalDamageEye: percentage of crown damage (eye-based)
- PercentFrondEye: percentage damage on the 18th frond (eye-based)
- PercentDamagePhoto: percentage damage from photo analysis
- Abunclass: damage class label
- Count: number of leaflets in that damage class
- distance: proximity to ant-exclosure (meters), with caveat for exclosure data

## Datasets and files
- BEFTA core plots dataset: data collected 2016–2017
- Replanted plots dataset: data from replanted stands
- Funding reference: NE/P00458X/1

## Miscellaneous and notes
- The dataset provides detailed metadata to support data reuse, including data collection methods, processing steps, quality checks, and field identifiers.
- The distance column indicates exclosure-related proximity and may limit use for certain analyses.

## Potential uses and caveats
- Suitable for analyzing spatial and temporal patterns of herbivory across estates, plantation histories (mature vs replanted), and experimental treatments.
- Useful for investigating effects of proximity to ant-exclusion experiments on herbivory measurements.
- When using distance data, exercise caution due to exclosure design; consider filtering to exclude affected observations.
- Ensure alignment of the long-format structure with analysis software and handle repeated percentage rows appropriately.