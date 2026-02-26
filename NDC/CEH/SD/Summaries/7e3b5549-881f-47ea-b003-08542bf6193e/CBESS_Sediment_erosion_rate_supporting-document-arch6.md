# Coastal Biodiversity Ecosystem Service Sustainability (CBESS) the erosion rate of sediment cores from salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset measuring erosion rate (% mass loss per hour) from sediment cores placed in a flume tank under three water flow forces (low, medium, high).
- Core data: 16 cm diameter, 30 cm height, collected from 1 m x 1 m quadrats; vegetation cover noted.
- Erosion rate derived from mass loss over 30 minutes, with measurements at 0, 5, 10, 15, and 30 minutes.

## Study sites and site characteristics
- Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM); clay soils; hare grazing; heavy over-wintering Brent geese grazing at AH and FW.
- Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP); sandy soils; grazing patterns include intensive sheep grazing and pink-footed geese; West Plain lightly grazed.

## Sampling campaign and timing
- General field campaign conducted Winter and Summer 2013.
- Essex winter samples collected during an additional window: 2–6 March 2013.

## Data collected and measurement protocol
- For each 1 m x 1 m quadrat, one core collected and placed in the flume for 1.5 hours with 0.5 hour exposure at each of three flow rates (low, medium, high).
- Erosion rate calculated from mass loss per hour using measurements at 0, 5, 10, 15, and 30 minutes.
- Attributes recorded include above-ground vegetation cover.
- Two entries (1 and 2) describe the same core sampling and erosion measurement procedures.

## Calibration and data quality
- Calibration: stagnation pressures set to low 61 Pa, medium 146 Pa, high 351 Pa.
- Data quality notes: mass loss per hour > 100 is considered valid; low-flow measurements can yield negative values due to initial water saturation; some high-flow cores were destroyed; medium-flow results are more reliable and recommended for overall erosion rate estimates.

## Data format and fields
- File format: Excel workbook.
- Key fields include:
  - Season (Winter/W, Summer/S)
  - Location (Essex or Morecambe)
  - Site (AH, FW, TM; CS, WS, WP)
  - Habitat (Mudflat MF; Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A–D representing 1 m, 1–10 m, 10–100 m, etc.)
  - L_%massloss (low velocity, % mass loss per hour at 1.0 m/s)
  - M_%massloss (medium velocity, % mass loss per hour at 1.6 m/s)
  - H_%massloss (high velocity, % mass loss per hour at 2.2 m/s)

## Data notes and interpretation
- % mass loss per hour values greater than 100 are valid.
- Negative values at low flow can occur due to initial water saturation of cores.
- Medium-flow results are the most reliable for modeling erosion rates.

## Potential data products and usage
- Dashboards or pivot tables to compare erosion rates by site, soil type, season, and grazing regime.
- Self-serve data access for researchers and policymakers to explore erosion under different hydrodynamic conditions.
- Documentation to support replication and reuse, including procedural notes and calibration details.

## Limitations and considerations
- High-flow experiments may destroy some cores, potentially biasing results toward remaining samples.
- No explicit data checking procedures recorded; some data treatment notes indicate None.