# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) plant height on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset measuring plant height on salt marsh sites in Morecambe Bay and Essex as part of CBESS.
- Ten direct measurements of plant height within each 1m x 1m quadrat.
- Staff responsible: Hilary Ford.
- Data collection occurs during Winter and Summer 2013.

## Data Scope and Content
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) with specified coordinates.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) with specified coordinates.
- Site descriptions:
  - Essex sites: contrasting clay soils, hare grazing; heavy grazing by Brent geese at Abbotts Hall and Fingringhoe Wick.
  - Morecambe Bay sites: contrasting sandy soils; heavier sheep grazing and winter grazing by pink-footed geese; one site (West Plain) lightly grazed.
- Observational period: Winter and Summer 2013 as part of a general field campaign.
- Measured variables:
  - Primary: Plant height (cm).
  - Derived per quadrat: Standard deviation (SD), Standard error (SE), Coefficient of variation (CoV).
- Data format: Excel workbook.

## Methods and Procedures
- Sampling design: Ten direct measurements of plant height per 1m x 1m quadrat, taken randomly within each quadrat using hand and meter rule.
- Calibration: None reported.
- Data quality and processing:
  - CoV calculated as (SD/Mean) × 100 to provide a vegetation height diversity score.
  - No explicit data quality control procedures described.

## Dataset Structure and Field Descriptions
- Primary fields:
  - Row Number (sorting index).
  - Season (Winter W or Summer S).
  - Location (Morecambe M or Essex E).
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex).
  - Habitat (Mudflat MF or Saltmarsh SM).
  - Quadrat Number (1–22).
  - Scale (A, B, C, D representing spatial extents).
  - Height measurements: H1–H10 (cm) for the ten measurements.
  - Mean Height (cm) across H1–H10.
  - SD (of H1–H10).
  - SE (of H1–H10).
  - CoV (of H1–H10).
- Field definitions emphasize:
  - Location and site codes, habitat type, and quadrat numbering.
  - Height-related metrics and derived statistics for each quadrat.

## Location, Context, and Metadata
- Spatial context emphasizes two contrasting salt marsh regions (Essex vs. Morecambe Bay) with differing soils, inundation, and grazing regimes.
- Metadata reflects:
  - Seasonal context (Winter/Summer).
  - Site-level descriptors and habitat type.
  - Measurement methodology and units (centimeters).
  - Data structure designed for multi-measurement per quadrat analysis.

## Data Quality, Access, and Stewardship Implications for Data Leaders
- Stewardship:
  - Dataset linked to CBESS with a named staff contact (Hilary Ford).
  - Clear documentation of locations, habitats, and measurement protocol.
- Data quality considerations:
  - Explicit quality control procedures are not described; potential gaps in QC and data validation.
  - Calibration is noted as none, which may affect cross-study comparability if measurement practices differ.
  Data format is Excel, which supports accessibility but may require governance around versioning and long-term preservation.
- Discoverability and reuse:
  - Comprehensive field descriptions and site-level context aid discoverability.
  - Metadata could be enhanced with data standards alignment (e.g., standardized field names, units, and controlled vocabularies) to improve interoperability across CBESS datasets and external data partners.
- Strategic implications:
  - The dataset supports analysis of vegetation height diversity (via CoV) and spatial comparisons between sites with different soils and grazing regimes.
  - Useful for assessing ecosystem service indicators related to vegetation structure, with potential integration into broader data networks and data-sharing workflows.
  - Highlights the need for explicit data quality controls, metadata completeness, and clear data access/licensing to strengthen governance and reuse across networks.