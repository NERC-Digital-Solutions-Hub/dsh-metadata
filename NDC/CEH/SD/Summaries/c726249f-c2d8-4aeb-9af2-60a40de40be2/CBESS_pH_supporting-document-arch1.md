# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil pH on salt marsh sites at Morecambe Bay and Essex.

## Overview
- Dataset captures soil pH from salt marsh sites in Essex and Morecambe Bay as part of CBESS.
- Focus is on pH of 10 g soil samples from the top 5 cm within 1 m x 1 m quadrats.
- Sites represent contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation, habitat structure, and grazing regimes.

## Locations and Site Context
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Site descriptions highlight differences in soil type (clay vs. sand), inundation frequency, creek structure, and dominant vegetation.
- Grazing context:
  - Essex: hare-grazed; heavy grazing by over-wintering Brent geese at AH and FW.
  - Morecambe Bay: intensive sheep grazing at CS and WS; pink-footed geese grazing in winter; WP lightly grazed.

## Sampling Design and Timeline
- Sampling conducted during Winter and Summer 2013, with Essex winter samples collected in an extended sampling window (2–6 March 2013).
- Quadrat-based sampling within 1 m x 1 m plots; up to 22 quadrats per site (Quadrat Number 1–22).
- Scale categories used to denote spatial resolution: A (1 m), B (1–10 m), C (10–100 m), D (100 m onward).

## Measurements and Procedures
- Target variable: pH of soil.
- Field/lab protocol:
  - 10 g soil (fresh mass) mixed with 25 ml deionised water.
  - 1:2.5 dilution, shaken ~30 minutes.
  - pH measured with a Jenway 4320 pH/electrical conductivity probe.
  - pH values adjusted for ambient temperature.
- Calibration: None reported.
- Data collection was part of a broader field campaign with attention to recording exact site and habitat context.

## Data Structure and Formats
- Dataset fields include:
  - Row Number (1–N): sorting aid for original input order.
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: Morecambe – CS, WS, WP; Essex – AH, FW, TM.
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22.
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100 m and up).
  - pH: numeric value (adjusted for temperature).
- File format: Excel workbook.

## Quality and Meta-Data Notes
- Calibration procedures: None documented.
- Data checking/quality control procedures: Not specified in the dataset description.
- The dataset includes both raw sampling details (locations, habitats, grazing context) and the measured pH values, enabling context-sensitive analyses.