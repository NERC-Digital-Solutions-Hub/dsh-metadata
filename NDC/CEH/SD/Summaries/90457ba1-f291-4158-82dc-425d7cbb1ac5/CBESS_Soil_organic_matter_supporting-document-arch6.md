# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil organic matter content from three soil depths on saltmarsh sites at Morecambe Bay and Essex

## Overview
- Datasets soil organic matter (OM) content at three depths (0–10 cm, 10–20 cm, 20–30 cm) from saltmarsh sites in Morecambe Bay and Essex.
- OM measured by loss-on-ignition (LOI) using bulk density samples, collected during Winter and Summer 2013.

## Coverage and sites
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Site coordinates provided (lat/long) for each location.
- Habitat context: saltmarsh with contrasting soil types (Essex: clay; Morecambe Bay: sandy); differing inundation frequency, creek structure, and vegetation.
- Land use: Essex sites heavily grazed by over-wintering Brent geese and hare grazing; Morecambe Bay sites heavily grazed by sheep with geese grazing in winter; West Plain less intensive grazing.

## Sampling details
- Field campaign: Winter and Summer 2013; Essex winter samples collected 2–6 March 2013 as an additional window.
- Bulk density rings used (3.1 cm height, 7.5 cm diameter) to quantify three depth zones per quadrat.
- OM determined by LOI after drying: 105°C for 72 hours, then a sub-sample dried at 375°C for 16 hours.
- Staff responsible: Hilary Ford.

## Variables and data structure
- Primary variable: Soil organic matter (%) by depth (0–10 cm, 10–20 cm, 20–30 cm).
- Dataset fields include: Row Number (sorting index), Season (Winter, Summer), Location (Morecambe, Essex), Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex), Habitat (Mudflat, Saltmarsh), Quadrat Number, Scale (A=1 m; B=1–10 m; C=10–100 m; D=100 m–upper limit).
- OM fields: OM_10-20 and OM_20-30 described; dataset also indicates measurements across three depths (including 0–10 cm), to be mapped accordingly.
- File format: Excel workbook; NA cells indicate missing data.

## Data quality and notes
- Calibration procedures: None documented.
- Data checking/quality control: Not described.
- Documentation provides detailed site metadata and measurement methods, enabling cross-site comparisons while noting potential variability due to grazing and soil type.

## Practical notes for reuse
- Use site, habitat, and soil-type context to compare OM across clay (Essex) vs sandy (Morecambe Bay) soils and under different grazing regimes.
- Account for seasonal differences (Winter vs Summer, with an explicit Essex winter window in early March 2013).
- Handle missing data with NA values as indicated.
- Data are organized for grid-based quadrats with explicit scaling and quadrat numbering, useful for spatial analyses within and across sites.