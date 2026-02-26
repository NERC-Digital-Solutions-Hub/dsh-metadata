# Data description Beech tree ring data from hot and dry European distribution edges, 2019

## Overview
- Purpose: use the relationship between European Beech tree growth and environmental factors (including climate) to monitor and forecast drought-related declines in forest growth across Europe.
- Main measurements: inter-annual tree growth quantified via dendroecology (ring width).

## Sampling and sites
- 12 sites sampled in late 2019 across Bulgaria, Albania, Kosovo, and Spain.
- Sites chosen at lower elevational ends to represent hot and dry edge conditions of European Beech distribution.
- Metadata available for sites (see site_meta.csv).

## Data collected and metadata
- site_meta.csv: metadata for the 12 sites including latitude, longitude, elevation, and nearest town or village.
- At each site: minimum 15 standard canopy-level trees; two cores per tree.

## Processing and measurement methods
- Standard dendrology procedures followed for core preparation.
- Cores air-dried in a shaded, ventilated space; mounted onto carriers; sanded through grit series 80, 120, 300, 600, 1200.
- Cores scanned into 2400 PPI images for CDendro measurements with 0.01 mm precision.
- Cross-dating (virtual and statistical) performed; COFECH used to control cross-dating quality.

## Data structure
- 12 measurement files, one per site, containing ring width measurements for each core by year (units: mm, resolution: 0.01 mm).
- First column: year.
- Remaining columns: ring width measurements from each core.
- Tree core IDs: combination of site ID and tree ID; suffixes 'a' and 'b' denote the two cores from the same tree.
- Missing values indicated as NA.

## Intended analyses and uses
- Correlate tree growth with climate and environmental variables to assess drought impacts.
- Extend the European Beech Tree Ring Network (EBTRN) by filling climatic data gaps at edge sites.
- Develop and test predictive models of growth response to environmental factors.

## Considerations and notes
- Data at 12 sites with multiple cores per tree provides robust within-site replication but may still face limitations related to spatial coverage and missing years (NA).
- High-resolution measurements (0.01 mm) support fine-grained analyses but require careful alignment with corresponding climate data.
- Cross-dating quality control via COFECH enhances reliability of yearly ring-width records.