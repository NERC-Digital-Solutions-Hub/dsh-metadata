# Coastal Biodiversity Ecosystem Service Sustainability (CBESS) the erosion rate of sediment cores from salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset measuring erosion rate of sediment cores from salt marsh sites in Morecambe Bay and Essex.
- Core description: 16 cm diameter, 30 cm height, placed in a flume tank to measure % mass loss per hour under three flow conditions.

## Scope and locations
- Sites in Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Sites in Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat context: saltmarsh with contrasting soils (clay in Essex; sandy in Morecambe Bay) and differing inundation, creek structure, and vegetation.
- Grazing regimes varied by site (Essex heavily grazed by geese; Morecambe Bay variable grazing).

## Data collection and methods
- Campaign timing: Winter and Summer 2013, with an additional Essex sampling window (2–6 March 2013).
- Protocol: one large core per 1 m x 1 m quadrat; vegetation cover recorded; cores analyzed in Bangor University’s School of Ocean Sciences.
- Erosion measurement: mass loss over 30 minutes used to derive rate; measurements at 0, 5, 10, 15, and 30 minutes.
- Calibration: stagnation pressures for flow levels—low 61 Pa, medium 146 Pa, high 351 Pa.
- Procedures noted as field/lab activities; no explicit data checking procedures described.

## Variables and data structure
- Primary measurements: % mass loss per hour at three flow levels
  - Low velocity (L_%massloss) = 1.0 m/s
  - Medium velocity (M_%massloss) = 1.6 m/s
  - High velocity (H_%massloss) = 2.2 m/s
- Dataset fields include: season (Winter/W), location ( Essex or Morecambe), site (AH, FW, TM, CS, WS, WP), habitat (Mudflat or Saltmarsh), Quadrat Number, Scale (A–D), and the three mass loss variables.
- Additional notes: >100% mass loss per hour is considered valid; low-flow results can be negative due to initial water saturation; some cores were destroyed at high flow; medium-flow results are generally more reliable for overall modeling.
- File format: Excel workbook.

## Data quality and caveats
- Data checks/quality control procedures not specified.
- Some measurements (especially at low flow) may be influenced by initial core saturation.
- Destruction of cores at high flow indicates limits to experimental conditions and sample integrity.
- Medium-flow results preferred for model calibration due to reliability.

## Access and governance
- Staff responsible: Hilary Ford.
- Data steward/affiliation: Bangor University, School of Ocean Sciences.
- Metadata and field descriptions exist within the dataset to support discoverability and reuse.

## Use and implications
- Suitable for erosion-rate modeling and assessment of sediment core erosion under varying hydrodynamic forces.
- Provides spatial (Essex vs. Morecambe Bay) and habitat-level context, useful for cross-site comparisons and understanding the influence of soil type and grazing on erosion dynamics.
- Important considerations for reuse: ensure proper handling of negative low-flow values, account for potential core destruction at high flow, and preferentially use medium-flow data for modeling purposes.