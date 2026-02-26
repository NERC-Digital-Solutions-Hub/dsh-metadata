# Survey Overview

- Purpose and scope: A monitoring study within the NERC InSAR ToPS project to assess climate impacts on peatlands in the Flow Country (Caithness and Sutherland) from Sept 2017 to Nov 2018, using multiple measurement approaches (peat cores, teabag index, peat depth, humification, bulk density, moisture, LOI, OC, and ash) to inform understanding and decision-making about environmental health and carbon dynamics.

- Study sites and context:
  - Knockfin Heights, upland blanket bog (>300 m above sea level), part of the RSPB Forsinard estate; features include peat hags, drained/undrained pools, and a mix of sedge, sphagnum, heather, and grasses.
  - Munsary, lowland blanket peatland within the Plantlife Munsary Nature Reserve; features numerous pool systems (Dubh Lochans), near-natural condition with historic grazing, peat extraction, and recent restoration (drain blocking).

- Measurement approaches and protocols:
  - Peat cores: Russian corer (max 4 m), sectioned into 50 cm intervals; first 50 cm sampled at 5 cm increments, remaining at 10 cm; on-site description of texture and features; bulk volume measured for Knockfin Heights when access issues prevented standard sampling.
  - Peat depth: measured in November 2018 on a predefined 1 km^2 grid; depth relative to peat surface following NatureScot guidance (Peat Depth and Condition Survey, 2021).
  - Teabag Index (TBI): 100 pairs installed at benchmarks at ~5 cm depth during early June 2018 and retrieved in Sept 2018; data affected by deer damage and loss; calculations yield S (litter breakdown) and K (decomposition rate) using standard online tools.
  - Von Post humification: field evaluation following established methodologies (Von Post and Granlund; FAO references).
  - Bulk density: measured by water displacement on ~2 cm^3 peat samples; density values recorded for wet and dry states.
  - Soil moisture and LOI: moisture calculated from dry/wet masses; LOI derived from loss on ignition at 550°C (with OC estimated as half of LOI and Ash as remainder); standard equations applied.
  - Data interpretation and quality: samples described for features (e.g., air bubbles, texture); lab processing and calculations follow defined protocols (Chambers et al. 2011; FAO 2011; NatureScot 2021; related methodological references).

- Data management and file conventions (relevant to monitoring frameworks):
  - File naming and metadata structure: consistent conventions for site codes, sub-sites, environmental monitoring data, and sampling times; explicit field headers for each dataset (e.g., Peat Depth, Bulk Density, Teabag Index, TPI).
  - Key metadata fields: Waypoint_Name (site), Lat_OSGB and Long_OSGB (OSGB36 coordinates), Height_m.a.s.l (peat surface), Peat_Depth, X/Y coordinates for Teabag measurements, and descriptive Comments for site observations.
  - Data accessibility and governance: outputs presented via reports, charts, or dashboards; underlying data intended to be shared appropriately with stakeholders, following data governance principles; acknowledges potential barriers to public sharing of datasets and need for metadata standardization.

- Data products and markers:
  - Peat Depth data: depth measurements across the 1 km^2 grid; site-specific peat surface elevations recorded.
  - Bulk Density and LOI/OC/ash data: interval-based measurements along cores with associated metadata (site, interval, mid-point, density values, humification, LOI, OC, ash, moisture).
  - Teabag Index results: S and K values per benchmark location with site locations and coordinates.
  - Coring locations and protocol: a defined set of sub-sites (Munsary A–G, Knockfin A–F) with precise OSGB36 coordinates; sampling protocol includes 50 cm intervals and on-site processing steps.

- Survey area details and management context:
  - Knockfin Heights: large upland bog with drainage complexity; managed by multiple landowners; landscape features include peat pools and hummocks influencing sampling accessibility.
  - Munsary: lowland bog with high water table; patches of shrub-dominated margins; subject to historic and ongoing restoration; survey area is described as near-natural in condition.

- Practical considerations and challenges:
  - Deer damage noted at teabag benchmarks leading to loss/damage of samples and potential data gaps.
  - Data gaps and data sharing barriers acknowledged as considerations for monitoring frameworks; the need for robust metadata and standardized data formats to facilitate data reuse and governance.

- Methodological references and standards used:
  - Chambers, Beilman, and Yu (2011) for peat humification and carbon-related metrics.
  - FAO (2011) classification of organic soils and Von Post classification guidance.
  - NatureScot (2021) peat depth and condition survey guidance.
  - Teatime4Science protocols for teabag index methods and calculations.