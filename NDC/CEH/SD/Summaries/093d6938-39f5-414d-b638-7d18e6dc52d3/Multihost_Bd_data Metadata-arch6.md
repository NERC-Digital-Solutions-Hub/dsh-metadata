# MultihostBDdata.csv

## Overview
- Dataset from a 2017 mesocosm experiment at the Centre for Captive Breeding of Threatened Amphibians (Rascafría, Spain) investigating how non-reservoir hosts affect maintenance and transmission of Batrachochytrium dendrobatidis (Bd) infections.
- Focuses on a dynamic amphibian community in Guadarrama Mountain National Park with 10 co-occurring species; salamander larvae identified as a key reservoir due to high infection prevalence and persistence.
- Data intended to support understanding of multi-host Bd dynamics and to enable exploration of host-community effects on infection load and transmission.

## Experimental context and design
- Setting: Mesocosm tanks (36 total) representing an amphibian community within a network of ponds.
- Species and hosts involved: Salamandra salamandra (salamanders), Hyla meridiensis (tree frogs), Bufo spinosus (spiny toads).
- Treatments (five levels):
  1) Control: 24 salamanders only (Ss control)
  2) Ss + Bs: 12 salamanders + 12 toads
  3) Ss + Hm: 12 salamanders + 12 frogs
  4) Ss + Bs + Hm: 12 salamanders, 6 toads, 6 frogs (non-random)
  5) Random: three-species composition with random relative abundances
- Sampling design: Salamanders sampled at three time points (initial, intermediate, final); frogs and toads sampled only at final interval.
- Objective aligned with assessing Bd infection dynamics across host community structures.

## Data structure and key variables
- unique_ID: Unique identifier for each data point.
- date: Sampling date for the data point.
- tank_ID: Identifier for the mesocosm tank (36 tanks in total).
- time_interval: Sampling stage (initial, intermediate, final) for salamanders; final interval for frogs/toads.
- sample_type: Method of sample collection (swab, mouth clip, tail clip, toe clip, or dead/corpse).
- treatment: Coded treatment label corresponding to the five experimental setups:
  - Ss control
  - Ss + Bs
  - Ss + Hm
  - Ss + Bs + Hm (non-random)
  - random (three-species random)
- fate: Outcome for the individual (euthanised, metamorphosed, or died during the experiment).
- infection_load: Bd DNA load measured as genomic equivalents (quantitative infection metric).

## Data quality and considerations
- Patchy sampling: Salamanders sampled at multiple time points; amphibians (frogs/toads) only at the final interval, leading to incomplete time-series for some taxa.
- Heterogeneous data sources: Multiple sample types and varying host species across treatments; requires careful harmonisation when combining datasets.
- Cross-study provenance: Data linked to published references on Bd infection dynamics and host interactions; designed to support integration with external datasets and literature.

## Potential data products and analyses (Data Support perspective)
- Dashboards or pivot tables to compare infection_load across treatments, time_intervals, and sample_types.
- Time-series visualisations for salamanders; end-point comparisons for frogs and toads.
- Data quality reports highlighting missingness by tank, time point, and species.
- Provenance documentation and data lineage diagrams to aid reuse and reproducibility.
- Summaries that link infection_load to treatment effects, enabling quick assessment of multi-host impact on Bd dynamics.
- Opportunities to integrate this dataset with external Bd-related datasets for broader meta-analyses.

## Data provenance and references
- Primary authors and affiliations:
  - Andy Fenton; David Daversa; Jaime Bosch; Celia Serrano; Andrea Manica; Trent Garner; affiliations across University of Liverpool, ZSL, CNIC Madrid, Parque Nacional de la Sierra de Guadarrama, Cambridge University.
- References (context for Bd dynamics and cross-host transmission):
  - Fernández-Beaskoetxea et al. 2016
  - Bosch et al. 2018
  - Medina et al. 2015
  - Gabor et al. 2017
  - Hite et al. 2016