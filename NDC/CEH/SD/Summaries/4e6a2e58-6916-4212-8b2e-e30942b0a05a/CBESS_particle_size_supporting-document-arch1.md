# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) sediment particle size in mudflat and saltmarsh habitats..

- Overview
  - Dataset collects sediment particle size data from CBESS project, focusing on mudflat and saltmarsh habitats.
  - Based on data from 6 sites across 2 locations, each with 2 habitats (mudflat and saltmarsh).
  - Sampling occurred in winter and summer 2013, with 3 replicates across 22 quadrats at 4 spatial scales.
  - Staff responsible: Christina Wood and Martin Solan.

- Locations and Habitat Context
  - Essex sites: Abbotts Hall (AH) and Fingringhoe Wick (FW); saltmarsh habitats with clay soils representative of south-eastern Atlantic UK.
  - Morecambe Bay sites: Cartmel Sands (CS) and Warton Sands (WS); saltmarsh habitats with sandy soils representative of west UK.
  - Saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation; mudflat sites in Essex are cohesive clay, mud, and silt, while Morecambe mudflats have coarser, mobile sediments.

- Sampling Design and Timeline
  - Part of the general CBESS field campaign (winter and summer 2013).
  - No planned repeat sampling beyond the 2013 campaigns.
  - Design includes 3 replicates per site, across 22 quadrats, spanning 4 spatial scales.

- Variables and Measurements
  - Primary variable: sediment particle size.
  - Sampling methods:
    - Mudflats: surface sediment scrapes.
    - Saltmarsh: sediment cut from 2 cm below surface.
  - Samples frozen at -20°C and analyzed using the Malvern Mastersizer particle size protocol.
  - Measured and reported metrics include multiple percentiles and size distributions (e.g., d(0.050), d(0.160), d(0.5), d(0.840), d(0.950)), D[4,3] (mean particle size descriptor), inclusive mean (Phi), kurtosis, skewness, standard deviation, and various clay/silt fractions across phi classes.
  - Many field definitions are provided to describe how each measurement is derived and represented (see dataset field descriptions).

- Procedures, Calibration, and Quality Control
  - Calibration and measurement details linked to external resources (e.g., Gradistat, Malvern Mastersizer protocol).
  - Data checking procedures documented via linked resources.
  - Full methodology and references available in linked information (e.g., external technique pages and related literature).

- Data Structure and Formats
  - File format: CSV.
  - Dataset fields include: Row Number, Season (Winter W / Summer S), Location (Essex E / Morecambe M), Site (AH, FW, TM for Essex; CS, WS for Morecambe), Habitat (Mudflat MF or Saltmarsh SM), Quadrat Number, Scale (A-D with defined spatial extents), Replicate, Measurement Type (PSA), and numerous particle-size descriptors (e.g., d(0.050), d(0.160), d(0.5), D[4,3], inclusive mean, inclusive kurtosis, inclusive skewness, inclusive standard deviation, etc.), as well as %Clay across size fractions.
  - Some metadata notes reference additional sources (e.g., Blott & Pye 2001; Gradistat) and include links to detailed methodology and calibration.

- Data Use, Access, and Documentation
  - Context and provenance documented; data are part of the CBESS dataset collection.
  - Links provided to full articles and technique pages for deeper methodological understanding.
  - The data are suitable for analyses of spatial-scale effects on sediment size distributions and potential links to habitat characteristics and ecosystem services.

- Considerations and Limitations for Analysts
  - Limited to winter and summer 2013 snapshots; no planned repeat sampling for these sites beyond that campaign.
  - Cross-site comparability is supported by standardized measurement protocol but differences in habitat type and soil texture (clay vs. sand) may influence size distributions.
  - Complex dataset with many interrelated size metrics; careful handling of phi-based measures and unit consistency recommended.
  - Availability of metadata and calibration references enhances reproducibility but requires consulting linked resources for full methodological details.