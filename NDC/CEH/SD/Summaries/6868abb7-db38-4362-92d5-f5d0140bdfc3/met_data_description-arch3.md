# Supporting Documentation

## Overview
- Dataset name: Hampshire Avon: soil temperature and water content data from three sub-catchments (two entries listed; depositor James Stockdale).
- Depositor and contact: James Stockdale, james.stockdale@york.ac.uk.
- File details: met_data.csv covering measurements from 02 December 2013 to 02 September 2015.
- Location references: Chalk site at OS grid ST 85862 38261; Clay site at OS grid ST 92218 27263; Greensand site at OS grid SU 09720 57896.
- Measurements: soil temperature (°C) and volumetric water content (m3 m-3) from plots under two conditions (control and warming) co-located with lysimeters in unimproved pastures.
- Purpose in dataset: near-continuous, hourly-mean soil measurements across three geologies to assess warming effects on soil temperature and moisture.

## Dataset structure
- datetime: date and time of measurement conclusion (format ddmmmyyyy:hh:mm:ss).
- site: two-character code per site; CH = Chalk, CL = Clay, Greensand site designated separately.
- plot: numeric identifier for each measurement plot.
- treatment: two-character code for treatment; CO = control, warming.
- temp: soil temperature in degrees Celsius.
- moisture: volumetric water content in m3 m-3.

## Methods summary
- Experimental setup: plots co-located with lysimeters in unimproved pastures across three underlying geologies (Chalk, Clay, Greensand).
- Depth and position: sensors placed 5 cm below soil surface.
- Treatments: ambient (control) and active surface warming.
- Instrumentation: 
  - Thermistor for soil temperature (ST1, Delta-T Devices).
  - Theta probe for volumetric water content (ML2, Delta-T Devices).
  - Data loggers: GP1 and DL2e (Delta-T Devices).
- Data handling: near-continuous measurements with hourly means; quality control to remove failed sensors (commonly due to animal damage).

## Data quality and governance considerations
- Metadata and traceability: dataset includes site codes, coordinates, and units, with explicit sensor types and data loggers.
- Quality control: post-measurement QC to exclude faulty sensors; ensures cleaned data for analysis.
- Data sharing and provenance: depositor contact provided; dataset appears to be documented for reuse, but explicit public access conditions are not stated; data governance steps (documentation, transparency, and source data management) are outlined.
- Potential data transformation: raw readings are summarized into hourly means; format is structured for integration into monitoring frameworks.

## Relevance for Monitoring Frameworks
- Demonstrates a structured approach to environmental monitoring data: clear variables, standardized coding for sites and treatments, and explicit measurement practices.
- Highlights the importance of metadata, data provenance, and quality control in building trustworthy datasets for policy evaluation.
- Provides a concrete example of how to capture climate-related soil responses (temperature and moisture) under controlled warming vs. ambient conditions across multiple geologies.

## Limitations and considerations for policy use
- Temporal coverage: data span mid-2013 to late-2015; may limit long-term trend analyses.
- Spatial scope: only three sub-catchments representing three geologies; results may not generalize beyond these sites.
- Potential data gaps: hourly data processing implies potential gaps if sensors failed; QC steps mitigate but users should verify completeness.
- Access considerations: while contact is provided, explicit data access permissions are not detailed; governance and licensing should be confirmed for reuse.