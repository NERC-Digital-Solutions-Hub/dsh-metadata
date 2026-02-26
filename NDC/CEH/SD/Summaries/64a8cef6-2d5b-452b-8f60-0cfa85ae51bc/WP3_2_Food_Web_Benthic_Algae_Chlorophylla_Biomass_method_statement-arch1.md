# WP3.2_Food_Web_Benthic_Algae_Chlorophylla_Biomass

- Data type: chlorophyll-a content and ash-free dry mass (AFDM) of benthic biofilm; recorded as means with standard deviations from up to 10 replicate samples per site per occasion.
- Form: quantitative metrics per site/date, with replicates and summary statistics.

## Sampling locations and times

- Sites: three chalkstream sites in the Wessex chalk area — Nine Mile River, River Till, and River Wylye — representing a gradient of landscape integrity.
- Sampling period: seven occasions for Wylye and Nine Mile River; five occasions for Till; conducted between October 2012 and October 2013.
  
## Data collection procedure

- At each site and occasion:
  - 10 flat stones collected from the stream bed within a 100 m survey reach.
  - A 25 x 25 mm area of the stone surface scrubbed with a toothbrush; dislodged material collected in a tray, including material from toothbrush bristles.
  - Tray contents decanted into labeled 200 ml bottles and frozen.
- In the lab:
  - Samples thawed and split into two aliquots.
  - Aliquot 1: chlorophyll-a determined after extraction in 90% cold acetone (24 h) and filtered through a Whatman GFC filter.
  - Aliquot 2: AFDM determined by filtration on a preweighed Whatman GFC filter, drying at 80°C (≥24 h), weighing, then incinerating at 560°C (8–12 h) and reweighing.
- Output: chlorophyll-a content and AFDM per unit area (mg m^-2) with associated counts.

## Purpose and interpretation

- Used to construct quantified food webs detailing fluxes of mass and nutrients among nodes.
- Monitoring of autotrophic resource standing stocks via stone scrapes.

## Data stewardship and responsibility

- Data collection, processing, interpretation, and management led by the Queen Mary University of London River Communities Group, under Dr J. Iwan Jones.

## Completeness and limitations

- Completeness: 7 occasions for Nine Mile River and Wylye; 5 occasions for River Till.
- Limitations: no sampling during salmonid breeding season (Dec–Mar) to avoid redd disturbance; two replicate chlorophyll-a samples from Nine Mile River in March 2013 not processed.

## Data quality and checks

- Followed standard laboratory procedures for chlorophyll-a (Lorenzen, 1967) and AFDM (Vernon, 1960).
- No formal QA procedure reported; final values checked for marked outliers (none found) prior to calculations.

## Data structure: columns and definitions

- RIVER_ID: unique river identifier
- SITE_ID: unique site identifier within each river
- RIVER_NAME: river name (OS map)
- SITE_NAME: site name
- NGR: National Grid Reference
- EASTING: OS Easting
- NORTHING: OS Northing
- SAMPLE_DATE: date of sampling
- Mean_Chla_mgperm2: mean chlorophyll-a content (mg m^-2)
- StdDev_Chla_mgperm2: standard deviation of chlorophyll-a content
- Chla_n: number of biofilm samples processed for chlorophyll-a
- Mean_AFDM_mgperm2: mean AFDM (mg m^-2)
- Std_Dev AFDM_mgperm2: standard deviation of AFDM
- AFDM_n: number of biofilm samples processed for AFDM

## References

- Lorenzen CJ, 1967. DETERMINATION OF CHLOROPHYLL AND PHEOPIGMENTS: SPECTROPHOTOMETRIC EQUATIONS. Limnology and Oceanography 12(2):343-346.
- Vernon LP, 1960. Spectrophotometric Determination of Chlorophylls and Pheophytins in Plant Extracts. Analytical Chemistry 32(9):1144-1150.