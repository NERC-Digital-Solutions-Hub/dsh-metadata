# Overall sampling design

- Aim
  - Assess how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with geology, by measuring process rates and correlating them with functional gene copy numbers.

- Spatial sampling design
  - At each site, 9 soil samples collected within a 40 × 40 m transect at 20 m intervals.
  - Sub-samples prepared and stored differently depending on the analysis to be performed.

- Data products (GIS-ready emphasis)
  - Process rates: mineralization, nitrification, denitrification, nitrous oxide (N2O) production.
  - Environmental and soil properties: soil moisture, soil pH, ammonium, nitrate, soil temperature, etc.
  - Metadata linking samples to site location, geology, and river context to enable spatial mapping and cross-dataset integration.

- Depth and sampling details
  - Focused on 0–10 cm surface soils.
  - Exetainer-based incubation and measurement protocols described for rate calculations.

## Methodologies (data generation and measurement approaches)

- Soil water content and soil pH
  - Measured using the methods of Rowell (Soil Sciences Methods and Applications, 1994).

- Mineralization and nitrification rates
  - Determined by isotope dilution; calculations follow Kirkham and Bartholomew (1954).

- Denitrification
  - Measured using a 15N enrichment technique developed for this research.
  - About 3 g of 15N-enriched soil (40% 15N) weighed into each of 12 exetainers (12.5 ml) and incubated at in situ temperature for 2 days.

- Nitrous oxide (N2O) production
  - Measured by Gas Chromatography with an Electron Capture Detector (GC-ECD), following Robinson (Estuary N2O sources, Mar Ecol Prog Ser).

- Ammonium and nitrate extraction and analysis
  - Ammonium and nitrate extracted with 2 M KCl.
  - Ammonium quantified by colorimetric analysis (Krom, 1980).
  - Nitrate quantified by ultraviolet absorption at 220 nm (John & Coletti, 2002).

- Practical extraction details
  - Aliquots of soil (8 g wet weight) for ammonium; 4 g for nitrate.
  - Extraction performed with 40 ml 2 M KCl, shaking, roller extraction, centrifugation, filtration, and appropriate analytical methods.

- Operational specifics
  - 3 g of soil per measurement unit used for incubation-based rate assessments.
  - Exetainers and incubation times standardized across measurements.

## Data structure and metadata (Identifying information)

- Year and date
  - Year, Measurement; Year, Definition; date, Measurement; date, Definition (Month-Year).

- Site naming and geography
  - site.name: Short site name; encoding scheme:
    - First letter = underlying geology (C = chalk, A = clay, G = greensand)
    - Second letter = initial of river name
    - Number = site-specific identifier (e.g., GA2 = River Avon; CW2 = River Wylye; AS2 = River Sem)
  - geology: Sub-catchment underlying geology type; definitions: Clay, Chalk, Greensand.
  - Lat/long context: Several site identifiers include lat/long for rivers to facilitate mapping (e.g., GA2: 51.318289, -1.8600020).

- Measured variables (example keys and units)
  - mineralisation: Rate of mineralization; µg N g-1 dry weight soil day-1.
  - nitrification: Rate of nitrification; µg N g-1 dry weight soil day-1.
  - dn.insitu.moisture: In situ water content for denitrification; %.
  - dn.sat.moisture: Denitrification rate when soil saturated; %.
  - n2o.insitu.moisture: In situ water content for N2O production; %.
  - n2o.saturated.moisture: N2O production when soil saturated; %.
  - soil.ph: Soil pH; pH units.
  - water.content: Soil water content; %.
  - soil.temp: Soil temperature; °C.
  - ammonium: Soil ammonium; µmol NH4 g-1 dry weight soil day-1.
  - nitrate: Soil nitrate; µmol NO3 g-1 dry weight soil day-1.

- Quality control and validation
  - Measurements validated by the Centre for Ecology & Hydrology, Lancaster.

## GIS-focused considerations and implications

- Data integration
  - The site naming scheme and geology metadata enable linking soil process rates to geological maps and river catchments for spatial analyses.
  - Coordinate details for rivers are provided; ensure sample locations can be georeferenced using the site encoding and any available coordinates.

- Resolution and scale
  - The 9-sample-per-site design within 40 × 40 m plots yields moderate spatial resolution suitable for mapping within landscape-scale units; align with existing geospatial layers (geology, hydrology, land cover).

- Data quality and standardization
  - Diverse measurement methods and units across variables; harmonize units and maintain method-level metadata for reproducibility in GIS analyses.
  - QA validation by a recognized authority (CEH, Lancaster) supports data credibility for spatial analyses.

- Data management and packaging
  - Multi-method data (soil properties, isotopic process rates, N2O production) should be organized into a consistent schema with clear field mappings for GIS import (e.g., CSV/SHP/GeoPackage with metadata).
  - Include the Identifying information and methodological references as metadata to support provenance and re-use.

- Potential challenges
  - Data depth limitation (0–10 cm) may affect integration with deeper soil datasets.
  - Data may come from multiple analyses requiring careful data cleaning and joining by site and date.
  - Large or complex datasets may require chunking and careful packaging for efficient GIS processing.