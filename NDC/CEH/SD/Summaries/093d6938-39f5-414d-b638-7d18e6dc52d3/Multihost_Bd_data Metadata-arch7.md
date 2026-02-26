# Metadata for: MultihostBDdata.csv

## Overview
- Metadata for a mesocosm Bd infection experiment conducted in late summer 2017 at the Centre for Captive Breeding of Threatened Amphibians in Rascafría, Guadarrama Mountain National Park, near Madrid, Spain.
- Objective: determine how non-reservoir hosts influence maintenance and transmission of Batrachochytrium dendrobatidis (Bd) supported by reservoir hosts.
- System: amphibian community with a dynamic assemblage of ten co-occurring species; focus on salamanders as a seasonal Bd reservoir.

## Study site and background
- Location: Guadarrama Mountain National Park, Penalara Massif near Madrid, Spain.
- Key species: larval Fire salamanders (Salamandra salamandra) emphasized as a major Bd driver due to overwintering behavior, high infection prevalence, strong infectivity, and high survival when infected.
- Experimental aim: test hypotheses about the role of salamanders and other co-occurring hosts in Bd dynamics; not all hypotheses have been experimentally tested.

## Experimental design
- Host community treatments (five total):
  1) Control: 24 Salamandra salamandra (Ss) only
  2) Ss + Bufo spinosus (Bs): 12 salamanders + 12 toads
  3) Ss + Hyla meridiensis (Hm): 12 salamanders + 12 tree frogs
  4) Ss + Bs + Hm (non-random): 12 salamanders, 6 toads, 6 tree frogs
  5) Ss + Bs + Hm (random): 3-species composition with random relative abundances
- Tanks: 36 mesocosm tanks housing the experimental communities.

## Data collection and variables
- Data identifiers:
  - unique_ID: unique identifier for each datapoint
  - date: sampling date
  - tank_ID: identifier for the mesocosm tank
  - time_interval: sampling stage (initial, intermediate, final); salamanders sampled at all three; frogs and toads sampled only at final
  - sample_type: type of sample (swab, mouth clip, tail clip, toe clip, or analysis of a corpse)
  - treatment: one of the five treatment categories above
  - fate: ultimate outcome for the individual (euthanised, metamorphosed, or died)
  - infection_load: Bd DNA quantified as genomic equivalents
- Temporal scope: salamanders sampled at three time points; amphibians (frogs, toads) sampled only at final time point.

## Geographic/Spatial context for GIS
- Spatial coordinates not provided in metadata; study is within a specific national park site.
- GIS opportunities: link tank-level data to spatial layout of the mesocosm network within the Guadarrama site, map infection_load by tank and treatment over time, and integrate with environmental/contextual layers if coordinates or pond-network data are added.

## Data quality and considerations for GIS use
- Multi-species and multi-time-point data across five treatments require harmonization of resolutions.
- Some variables (e.g., sampling of non-salamander species only at final) introduce missingness that users should account for in spatial analyses.

## Potential GIS applications
- Visualize spatial distribution of Bd infection load across tanks and treatments over time.
- Compare infection dynamics between single-species and multi-species communities.
- Integrate with environmental or habitat data if spatial coordinates or site maps are linked.

## References
- Fernández-Beaskoetxea S, Bosch J, Bielby J. 2016. Infection and transmission heterogeneity of a multi-host pathogen (Bd) within an amphibian community.
- Bosch J, Fernández-Beaskoetxea S, Garner TWJ, Carrascal LM. 2018. Long-term monitoring of an amphibian community after climate change- and infectious disease-driven extirpation.
- Medina D, Garner T, Carrascal L, Bosch J. 2015. Delayed metamorphosis of amphibian larvae facilitates Bd transmission and persistence.
- Gabor C, Forsburg Z, Vörös J, Serrano-Laguna C, Bosch J. 2017. Differences in chytridiomycosis infection costs between two amphibian species from Central Europe.
- Hite JL, et al. 2016. Joint effects of habitat, zooplankton, host stage structure and diversity on amphibian chytrid.