# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil bulk density from three soil depths on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset documenting bulk density (g/cm3) across three soil depths (0–10 cm, 10–20 cm, 20–30 cm) for salt marsh sites in Essex and Morecambe Bay.
- Samples collected in Winter and Summer 2013, with additional Essex winter sampling (2–6 March 2013).
- Staff responsible: Hilary Ford.
- Sites include Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM); Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS). Location coordinates are provided for each site.
- Site descriptions note contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing grazing/inundation regimes.

## Data scope and structure
- Variables observed: Bulk density (g/cm3) at three depths (D1 0–10 cm, D2 10–20 cm, D3 20–30 cm).
- Sampling units: Bulk density rings (3.1 cm height, 7.5 cm diameter) within quadrats; three depth zones per quadrat.
- Sampling design: Quadrats with 22 rows of data described; sites include different habitats (Mudflat, Saltmarsh) and scales (A–D) for spatial context.
- Data format: Excel workbook; NA cells indicate missing data.
- File formats used: Excel workbook.

## Metadata, provenance, and field descriptions
- Location context: Saltmarsh sites chosen to represent two contrasting soil types; Essex sites are hare-grazed and heavily grazed by Brent geese in winter; Morecambe Bay sites are heavily sheep-grazed with pink-footed geese grazing in winter, compared to lightly grazed West Plain.
- Procedures: Soil samples dried at 105°C for 72 hours prior to bulk density calculation (dry mass / core volume).
- Dataset fields include:
  - Row Number (sorting key)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m, B: 1–10 m, C: 10–100 m, D: 100–upper)
  - BD_D1 (bulk density 0–10 cm)
  - BD_D2 (bulk density 10–20 cm)
  - BD_D3 (bulk density 20–30 cm)

## Data quality, standards, and governance
- Calibration procedures: None noted.
- Data quality controls: Explicit data checking procedures exist but details are not provided.
- Transparency and documentation: Core metadata (locations, depths, habitats, sampling times, and methods) is documented within the dataset description and field definitions.
- Provenance: Clear attribution to Hilary Ford and explicit site descriptions, coordinates, and historical grazing/inundation context.

## Access, sharing, and updates (governance considerations)
- Primary format: Excel workbook.
- Reusability considerations: Standardized field codes (Season, Location, Site, Habitat, Scale) and explicit depth definitions support interoperability, though some metadata (e.g., licensing, update procedures) is not specified.
- Sharing workflow (as per governance principles): Datasets should be uploaded to relevant portals and catalogues; ensure ongoing updates and metadata maintenance if new data are collected.

## Practical notes for data stewards
- Ensure consistent unit usage (g/cm3) across all records and documentation of the three depth intervals.
- Maintain and validate the mapping between Site, Location, Habitat, and Scale codes to prevent ambiguity.
- Promote completeness by addressing NA cells and documenting any missing data or gaps.
- Preserve provenance by maintaining links to site coordinates, sampling dates, and the drying/measurement protocol.
- Consider adding explicit data license, data access constraints, and a clear update schedule to support reuse and long-term stewardship.
- If integrating with a larger CBESS data catalogue, align field names and value vocabularies with existing metadata schemas.