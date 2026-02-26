# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment water content in saltmarsh and mudflat habitats

- Purpose and scope
  - Measures percentage water content in the surface sediment (2 mm) of saltmarsh and mudflat habitats to support environmental health monitoring and policy evaluation.
  - Seasonally sampled in winter and summer 2013; aims to provide baseline data across contrasting habitat types and regions.

- Study design and locations
  - Regions: Essex (saltmarsh with clay soils) and Morecambe Bay (saltmarsh with sandy soils).
  - Habitat contrasts: saltmarsh and mudflat sites to represent differing sediment types, inundation frequency, creek structure, and vegetation.
  - Sites and sites’ descriptions reflect broad environmental distinctions between the two regions.

- Sampling design
  - Sampling framework: general CBESS field campaign conducted in winter and summer 2013.
  - Quadrat layout: random allocation of 1x1 m quadrats to each mudflat and saltmarsh site.
  - Replicates: five replicates per quadrat; seasonal sampling conducted, with no planned repeat sampling of quadrats.
  - Quadrat count: 22 quadrats allocated per mudflat/saltmarsh site per region.

- Measurements and procedures
  - Variable observed: percentage water content of surface sediment.
  - Field/lab procedures: surface 2 mm of sediment sampled with a contact corer; flash-frozen with liquid nitrogen, stored below -80°C.
  - Laboratory processing: wet and dry weights determined after drying (freeze-dried) to calculate water content.
  - Spatial allocation: quadrats assigned across four spatial scales via R to define A (1 quadrat), B (three quadrats 1 m to 10 m apart), C (six quadrats 10 m to 100 m apart), D (twelve quadrats 100 m to 1000 m apart).

- Data structure and metadata
  - Data format: comma-separated values (.csv).
  - Core fields (examples): Season (Winter, Summer), Location (Morecambe, Essex), Site (e.g., CS, WS, WP, AH, FW, TM), Habitat (Mudflat, Saltmarsh), Quadrat Number (1–22), Scale (A–D), Percentage Water Content (average per quadrat), StDev (standard deviation), Other information (NA indicates missing due to inaccessibility).
  - Data quality and description: detailed dataset field descriptions and headers provided to enable traceability and reuse.
  - Processing and calibration: scales and laboratory protocols calibrated according to standard procedures; room for data quality checks through spreadsheet entry of readings.

- Data governance, sharing, and accessibility
  - Data are organized with extensive metadata to facilitate governance and reuse in monitoring frameworks.
  - Underlying data formats are open (CSV) with explicit field definitions and site-specific metadata.
  - Clear documentation of potential data gaps (e.g., NA entries due to inaccessibility) to support transparent interpretation.

- Temporal coverage and repeatability
  - Temporal scope: winter and summer 2013.
  - No planned repeat sampling of the same quadrats beyond the two seasonal timepoints in 2013.

- Practical considerations for monitoring frameworks
  - Provides a concrete, reproducible method for assessing sediment water content across contrasting coastal habitats.
  - Demonstrates integration of randomised spatial sampling, standardized lab workflows, and clear data governance.
  - Highlights typical challenges for monitoring data: data completeness, metadata richness, and harmonization across sites with differing habitat characteristics.