# Collection methods

## Study sites
- Two peatland sites in the Peak District, northern England: Withens Clough (Withens) and Kinder Scout (Kinder).
- At each site: three peatland gullies (Withens: W1–W3; Kinder: K1–K3) with specified lat/long coordinates.
- Sampling performed next to a gully dam (restoration feature) and at a comparison area downstream from the dam (unaffected by the dam).

## Sampling design
- Sample points: at the gully edge (0 m), 1 m from the edge, and 5 m from the edge into the peat mass.
- Depths sampled at each point: 5 cm, 40 cm, and 80 cm (mid-point depths).
- Extraction methods:
  - At the 5 cm depth (surface): 10 cm × 10 cm × 10 cm box corer.
  - At the gully edge for 40 cm and 80 cm depths: 1 m long, 110 mm diameter tube corer.
  - At 1 m and 5 m from the edge: 10 cm sample taken 5 cm either side of the mid-point depth.
- Sampling period: December 2021 to January 2022.

## Laboratory measurements and calculation of K
- Hydraulic conductivity (K) measured in the laboratory using a split cylinder method (adapted from the modified cube method).
- Process: peat saturated with site water; Mariotte regulator provides hydraulic head difference; drainage tube on the opposite end to create a gradient.
- Calculation: K = (Q / A) × (ΔL / ΔH), where Q is flow rate, A is cross-sectional area, ΔL is sample length, ΔH is head difference.
- Units: saturated hydraulic conductivity reported in centimetres per second (cm/s).
- Method advantages: avoids paraffin wax, enabling smaller peat samples to be analyzed for fine-scale K variation; internal lubrication uses silicone grease or petroleum jelly to prevent preferential flow.

## Data quality control
- For each sample, three measurements were taken; a mean of the three flow rates is reported as the dataset value.
- All work conducted at the School of Geography, University of Leeds.

## Data structure and fields
- Data are organized in columns:
  - Area: Withens or Kinder
  - Gully: W1, W2, W3, K1, K2, K3
  - Location: Block (near the dam) or Down (near open gully area)
  - Distance from gully edge: 0 (edge), 1 (1 m inside), 5 (5 m inside)
  - Depth: 5, 40, or 80 (mid-point depth in cm)
  - K: numeric saturated hydraulic conductivity value (cm/s)