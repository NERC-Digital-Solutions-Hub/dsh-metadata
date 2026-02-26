# Dry weight root biomass from three soil depths on salt marsh sites at Morecambe Bay and Essex.

- A dataset of root biomass (kg DW m^-2) across three soil depths (0-10 cm, 10-20 cm, 20-30 cm) for saltmarsh quadrats at six sites in Essex and Morecambe Bay.
- Part of the CBESS field campaign (Winter and Summer 2013); Essex winter samples collected additionally in March 2013. No planned repeats.

## Spatial and Temporal Coverage

- Sites:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Coordinates (representative):
  - Essex: AH 51°47'N, 0°52'E; FW 51°49'N, 0°58'E; TM 51°41'N, 0°56'E
  - Morecambe Bay: CS 54°10'N, 3°0'W; WS 54°8'N, 2°48'W; WP 54°9'N, 2°58'W
- Habitat context: contrasting soil types (Essex clay; Morecambe Bay sandy); varying inundation, creek structure, and grazing regimes.
- Sampling windows: Winter and Summer 2013; Essex winter samples additionally 2–6 March 2013.
- Locations are within saltmarsh zones (low, mid, high) across site rectangles 400×500 m to 1000×1000 m.

## Data Content and Structure

- Observed/derived variable: Root biomass (kg DW m^-2) for depth bands 0-10 cm, 10-20 cm, 20-30 cm; total 0-30 cm biomass calculated as sum.
- Data format: CSV.
- Dataset fields (selected):
  - Season (Winter or Summer)
  - Location (Morecambe or Essex)
  - Site (CS, WS, WP or AH, FW, TM)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat Number (1–22)
  - Scale (A–D) describing spatial arrangement:
    - A = 1 quadrat
    - B = 3 quadrats 1–10 m apart
    - C = 6 quadrats (10–100 m apart)
    - D = 100 m to upper limit
  - RB_0-10, RB_10-20, RB_0-30 (kg DW m^-2)
  - RB_0-30 (Total root biomass 0-30 cm)
  - Row Number and other descriptive fields
- Site rectangle context: Each site comprises a rectangular saltmarsh area; 22 1×1 m quadrats per site rectangle are randomly allocated across four spatial scales.

## Sampling Design and Methods

- Core sampling: One large sediment core (16 cm diameter, 30 cm depth) per 1×1 m quadrat, including soil, intact roots, and above-ground vegetation.
- Depth partitioning: Roots sorted into 0-10 cm, 10-20 cm, 20-30 cm; roots dried at 60°C for 72 hours and weighed.
- Data conversion: From kg DW per core area to kg DW m^-2.
- Quadrat allocation: 22 quadrats per site rectangle, randomly allocated using R (R Development Core Team, 2014) across four spatial scales.
- Quality checks: Readings entered into spreadsheets; outliers checked. Missing data indicated by blank cells.
- Calibration: Scales/calibration performed according to laboratory protocols as applicable.

## Data Quality, Provisos, and Documentation

- QA steps included data entry verification and outlier checks.
- Missing data noted as blank cells due to sample loss during processing.
- Field descriptions and header metadata provided to support interpretation and reuse.

## Data Formats and Field Descriptions

- File format: Comma separated values (.csv).
- Key fields include:
  - Season, Location, Site, Habitat, Quadrat Number
  - Scale (A–D) with corresponding descriptive text
  - RB_0-10, RB_10-20, RB_0-30 (and total RB_0-30)
  - Row Number and related metadata
- Notes: Total Root biomass (0-30 cm) is the sum of the three depth-specific measurements.

## GIS and Map-Ready Use Considerations

- Suitable for creating depth-resolved and total root biomass maps across saltmarsh sites.
- Can be joined to site polygons or site-rectangle extents, using provided site identifiers and coordinates.
- Useful for analyzing spatial patterns across soil types (clay vs. sandy) and grazing regimes, and for cross-site comparisons.
- Four spatial scales enable multiscale spatial analysis and sampling design evaluation.
- Be mindful of missing data and the specific sampling windows (March 2013 for Essex winter data) when integrating with other time-series datasets.