# Coastal biodiversity and Ecosystem Service Sustainability (CBESS) total organic carbon in mudflat and saltmarsh habitats.

## Overview
- Dataset measuring total organic carbon in mudflat and saltmarsh habitats as part of CBESS.
- Based on Loss on Ignition (LOI) analyses of sediment samples.
- Spatial and temporal scope: 6 sites across 2 locations (Essex and Morecambe Bay), 2 habitats, winter and summer 2013.
- Sampling design: 3 replicates across 22 quadrats, across 4 spatial scales.
- Staff: Christina Wood and Martin Solan.
- Primary data format: CSV with a detailed field dictionary.

## Dataset composition and scope
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitats: Mudflat (MF) and Saltmarsh (SM)
- Temporal coverage: Winter (W) and Summer (S) 2013
- Sampling intensity: 6 sites, 3 replicates per site, 22 quadrats per site
- Resolution scales (as per metadata): A (1 m), B (1–10 m), C (10–100 m), D (100 m to upper limit)

## Location and mapping details
- Site codes and locations are provided to support GIS integration:
  - Essex: AH, FW, TM
  - Morecambe Bay: CS, WS, WP
- Spatial references are embedded via site and habitat identifiers, enabling mapping of carbon-related metrics by location, habitat type, and scale.

## Variables and measurements
- Primary measurement: Organic carbon content via LOI.
- Key data fields include:
  - Row Number, Replicate, Quadrat Number (1–22), Season (Winter/Summer), Location (Essex/Morecambe), Site (AH, FW, TM, CS, WS, WP), Habitat (Mudflat/Saltmarsh), Scale (A–D)
  - Measurement Type: LOI
  - Weight measurements at various temperatures (Cr, Cr+Sed, etc.) for ignition steps (105°C, 400°C, 480°C, 950°C)
  - Dry and wet weights, Loss on Ignition (LOI) values
  - %Water, %Carbohydrate, %Total Organic, %Carbon, %CO2, wtCaCO3, %CaCO3, %Mineral Residue
- Data dictionary includes units and formats for each field (e.g., grams, percentages, text for seasons/locations)

## Data collection and quality control
- Field sampling: Mudflats – surface sediment scrapes; Saltmarsh – sediment cut from 2 cm below surface.
- Sample handling: Samples frozen at -20°C and analyzed using standard LOI procedure.
- Calibration and QA: Procedures and references available through the LOI techniques page (Calibrations/QA described on the linked Cambridge lab page).
- Data checks: LOI methodology and QA procedures referenced in metadata; explicit NA values used where data are not available.

## Data formats and accessibility
- Primary file format: .csv
- Dataset includes a comprehensive data dictionary (field descriptions, formats, and category codes) to support GIS joins and attribute queries.
- Additional references: LOI technique documentation linked in metadata for reproducibility.

## GIS-focused guidance and use cases
- Suitable for creating map-based visualisations of organic carbon distribution by site, habitat, and scale.
- Can be joined with site shapefiles (points/polygons) to visualise spatial patterns of carbon content and related components (e.g., %Total Organic, %CaCO3).
- Scales A–D enable multi-resolution mapping analyses, from fine 1 m extents to broader 100 m- scale assessments.
- Useful for comparing sediment types across contrasting habitats and regions (Essex vs. Morecambe Bay) and for ecosystem service assessments related to carbon content.

## Considerations for integration and reuse
- Temporal limitation: Data from a single campaign (Winter/Summer 2013) with no planned repeats; consider for baselining rather than trend analysis.
- Data availability: Consolidated within a CSV, but cross-referencing other CBESS datasets may require harmonisation of field codes and scales.
- Data quality: LOI-based carbon content relies on standard methodologies; refer to the LOI page for detailed procedures and calibrations.

## Provenance and contacts
- Staff responsible: Christina Wood; Martin Solan
- For methodological details and QA references, see the LOI technique page linked in metadata.