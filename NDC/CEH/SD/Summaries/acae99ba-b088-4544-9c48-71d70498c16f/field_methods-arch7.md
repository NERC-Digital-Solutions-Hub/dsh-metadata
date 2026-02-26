# Materials and methods

- Overview
  - Multisite sampling to represent different endotoxin exposure levels: an urban background site, a rural background site, a composting facility, and an intensive chicken farm.
  - Sampling occurred in summer and winter, with location-specific activities and distances to study features (e.g., windrows, sheds).

- Study sites and sampling locations (GIS-relevant context)
  - Rural background: farmland near farmland, at least 2.5 km from major towns.
  - Urban background: empty car park about 100 m from a dual carriageway.
  - Composting facility: processes green waste and food waste; sampling 20–50 m from windrows during activities (turning, screening, shredding); occasional waste delivery or compost removal during sampling.
  - Intensive chicken farm: up to 23,000 chickens across eight 60 × 20 m sheds; 7 sheds in use during sampling; boundary sampling 20–50 m from sheds.
  - Sampling schedule relative to poultry age: 12, 15, 21, and 27 days old; boundary sampling at specified distances.

- Instruments and measurements (data streams for GIS visualisation)
  - Osiris particulate monitor:
    - Measures total suspended particulates (TSP), PM10, PM2.5 using light-scattering.
    - Operating at 0.6 L/min for at least 30 minutes per location, concurrently with bioaerosol sampling.
    - Logs temperature, relative humidity, wind speed, and wind direction every minute.
  - Andersen samplers (bioaerosols):
    - Two eight-stage non-viable samplers used for endotoxin and particle size characterization.
    - Flow 28.3 L/min; sampling days include at least 3 × 1-hour runs per day (total 6 filter sets).
  - Field and laboratory QA instrumentation:
    - Filters decontaminated before sampling; handling and transport protocols to lab; samples analyzed within 24 hours.

- Sampling and laboratory procedures (operational details for data provenance)
  - Endotoxin sampling and analysis:
    - Filters extracted with pyrogen-free water; shaking and sonication; centrifugation to remove glass fibre.
    - Endotoxin quantified with kinetic chromogenic LAL assay (Glucashield used to prevent Glucan interference).
    - Standard curve: control endotoxin in range 50 to 0.005 EU/mL; plate incubated at 37°C with reading at 405 nm for 90 minutes.
    - Each sample assayed in duplicate.
  - Viable microorganisms sampling and analysis:
    - Single-stage Andersen samplers used with nutrient agar (NA), MacConkey (MAC), and malt extract agar (MEA) per AfOR Protocol.
    - Plates incubated for 48 hours, then checked at 3–4 days for bacteria (37°C) and fungi (40°C) to favour thermotolerant fungi.
    - Four duplicate samples per location; field blanks and control plates included to assess contamination.
    - Positive hole correlation applied when plates exceed 20 colonies to estimate total counts.
    - Results expressed as colony forming units per cubic metre (CFU/m³); LOD for viable microorganisms with single-stage sampler: 4 CFU/m³.
  - Contamination controls:
    - Control filters exposed to the Andersen sampler without pumping to check contamination.
    - Field blanks (plates loaded and transported without exposure) and other blanks routinely used.

- Data quality assurance and standardisation (GIS-ready data aspects)
  - Replicates and blanks used to assess contamination and variability.
  - Consistent sampling protocols across sites to enable cross-site comparisons.
  - Data include sample location, sampling time, device readings (Osiris), wind conditions, endotoxin concentrations (EU/mL), and viable CFU/m³ counts.

- Schedule, context, and constraints (temporal and logistical)
  - Sampling occurred during both summer and winter seasons.
  - At the poultry site, several age points (days 12, 15, 21, 27) with boundary sampling near sheds.
  - Composting activities (turning, screening, shredding) occurred during sampling windows.

- Outputs and GIS-ready data opportunities
  - Spatial layers:
    - Sampling locations by site type (urban/rural background, composting facility, intensive farm).
    - Distances to key features (windrows, sheds, boundaries).
    - Wind data (speed and direction) linked to each sampling time.
  - Temporal layers:
    - Time-stamped measurements for Osiris (TSP, PM10, PM2.5, temperature, humidity, wind) and for endotoxin and viable microbial counts.
  - Data products:
    - Maps of pollutant distributions (concentrations by location and time).
    - Size-fraction data (particle-size-resolved concentrations) from Osiris.
    - Endotoxin concentration surfaces and CFU/m³ distributions.
  - Quality flags:
    - Replicate and blank results, LOD considerations, and QA notes to accompany GIS layers.