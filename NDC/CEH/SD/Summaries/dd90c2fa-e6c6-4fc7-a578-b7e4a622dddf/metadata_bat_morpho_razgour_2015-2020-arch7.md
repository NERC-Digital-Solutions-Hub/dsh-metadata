# Metadata for 'bat_morpho_razgour_2015-2020.csv'

## Overview
- Dataset of morphological and life history data collected 2015–2020 from three bat species: Barbastella barbastellus, Plecotus auritus, and Myotis escalerai.
- Geographically: England, Spain, and Portugal; part of a NERC IRF project.
- Purpose: study adaptive responses to climate change.

## Data scope
- Data presented in a single CSV file; empty cells denote missing values.
- Temporal span: 2015–2020.
- Spatial scope: captures at roosts, caves, foraging sites, and over small water bodies.

## Collection and generation methods
- Samples collected during bat captures: tissue (wing biopsies), blood, or fecal samples.
- Capture methods: mist nets and harp traps; bats held individually in cotton bags during processing.
- Non-target species released immediately; target species released at the site of capture after processing.

## Nature and units of recorded values
- Spatial coordinates: Latitude and Longitude in WGS84 decimal degrees, with a resolution of 10 km.
- Sex: F (female) or M (male).
- Age: Adults, Sub-adults, or Juveniles.
- Reproductive condition:
  - Females: Nulliparous, Pregnant, Lactating, Post-lactating, Nonreproductive.
  - Males: determined by position and size of the testes.
- Forearm: measurements in millimetres.
- BodyMass: measurements in grams.

## Quality control
- All measurements taken by the same experienced person.
- Data checked for outliers and anomalies.

## Details of data structure
- Three bat species included; data stored in a single CSV file.
- Empty cells indicate missing values.

## GIS-specific considerations
- Coordinates enable map-based visualizations of species distribution and life-history traits.
- 10 km coordinate resolution limits fine-scale localization in analyses.
- Data integration may require handling missing values and aligning species/traits across records.