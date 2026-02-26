# Soil Core Sample Metadata and Measurements Data Dictionary

## Overview
- Defines the fields and descriptions for soil core samples collected under a biochar amendment and moisture-treatment experiment.
- Captures identifiers, treatment conditions, sampling details, site characteristics, and a range of physicochemical properties measured or derived from the samples.

## Data fields

- soilcorenumber: Individual number given to the soil sample/core.
- biocharamendment: Is the sample un-amended or amended with biochar?
- wettedtreatment: Is the sample periodically wetted to a high water content or not?
- site: The field site in which the sample is located.
- depth: The depth of the soil sample from the soil surface.
- replicate: The replicate number of the soil sample from the same treatment.
- timesample: The time of the sampling.
- pH.water: The pH of the soil in water at a 1:2.5 ratio.
- total.C.percent: The total carbon content of the soil as a percentage.
- total.N.percent: The total nitrogen content of the soil as a percentage.
- CN ratio: The ratio of total carbon to nitrogen content in the soil.
- extract.nh4-n.mgkg: The extractable ammonium in the soil.
- extract.no3-n.mgkg: The extractable nitrate in the soil after the start of the incubation.
- drysoilweightg: The weight of the dry soil in the soil core in grams.
- gravwatercontproportion.before: The soil gravimetric water content as a proportion before the incubation started.
- bulkdensitygcm3.before: The bulk density of the soil before the start of the incubation.
- particledensitygcm3: The particle density of the soil.
- totalporosityproportionbefore: The total porosity of the soil before the start of the incubation (1 - (bulk density / particle density)).
- wfpsproportionbefore: The water filled pore space of the soil before the start of the experiment (gravimetric water content * (bulk density / total porosity)).

## Notes
- Derived fields:
  - totalporosityproportionbefore is calculated from bulkdensitygcm3.before and particledensitygcm3.
  - wfpsproportionbefore is calculated using gravwatercontproportion.before, bulkdensitygcm3.before, and totalporosityproportionbefore.
- The dataset integrates treatment (biochar amendment and wetted treatment), spatial and temporal identifiers (site, depth, replicate, timesample), and comprehensive soil chemistry and physics measurements for robust environmental health assessment.