# Collection methods

## Overview and sites
- Two peatland sites in the Peak District, northern England: Withens Clough (Withens) and Kinder Scout (Kinder).
- At each site: three peatland gullies (W1–W3 for Withens; K1–K3 for Kinder) with provided coordinates.
- Sampling conducted next to a gully dam (influence of dam feature) and at a downstream open area for comparison.
- Sample locations include peat at the gully edge, 1 m from the edge into the peat mass, and 5 m from the edge.
- Coordinates for sampling points documented, enabling geo-referencing of sample locations.

## Sampling scheme and depths
- At each sample point, peat was collected at three depth ranges with midpoints at 5 cm, 40 cm, and 80 cm.
- Depth-specific sampling methods:
  - 5 cm depth near the surface: 10 cm × 10 cm × 10 cm box corer.
  - 40 cm and 80 cm depths near the gully edge: 1 m long, 110 mm diameter tube corer.
- Sampling occurred between December 2021 and January 2022.

## Hydraulic conductivity measurement (K)
- Conducted in the laboratory at the School of Geography, University of Leeds.
- Method: split cylinder technique (modified from the cube method) allowing small samples and reducing preparation time.
- Sample preparation: peat cores cut from frozen peat, thawed, enclosed in an acrylic split-cylinder, with inner silicone grease or petroleum jelly to prevent preferential flow.
- Saturation: samples saturated with site water; a Mariotte regulator provides hydraulic head difference to drive flow.
- Computation: hydraulic conductivity K calculated via Darcy’s law adapted for the setup:
  - K = (Q / A) × (ΔL / ΔH)
  - Q = flow rate through the sample
  - A = cross-sectional area of the sample
  - ΔL = sample length
  - ΔH = hydraulic head difference
- Recorded units: saturated hydraulic conductivity in centimetres per second (cm/s).

## Quality control
- All lab work conducted in Leeds.
- For each sample, three measurements were taken; a mean value of the three flow rates was calculated and reported as the dataset value.

## Data structure, units, and fields
- Data structure is organized in columns with the following fields:
  - Area: coded as 'Withens' or 'Kinder'
  - Gully: coded as W1, W2, W3 (Withens) or K1, K2, K3 (Kinder)
  - Location: 'Block' (adjacent to gully dam feature) or 'Down' (adjacent to open gully area)
  - Distance from gully edge: '0' (at edge), '1' (1 m from edge), or '5' (5 m from edge)
  - Depth: '5', '40', or '80' (mid-point depth in cm)
  - K: numeric value of saturated hydraulic conductivity (cm/s)
- K values represent three-measurement means per sample as the reported dataset value.

## Temporal coverage
- Sampling and measurements conducted from December 2021 to January 2022.