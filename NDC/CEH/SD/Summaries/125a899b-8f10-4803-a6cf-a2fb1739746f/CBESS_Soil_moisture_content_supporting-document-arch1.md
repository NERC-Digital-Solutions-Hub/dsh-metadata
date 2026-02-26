# Coastal and Biodiversity Ecosystem Service Sustainability (CBESS) soil moisture content from three soil depths on salt marsh sites at Morecambe Bay and Essex

## Overview
- Field-measured soil moisture content (%), across three depth intervals (0–10 cm, 10–20 cm, 20–30 cm).
- Locations: six saltmarsh sites split between Essex (clay soils) and Morecambe Bay (sandy soils).
- Sampling focused on understanding moisture patterns in relation to habitat type, inundation, and grazing regimes.

## Datasets and personnel
- Dataset name: CBESS soil moisture content from three soil depths on salt marsh sites at Morecambe Bay and Essex.
- Depths and variables: Soil moisture content (%) at 0–10 cm (SMC_1), 10–20 cm (SMC_2), and 20–30 cm (SMC_3).
- Staff responsible: Hilary Ford.
- File format: Excel workbook.
- Data notes: NA entries indicate data not available due to loss of sample during processing.

## Sites and locations
- Essex (E) sites:
  - Abbotts Hall (AH)
  - Fingringhoe Wick (FW)
  - Tillingham Marshes (TM)
- Morecambe Bay (M) sites:
  - Cartmel Sands (CS)
  - Warton Sands (WS)
  - West Plain (WP)
- Coordinates provided for each site.
- Habitat types:
  - Saltmarsh (SM)
  - Mudflat (MF)
- Regional contrasts:
  - Essex: predominantly clay soils, differing inundation and vegetation; hare grazing and Brent geese grazing noted at AH and FW.
  - Morecambe Bay: sandy soils, higher sheep grazing intensity; pink-footed geese graze in winter; West Plain lightly grazed.

## Sampling and methods
- Campaign period: Winter and Summer 2013; Essex winter samples included an additional window (2–6 March 2013).
- Sampling approach: Field soil moisture measured from bulk density samples taken in each quadrat (1 m x 1 m).
- Depths and equipment: Soil moisture measured at ~0–10 cm, 10–20 cm, and 20–30 cm using a bulk density ring (3.1 cm height, 7 cm diameter).
- Weight measurements: Samples weighed fresh, then after 72 hours at 105°C to determine water content.

## Data structure and fields
- Row structure: Row Number (numeric) to preserve original input order.
- Temporal and location fields:
  - Season: Winter (W) or Summer (S)
  - Location: Morecambe (M) or Essex (E)
  - Site: CS, WS, WP (Morecambe); AH, FW, TM (Essex)
- Habitat: Mudflat (MF) or Saltmarsh (SM)
- Quadrat Number: 1–22
- Scale: A = 1 m, B = 1–10 m, C = 10–100 m, D = 100–upper limit
- Variables:
  - SMC_1: Soil moisture content (%) at 0–10 cm
  - SMC_2: Soil moisture content (%) at 10–20 cm
  - SMC_3: Soil moisture content (%) at 20–30 cm
- Data status: NA indicates data not available due to sample loss

## Data quality and considerations
- Calibration procedures and quality control procedures are not provided in the dataset metadata.
- Some data gaps exist (NA entries) due to sample loss.
- Data are organized to support cross-site and depth-wise comparisons, with explicit site, habitat, and seasonal context to enable correlations with grazing regimes, inundation frequency, and vegetation differences.

## Usage notes for analysis
- Suitable for evaluating soil moisture patterns by depth and site, and for exploring relationships with habitat type, inundation regime, and grazing.
- When combining sites, account for regional soil type differences (clay in Essex vs sandy in Morecambe Bay) and differing grazing histories.
- Be mindful of incomplete data (NA entries) and potential temporal misalignment between winter and summer campaigns.