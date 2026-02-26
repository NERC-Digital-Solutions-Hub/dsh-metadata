# Coastal and Biodiversity Ecosystem Service Sustainability (CBESS) soil moisture content from three soil depths on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset measuring soil moisture content (%) at three depths (0–10 cm, 10–20 cm, 20–30 cm) on salt marsh sites in Essex and Morecambe Bay.
- Field measurements taken from bulk density samples in 1 m × 1 m quadrats during Winter and Summer 2013; Essex winter samples also collected in early March 2013.
- Staff: Hilary Ford.

## Location and sampling design
- Essex sites:
  - Abbotts Hall (AH): 51°47'N, 0°52'E
  - Fingringhoe Wick (FW): 51°49'N, 0°58'E
  - Tillingham Marshes (TM): 51°41'N, 0°56'E
- Morecambe Bay sites:
  - Cartmel Sands (CS): 54°10'N, 3°0'W
  - Warton Sands (WS): 54°8'N, 2°48'W
  - West Plain (WP): location described but coordinates not listed
- Site characteristics:
  - Essex: clay soils, hare-grazed; heavily grazed by Brent geese at AH and FW.
  - Morecambe Bay: sandy soils, intensive sheep grazing at CS and WS; pink-footed geese winter grazing; West Plain lightly grazed.
- Sampling framework:
  - 1 m × 1 m quadrats; 3 depth measurements per quadrat; repeated in Winter and Summer 2013.
  - Additional Essex winter sampling window: 2–6 March 2013.

## Variables and data structure
- Primary variables:
  - SMC_1: soil moisture content (%) at 0–10 cm
  - SMC_2: soil moisture content (%) at 10–20 cm
  - SMC_3: soil moisture content (%) at 20–30 cm
- Data fields:
  - Row Number (sorting key)
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: CS, WS, WP (Morecambe); AH, FW, TM (Essex)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat Number: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)
  - SMC_1, SMC_2, SMC_3 (numeric)
- Data accessibility:
  - File format: Excel workbook
  - NA denotes data not available (loss of sample during processing)

## Data collection and quality notes
- Field collection:
  - Moisture measured from bulk density samples taken at approximately 0–10 cm, 10–20 cm, and 20–30 cm using a 3.1 cm height, 7 cm diameter bulk density ring.
  - Fresh mass measured, then samples dried for 72 hours at 105°C to determine water content.
- Calibration and quality control:
  - No documented calibration procedures, statistical treatment, or data quality checks in the metadata (entries marked as None/NA).