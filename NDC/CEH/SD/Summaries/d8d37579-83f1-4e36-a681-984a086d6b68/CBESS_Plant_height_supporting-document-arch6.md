# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) plant height on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset capturing plant height measurements on salt marsh sites as part of CBESS.
- Focuses on comparing two coastal regions: Morecambe Bay (west UK) and Essex (south-eastern Atlantic UK).
- Aims to support exploration of biodiversity and ecosystem service relationships through measurable plant height and diversity metrics.

## Data collection and scope
- Staff responsible: Hilary Ford.
- Monitoring period: Winter and Summer 2013.
- Observation locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Coordinates are provided for each site.
- Site characterization:
  - Essex sites represent clay soil saltmarsh with higher grazing pressure (hare grazing; Brent geese).
  - Morecambe Bay sites represent sandy soil saltmarsh with grazing by sheep and geese; grazing intensity varies by site.
- Data collection context:
  - Saltmarsh sites chosen to reflect contrasting soils, inundation frequency, creek structure, and vegetation types.

## Sampling method and structure
- Plot design: 1m x 1m quadrats; ten direct plant height measurements per quadrat.
- Quadrats numbered 1–22 per dataset location.
- Measurement approach: height measured in centimeters using hand and meter rule.

## Variables and calculations
- Primary measurements: Plant height (H1–H10, cm) for each quadrat.
- Derived and ancillary metrics:
  - Mean Height (cm) computed from H1–H10.
  - Variability metrics for each quadrat: SD, SE, CoV (coefficient of variation).
  - CoV used as a vegetation height diversity score (higher values indicate greater height diversity).
- Categorical descriptors:
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe (CS, WS, WP) or Essex (AH, FW, TM).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).

## Data structure and format
- File format: Excel workbook.
- Dataset fields (high level):
  - Row Number; Season; Location; Site; Habitat; Quadrat Number.
  - H1–H10 (10 height measurements per quadrat).
  - Mean Height (cm); SD; SE; CoV.
  - Scale codes (A–D) indicating measurement ranges and context for height data.

## Quality control and documentation
- Data checking procedures: Not explicitly documented.
- Calibration: None reported.
- Additional descriptive field mappings provided (Dataset Field Descriptions) to support data use and interpretation.

## Potential uses and insights
- Compare vegetation height and height diversity across Essex and Morecambe Bay saltmarshes.
- Assess influence of soil type and grazing regimes on plant height metrics.
- Integrate with broader CBESS datasets to explore relationships between height diversity and ecosystem services or biodiversity indicators.
- Create self-serve tools (e.g., dashboards) to enable end users to explore height data by site, season, and habitat.

## Considerations for use
- Time-bound data (Winter/Summer 2013); may require augmentation for broader temporal coverage.
- 22 quadrats per site provide within-site resolution; cross-site comparisons should account for site-specific grazing and environmental differences.
- Data are stored in Excel; ensure compatibility with analysis workflows.