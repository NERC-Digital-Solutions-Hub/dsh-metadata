# Coastal and Biodiversity Ecosystem Service Sustainability (CBESS) soil moisture content from three soil depths on salt marsh sites at Morecambe Bay and Essex

## Overview
- Field measurements of soil moisture content (%) at three depths on salt marsh sites in Morecambe Bay and Essex.
- Collected during Winter and Summer 2013, with an additional Essex winter sampling window (2–6 March 2013).
- Staff: Hilary Ford.

## Data collection and methodology
- Measurements taken from bulk density samples in each 1 m x 1 m quadrat.
- Depth zones: 0–10 cm, 10–20 cm, 20–30 cm.
- Bulk density ring: 3.1 cm height, 7 cm diameter.
- Wet mass measured in the field; samples oven-dried at 105°C for 72 hours to determine water/content.
- Data format: Excel workbook; NA indicates data not available due to sample loss.

## Location and site context
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Coordinates:
  - Essex: AH 51.78°N, 0.87°E; FW 51.82°N, 0.97°E; TM 51.69°N, 0.93°E.
  - Morecambe Bay: CS 54.17°N, 3.00°W; WS 54.13°N, 2.80°W; WP (location code listed but coordinates not provided here).
- Habitat and soil context:
  - Essex: clay soils; hare-grazed, with heavy Brent goose grazing at AH and FW.
  - Morecambe Bay: sandy soils; intensive sheep grazing, with pink-footed geese grazing in winter; West Plain lightly grazed.

## Variables and data structure
- Primary variable: Soil moisture content (%) at three depths.
  - SMC_1: 0–10 cm
  - SMC_2: 10–20 cm
  - SMC_3: 20–30 cm
- Dataset fields and coding:
  - Row Number (sorting order)
  - Season: Winter (W), Summer (S)
  - Location: Morecambe (M), Essex (E)
  - Site: CS, WS, WP (Morecambe); AH, FW, TM (Essex)
  - Habitat: Mudflat (MF), Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)
  - SMC_1, SMC_2, SMC_3: moisture at respective depths
- Data completeness:
  - NA entries indicate missing data due to sample loss.

## Data quality, processing, and format
- Procedures described for field collection and lab drying; no explicit calibration or statistical processing documented beyond basic moisture calculation.
- Quality control fields (calibration, statistics, data checking) are listed but not populated in the record.
- File format: Excel workbook.

## Access, stewardship, and reuse considerations for Data Leaders
- Provenance: field team and site-era context included; location, habitat, and grazing regimes documented to aid interpretation.
- Documentation gaps: some metadata fields labeled None or blank (calibration, QC, etc.); consider completing for full governance.
- Discoverability and interoperability:
  - Structured schema with explicit codes for sites, habitats, depths, and seasons supports linking with other CBESS datasets.
  - Clear depth-specific moisture variables enables straightforward cross-dataset analyses.
- Next steps for data governance:
  - Validate and fill missing metadata (calibration, QC procedures, data checks) to strengthen trust.
  - Standardize site codes, coordinates, and habitat descriptors across CBESS datasets.
  - Assess data gaps (gaps in seasons, sites, or depths) and plan targeted data collection or metadata enrichment.
  - Ensure clear licensing or usage rights if disseminating beyond the owning organization.