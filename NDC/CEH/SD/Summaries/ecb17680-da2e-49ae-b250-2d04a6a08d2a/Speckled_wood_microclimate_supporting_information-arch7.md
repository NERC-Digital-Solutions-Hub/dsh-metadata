# WINTER AND SUMMER SPECKLED WOOD SURVIVAL AND PERFORMANCE

## Overview
- Examines winter and summer survival and larval performance of F1 offspring of wild-caught P. aegeria in the UK.
- Compares performance in woodland versus grassland habitats across multiple sites.
- Includes datasets on survival, development, body mass, growth, microclimate, host-plant quality, and cold tolerance.

## Experimental design and sites (spatial context)
- Adult butterflies collected in a woodland site near the northern range boundary (Bishop Wood, near Selby, North Yorkshire; grid SE53).
- Eggs laid on potted Poa pratensis in greenhouses; larvae moved to field pots near female capture sites.
- Winter experiment: 2 field sites (woodland Bishop Wood SE5533; grassland Wistow SE6035); 40 pots per site; 5–15 larvae per pot; pots buried with nets.
- Summer experiment: 6 field sites total (3 woodland: Bishop Wood SE5533; The Grange SE6957; Skipwith Common SE6637; 3 grassland: University of York Campus SE6150; Wistow SE6035; Skipwith Common SE6637); 7 pots per site in summer; 5 larvae per pot with maternal contributions split across treatments.
- Measurements aggregated at the pot level; development time recorded as weeks (winter) or days (summer); pupal mass and growth rate calculated at pupation.

## Data collected and key variables

### Winter survival and performance (Winter_survival_and_performance.csv)
- Habitat: W (woodland) or G (grassland).
- Female: code for the adult female contributing offspring to the pot.
- Alive: number pupated successfully.
- Dead: number that died during the period.
- Development time: average weeks from field placement to pupation (NA if none pupated).
- Pupal mass: average mass at pupation (mg; NA if none pupated).
- Growth rate: average mg per week (NA if none pupated).

### Summer survival and performance (Summer_survival_and_performance.csv)
- Habitat: W or G.
- Site: woodland sites (1 The Grange, 2 Bishop Wood, 3 Skipwith Common); grassland sites (1 University of York Campus, 2 Wistow, 3 Skipwith Common).
- Pot: pot code (uneven due to losses).
- Alive as larvae: surviving larvae at end.
- Alive as pupae: larvae that pupated.
- Dead: total deaths during period.
- Development time: average days from field placement to pupation (NA if none pupated).
- Pupal mass: average pupal mass (mg; NA if none pupated).
- Growth rate: average mg/day (NA if none pupated).

### Winter microclimate (Winter_microclimate.csv)
- Temperature data loggers placed 30 cm above ground; hourly readings.
- Logger identifiers coded by habitat and logger number; some loggers failed (uneven counts).
- Date and time included; temperatures in °C per logger.

### Summer microclimate (Summer_microclimate.csv)
- Similar structure to Winter microclimate data.
- Columns include habitat code (W/G), site code, and logger code; hourly temperature readings.
- Uneven logger counts due to failures.

### Summer host plant quality
- Potted grass water content (Potted grass water content.csv)
  - Habitat: W or G.
  - Site: woodland or grassland site code.
  - Pot: pot code.
  - Percentage water content: water content of grass from each pot (NA if pot lost).

- Wild grass water content (Wild grass water content.csv)
  - Habitat: W or G.
  - Site: woodland or grassland site code.
  - Sample: grass sample number within site.
  - Percentage water content: water content of nearby wild grass (NA if no grass nearby).

### Speckled Wood cold tolerance (Cold_tolerance.csv)
- Exposure temperature: -5 °C or -10 °C.
- Duration of exposure: days at respective temperature.
- Sample: grouping of 10 larvae per treatment.
- Immediate survival (%): alive 2 days after removal from cold.
- Successful pupation (%): pupated after exposure.
- Successful eclosion (%): emerged as adults.
- Development time (days): days from removal to pupation (NA if none pupated).
- Pupal mass (mg): average pupal mass (NA if none pupated).
- Growth rate (mg/day): growth rate from removal to pupation (NA if none pupated).

## Spatial and data considerations for GIS
- Data linked to precise OS grid references and site codes, enabling spatial mapping of habitat effects.
- Multi-season, multi-site design introduces varying sample sizes and potential data gaps (e.g., uneven pots, logger failures, NA values).
- Datasets vary in resolution (pot-level measurements vs. site-level microclimate) and require harmonization for integrated GIS analyses.

## Potential GIS analyses and usage
- Map spatial patterns of survival, development, and growth by habitat and site.
- Link microclimate data to larval performance to model microhabitat suitability.
- Assess host-plant quality gradients and their association with performance metrics.
- Incorporate cold-tolerance results to evaluate risk under thermal stress across sites.
- Combine with other GIS layers to explore habitat management implications for P. aegeria.

## Summary of data structure and integration notes
- Data comprise multiple interrelated CSV files, each with clear habitat/site/pot or sample identifiers and standardized metrics.
- Missing data are represented as NA; uneven sample sizes require careful preprocessing for comparative analyses.
- The dataset supports spatially explicit analyses of monarch-like butterfly ecology, habitat effects, microclimate influences, and stress tolerance under controlled conditions.