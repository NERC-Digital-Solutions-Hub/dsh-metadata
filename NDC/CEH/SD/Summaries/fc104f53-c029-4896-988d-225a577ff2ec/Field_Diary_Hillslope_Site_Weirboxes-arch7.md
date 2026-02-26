# Weir boxes measuring drain and overland flow in the bowl

## Overview
- This file documents the two weir boxes used to measure drain flow (DRAIN) and overland flow (OLF) in the bowl.
- Installed on 01/11/06.
- Includes installation notes, measurement details, maintenance events, and data quality issues observed during monitoring.

## Measurements and specifications
- V-notch positions:
  - DRAIN flow weir box: approximately 23.33 mm above the V-notch.
  - OLF weir box: approximately 106 mm below the V-notch.
- V-notch and water-depth observations:
  - The V-notch length varied by about 9 mm between sides; average V length around 212.5 mm (DRAIN) and 211 mm (OLF).
  - Coefficient of variation (CV): 2.99% (DRAIN) and 1.3% (OLF).
  - Water depth at the edge during downloads: about 112 mm.
  - Depth of water above the V-notch (based on average V length): about 37.3 mm for DRAIN.
- Internal area (used for flow calculations):
  - DRAIN weir box internal area: ~0.520384 m^2 (75.2 cm × 69.2 cm).
  - OLF weir box internal area: ~0.517242 m^2 (approx. 74.5 cm × 69.1 cm, with similar dimensions to the drain).
- Notes on measurements:
  - Observations sometimes indicated potential partial blockages or misalignment affecting recorded levels.
  - Evaporation observed later causing water level to drop below the V-notch in some periods.

## Data collection timeline and maintenance
- 01/11/06: Installation of the two weir boxes.
- 08/11/06: DRAIN ~23.33 mm above V-notch; OLF ~106 mm below V-notch recorded.
- 14/11/06 – 23/11/06: OLF weir box leaking; removed and later reinstalled; wiring and transducer checks.
- 27/11/06 – 29/11/06: Data issue (drain flow problem; loose wire fixed); OLF reinstalled; water level set to zero at restart.
- 06/12/06 – 08/03/07: Wiring issues suspected on s'belt weir box; ongoing monitoring.
- 08/03/07 – 29/03/07: OLF guiding plastic extended; later noted a data gap caused by logger battery handling during download.
- 14/11/07 – 12/12/07: Additional blockages and sediment management; OLF gutter occasionally blocked; down pipe clear.
- 23/01/08 – 30/01/08: Data considered too low for observed overland flow; suspected blockage; down pipe/OLF gutter cleared.
- 03/03/08 – 13/03/08: Gap in data; download on 13/03/08 showed repeated data from prior file.
- 30/07/08 – 15/08/08: Data jump/gap observed following last download.

## Data quality issues and actions
- Leakage and hardware integrity:
  - OLF weir box leak detected (Nov 2006); box removed, dried, and repaired.
  - Wiring issues noted for both DRAIN/OLF-related equipment; repairs attempted (Dec 2006 – Mar 2007).
- Blockages and sediment:
  - Blockages in downpipes and OLF gutter observed (late 2007–early 2008); gutters cleared.
  - Mole/vole activity caused soil disturbance around the Hillslope OLF trap (Apr–May 2007).
- Evaporation and environmental effects:
  - Evaporation caused the water level to drop below the V-notch in Apr 2007.
- Data integrity and continuity:
  - Occasional data gaps and suspicious data (Mar 2008) suspected due to logger handling and software issues.
  - Noted data jumps/gaps between late 2007 and Aug 2008.
- Observational validation:
  - Discrepancy between small recorded overland flow and higher field observations suggested possible blockages or data loss (Jan 2008).

## Observations and notes relevant to GIS use
- The physical dimensions and V-notch positions are critical for converting stage readings to flow estimates; minor misalignment (9 mm V-length discrepancy) can affect accuracy.
- Data quality issues (leaks, blockages, evaporation, and logger handling) can introduce gaps or biases; these should be accounted for in any GIS-based temporal analyses.
- Regular maintenance events (reinstalls, gutter clearances, and wiring fixes) correspond to periods of potential data discontinuity; metadata should annotate these intervals for accurate time-series visualization.
- Internal area metrics enable consistent flow calculations across both weir boxes, important for standardized GIS analyses and cross-site comparisons.