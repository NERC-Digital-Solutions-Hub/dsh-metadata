# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil organic matter content from three soil depths on saltmarsh sites at Morecambe Bay and Essex

## Overview
- Dataset measuring soil organic matter (OM) content (%), obtained via loss-on-ignition (LOI) from bulk density samples.
- Focused on saltmarsh sites in Essex and Morecambe Bay, collected during Winter and Summer 2013 (with additional Essex winter sampling 2–6 March 2013).
- Depths sampled: 0–10 cm, 10–20 cm, 20–30 cm.
- Contextual notes include grazing regimes and vegetation differences between sites.

## Spatial coverage
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Coordinates provided for each site (approximate lat/long in degrees and minutes). Sites reflect contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation frequency, creek structure, and dominant vegetation.
- Site-level habitat types include saltmarsh and mudflat; grazing intensity varies by site (heavily grazed by geese/sheep in some locations; lightly grazed in others).

## Sampling design and methods
- Field campaign carried out in Winter and Summer 2013; Essex winter samples collected in a separate window (2–6 March 2013).
- OM determined from bulk density samples; bulk density rings used (3.1 cm height, 7.5 cm diameter) at three depths per quadrat.
- Sample prep: soils dried at 105°C for 72 hours; sub-samples dried at 375°C for 16 hours to determine OM%.
- Additional dataset details cover calibration, QA, and data checking procedures (not exhaustively specified here).

## Data structure and content
- File format: Excel workbook.
- Key fields and structure:
  - Row Number: sorting index.
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe – Cartmel Sands (CS), Warton Sands (WS), West Plain (WP); Essex – Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: Coded ranges (A = 1 m; B = 1–10 m; C = 10–100 m; D = 100 m and up).
  - OM_10-20: Soil organic matter (%) for the 10–20 cm depth (field name suggests 10–20 cm, though descriptions reference multiple depths).
  - OM_20-30: Soil organic matter (%) for the 20–30 cm depth.
  - NA cells indicate missing data.
- Indicates three depth-related OM fields (0–10 cm, 10–20 cm, 20–30 cm) within a structured quadrat-based sampling scheme across sites.

## File formats, access and metadata
- Primary data delivery as an Excel workbook.
- Data fields include season, location, site, habitat, quadrat, and depth-specific OM measurements.
- Metadata notes: locations and site descriptions, sampling windows, and grazing/vegetation context are included to aid interpretation and mapping.

## Data quality, limitations, and considerations for GIS
- Spatial precision: coordinates provided at site level; no explicit GIS-ready polygon footprints or CRS specified, so users may need to georeference points based on provided coordinates.
- Temporal scope: data from 2013 (Winter/Summer campaigns with an additional Essex winter window); time sensitivity to environmental conditions.
- Depth interpretation: OM measurements across three depth intervals; ensure consistency when mapping or aggregating (0–10 cm, 10–20 cm, 20–30 cm as applicable).
- Data completeness: some cells marked NA; presence of missing data should be handled in GIS analyses.
- Contextual factors: grazing intensity and vegetation differences across sites may influence OM distributions; consider incorporating habitat and grazing notes in GIS analyses to support interpretation.

## Practical GIS considerations and usage
- Map-ready attributes: location, site, habitat, season, quadrat, scale, and depth-specific OM values provide rich, multi-attribute layers for spatial analysis.
- Suitable GIS workflows:
  - Create point features for each quadrat with OM values per depth and associated metadata.
  - Use scale codes to derive neighborhood or transect-based analyses, or to aggregate data at different spatial extents.
  - Combine with site-level context (habitat type, grazing regime) to analyze drivers of OM variation.
  - Integrate with environmental layers (inundation frequency, vegetation cover) to explore spatial patterns.
- Data cleaning steps in GIS: handle NA values, verify coordinate syntax (convert degrees/minutes to decimal degrees if needed), and standardize depth field naming if consolidating multiple datasets.