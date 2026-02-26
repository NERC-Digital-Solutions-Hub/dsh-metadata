# Data collected 2017-18 during field transplant on Mt Etna

## Overview
- Field transplant study on Mt Etna across four elevations (500 m, 1000 m, 1500 m, 2000 m above sea level).
- Three Tinytag dataloggers deployed at plant height near transplanted plants at each elevation.
- Dataloggers recorded daily minimum and maximum temperatures over a 1-year period, then were collected for extraction of Temp.Min and Temp.Max (°C).

## Data collection details
- Dataloggers placed adjacent to transplanted plants to capture near-plant microclimates.
- Instruments left in the field for 12 months before retrieval.
- Prior to deployment, all dataloggers were kept together to help ensure accuracy (quality control practice).

## Variables / data structure
- Elevation: Transplant elevations (500 m, 1000 m, 1500 m, 2000 m ASL).
- Block: Three replicate plots (A, B, C) at each elevation, representing within-elevation replication.
- Date: Date of temperature recording.
- Temp.Min: Daily minimum temperature (°C).
- Temp.Max: Daily maximum temperature (°C).

## Data quality and preparation
- Pre-deployment quality control by keeping dataloggers together to check accuracy.
- Data intended for downstream analysis and visualization to support exploration of temperature patterns across elevations and replicates.

## Potential uses for data support
- Build time-series analyses of temperature variation by elevation and replicate.
- Create dashboards or pivot-table reports to enable self-serve exploration of daily min/max temperatures.
- Compare microclimate differences across elevations, assess consistency across blocks, and inform related ecological or plant-transplant studies.
- Integrate with other datasets (e.g., phenology, plants’ health metrics) to assess temperature-related effects.

## Considerations for end users
- Data represent daily min/max temperatures at plant height over a 12-month period at Mt Etna.
- Structure supports grouping by Elevation and Block; Date enables temporal analyses.
- If combining with other datasets, ensure consistent date formats and unit interpretation (degrees Celsius).