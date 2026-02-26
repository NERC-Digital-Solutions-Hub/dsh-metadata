The dataset contains model output from an agricultural land use model at kilometre scale resolution over Great Britain (GB) for 4 different climate and policy scenarios.

## Overview
- Provides yearly arable land area on a 2 km x 2 km grid for Great Britain from 2000 to 2089.
- Four scenario combinations: climate tipping point (AMOC collapse) vs standard climate change, with or without widespread irrigation.
- Output intended to support environmental monitoring, policy evaluation, and future decision-making regarding land use under climate and irrigation conditions.

## Data sources and climate drivers
- Climate inputs: Met Office Hadley Centre Regional Model Perturbed Physics Ensemble simulations for the UK (HadRM3-PPE-UK), UKCP09; daily data 1950–2100 at ~25 km resolution, bias-corrected by shifting future projections by the mean bias (1960–1989).
- AMOC collapse scenario: derived from HadGEM3 model with GC2 configuration; includes a progressive collapse from 2030–2050 using a linear weighting of AMOC differences; results used to create an idealised climate shift.
- Irrigation: modelled as a threshold where grid cells receive at least the rainfall level deemed optimal for GB arable farming, representing widespread irrigation.

## Scenarios and simulations
- Four scenario codes:
  - 1: Climate tipping point = No; Irrigation = No
  - 2: Climate tipping point = No; Irrigation = Yes
  - 3: Climate tipping point = Yes; Irrigation = No
  - 4: Climate tipping point = Yes; Irrigation = Yes
- Timeframe: 2000–2089; grid resolution: 2 km x 2 km across GB.
- Driving data period for climate means: growing season (April–September) means of the preceding 30 years.

## Outputs and data structure
- Four CSV files named Ag_model_sc{scenario #}.csv containing:
  - Unique grid cell identifier
  - Total arable land area per grid cell (hectares; max 400 ha)
- Grid reference file Ag_model_grid_2km.csv containing:
  - Grid cell center coordinates (easting, northing)
  - Corner coordinates (min/max x and y)
  - Matching to unique grid cell identifiers
- Baseline input data: land-use data derived from the June Agricultural Census on a 2 km grid over GB, covering 1972–2010 (ten unevenly spaced years).

## Quality control and methodological basis
- Outputs produced using the approach developed by Fezzi & Bateman (2011), central to the UK National Ecosystem Assessment framework.
- Data structure and input data have been widely peer-reviewed (e.g., Fezzi et al. 2014, 2015; Bateman et al. 2013, 2014).
- Spatial resolution and annual outputs enable site-specific monitoring and policy analysis.

## Data provenance, sharing, and governance
- Data provenance linked to the June Agricultural Census and established climate projections; bias correction applied to align with observed data.
- Metadata and data sharing considerations acknowledged: attempts to verify and supplement metadata by contacting data originators; public sharing of underlying data discussed as part of data governance and openness.
- Outputs are designed to be interoperable (grid IDs and coordinates) to support integration into monitoring dashboards, policy evaluation, and scenario testing.

## References and supporting materials
- Key methodological and validation references include Fezzi & Bateman (2011), Fezzi et al. (2014, 2015), Bateman et al. (2013, 2014), Jackson et al. (2015), Jenkins (2009), Mecking et al. (2016), Nakicenovic et al. (2000), UKCP09 (2014), and related UK NEA work.