# Survey Overview

- Purpose and timeframe
  - To take peat cores and teabag index measurements to monitor climate impact over September 2017 to November 2018.
  - Sites located in the Flow Country, Caithness and Sutherland, Scotland.

- Survey sites and context
  - Knockfin Heights: upland blanket peatland (>300 m above sea level), part of the RSPB Forsinard Estate; diverse microtopography with peat hags, drained/undrained pools and lochans.
  - Munsary: lowland blanket peatland (~100 m a.s.l.), part of Plantlife Munsary Nature Reserve; features Dubh Lochans and near-natural peat margins; historic grazing, peat extraction and burning with recent restoration.
  - Overall goal: assess peat characteristics and decomposition dynamics across contrasting elevations and land management contexts in the Flow Country.

- Survey area details
  - Locations: RSPB Forsinard, Knockfin Heights (OSGB36 coordinates NC94958) and Plantlife Munsary (ND21677 46186) forming part of the Flow Country.
  - Site layout includes permanent benchmarks, environmental monitoring equipment, peat cores, and sample sub-sites.

- Coring locations and sampling protocol
  - Cores collected at multiple sub-sites:
    - Munsary A–G and Knockfin A–F with specific OSGB36 coordinates provided.
  - Method: Russian corer with maximum length 4 m; cores sectioned into 50 cm intervals.
  - Sampling scheme:
    - Within the first 50 cm: 5 cm interval sampling.
    - From 50 cm depth downward: 10 cm intervals.
  - On-site processing: each interval described (texture, air bubbles, etc.); at Knockfin Heights, peat volume measured on-site by difference due to accessibility; Munsary cores processed in the lab per Chambers et al. (2011).

- Peat depth measurement protocol
  - November 2018: relative peat depth measured on a predefined 1 km^2 grid around Knockfin Heights.
  - Measurements aligned to the peat surface; following NatureScot (2021) Peat Depth and Condition Survey Guidance.

- Teabag Index (TBI) component
  - 100 teabag pairs installed at benchmarks at ~5 cm depth in June 2018; removed in September 2018.
  - Purpose: assess litter decomposition with the 2018 European drought peak.
  - Observations: deer damage caused substantial loss/damage to teabags.
  - Post-processing: wet/dry weights used to calculate S (litter breakdown) and K (decomposition rate) using provided spreadsheets.

- Von Post humification
  - Humification classified in the field following Von Post and Granlund (1926) and FAO (2011) guidelines, with reference to FAO classifications.

- Bulk density and related soil chemistry
  - Bulk density measured by water displacement (wet vs dry mass), using approximately 2 cm^3 peat per sample.
  - Procedures include weighing, oven-drying, and calculating density.
  - Soil moisture and loss on ignition (LOI) calculated from oven-dried and ash measurements.
  - LOI, OC (organic carbon), and ash percentages derived from wet/dry weights and LOI equations.

- Data naming, structure, and metadata
  - File naming conventions:
    - Site codes: KH = Knockfin Heights, MUN = Munsary
    - ENV = Environmental Monitoring Data
    - SITE = SUB SITE A–F
    - WT = Water Level (collected separately)
  - Data fields and formats:
    - Peat Depth
      - Waypoint_Name, Lat_OSGB, Long_OSGB, Height_m.a.s.l, Peat_Depth, Comments
    - Bulk Density
      - Site, Interval, Mid, Density_gcm-3_wet, Density_gcm-3_dry, Von Post, Ash_%, LOI_%, Moisture_%, Comments
    - Teabag Index (TPI)
      - No, Site, X_BNG, Y_BNG, Location, S, K
  - References for methods:
    - Chambers, Beilman & Yu (2011): peat humification, bulk density, carbon content methodologies
    - FAO (2011): Organic soils classification
    - NatureScot (2021): Peat Depth and Condition Survey Guidance
    - Von Post & Granlund (1926)

- Key considerations and challenges
  - Accessibility constraints at Knockfin Heights affected on-site peat volume measurements.
  - Teabag deployment exposure to deer damage limited data at several benchmarks.
  - Data collection spanned diverse peatland types and required standardisation across sites for comparability.
  - Emphasis on traceable data provenance and metadata to facilitate cross-site analyses and dataset discoverability.