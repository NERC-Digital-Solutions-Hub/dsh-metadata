# Background

- Context
  - NERC Soil Biodiversity Thematic Programme (established 1999) focused on an intensive field experiment at Sourhope (Macaulay Land Use Research Institute, now James Hutton Institute) in the Scottish Borders (grid reference NT8545019630).
  - Aimed to understand soil biota diversity and the functional roles of soil organisms in key ecological processes.
  - Funded 24 separate projects covering soil structure, soil processes (e.g., carbon and nitrogen cycles), and the roles of micro-, meso-, and macro-fauna.

- Site and data emphasis
  - The programme involved long-term monitoring of aboveground biomass production, species composition, and relative abundance.
  - Meteorological and related environmental data were collected to contextualize soil biodiversity studies.

- GIS-relevant context
  - The document provides a core weather dataset from a on-site Automatic Weather Station (AWS) that can be linked to soil biodiversity observations for spatial-temporal analyses.

---

## Meteorological data

- Data collection period
  - February 1999 to September 2002.

- Data source and delivery
  - On-site AWS located on experimental plots.
  - Data regularly downloaded and transmitted to the Soil Biodiversity Data Manager at the Centre for Ecology & Hydrology (CEH).

- Data format
  - Hourly summaries derived from 5-second samplings.
  - File: CHA_Sourhope_AWS_1999_2002.csv (CSV).

- Dataset scope and location context
  - Collected at the Sourhope field site; data can be associated with map-based analyses of the experimental plots via the grid reference provided (NT8545019630).

- Dataset columns and units
  - EXPERIMENT_ID: 'AWS'
  - AWS_DATE: Date
  - AWS_TIME: Time
  - RAINFALL: mm
  - WIND_SPEED: ms-1
  - WIND_DIRECTION: degrees (0-360)
  - AIR_TEMP: °C
  - SOIL_TEMP_2CM: °C
  - SOIL_TEMP_MINUS_2CM: °C
  - SOIL_TEMP_MINUS_5CM: °C
  - SOIL_TEMP_MINUS_10CM: °C
  - SOIL_TEMP_MINUS_30CM: °C
  - SOIL_MOISTURE: m3m-3

- Data management and accessibility
  - Data managed by the Soil Biodiversity Data Manager at CEH; part of the NERC programme data assets.

---

## Data quality and governance

- Quality control
  - Verification steps include numeric range checks, data formatting checks, and logical integrity checks.

- Limitations and liability
  - NERC is not warranted to the accuracy of the data.
  - No responsibility for the fitness of the data for the user’s intended use.
  - Provision of data carries no liability for loss, damage, or injuries arising from use.

---

## GIS-oriented considerations

- Potential uses for map-based analyses
  - Temporal contextualization of soil biodiversity observations with weather variables.
  - Linking AWS-derived weather variables to spatially referenced soil plots for climate–soil–biota studies.

- Data preparation notes
  - Convert CSV time series to GIS-friendly formats (e.g., time-enabled point features or raster layers for summaries).
  - Ensure consistent coordinate reference system and align with plot-level geolocation (grid reference NT8545019630).
  - Verify units and handle any metadata gaps; document data quality and QA steps.

- Integration opportunities
  - Combine with the broader 24-project soil biodiversity datasets to produce thematic maps of soil processes, biodiversity indices, and environmental drivers.
  - Use time stamps to create dynamic maps or time-enabled visualizations for policy briefs, clients, or public-facing outputs.