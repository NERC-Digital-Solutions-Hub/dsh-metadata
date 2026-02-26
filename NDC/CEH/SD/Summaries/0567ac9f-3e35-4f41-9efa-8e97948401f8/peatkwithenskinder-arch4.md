# Collection methods

- Sites and sampling locations
  - Two peatland sites in the Peak District, northern England: Withens Clough (Withens) and Kinder Scout (Kinder).
  - At each site: three peatland gullies (W1, W2, W3 for Withens; K1, K2, K3 for Kinder) with specified coordinates.
  - Sampling included gully-edge areas near a gully dam (restoration feature) and comparison areas further down the gully not influenced by the dam.

- Sampling design and depth/positioning
  - Sampling positions relative to gully edge: at edge (0), 1 metre from edge, and 5 metres from edge into the peat mass.
  - Depths at which peat was sampled: 5 cm, 40 cm, and 80 cm (mid-point depths).
  - Sampling methods by position/depth:
    - 5 cm depth: surface sampling using a 10 cm x 10 cm x 10 cm box corer.
    - Gully edge samples for 40 cm and 80 cm depths: box corer applied at the gully face.
    - 1 m and 5 m positions: 40 cm and 80 cm depths sampled with a 1 m long, 110 mm diameter tube corer.
  - For each depth, a 10 cm sample was collected, centered around the mid-point depth.

- Sampling period
  - December 2021 to January 2022.

- Laboratory measurements
  - Hydraulic conductivity (K) measured in the University of Leeds School of Geography laboratories using a split cylinder method.
  - Process: peat sample thawed from a frozen cube, enclosed in an acrylic split-cylinder with silicone grease or petroleum jelly to prevent preferential flow, saturated with site water, and a Mariotte regulator applied to establish a hydraulic gradient.
  - Calculation: K = (Q / A) × (ΔL / ΔH), where
    - Q = flow rate through the sample
    - A = cross-sectional area of the sample
    - ΔL = sample length
    - ΔH = head difference across the sample
  - Unit for K: centimetres per second (cm/s).

- Quality control and data processing
  - For each sample, three measurements were taken; the mean of the three flow rates was reported as the dataset value.

- Data structure and fields
  - Area: Withens or Kinder
  - Gully: W1, W2, W3, K1, K2, K3 (W indicates Withens site, K indicates Kinder site)
  - Location: Block (near the gully dam) or Down (near open gully area)
  - Distance from gully edge: 0 (edge), 1 (1 metre from edge), 5 (5 metres from edge)
  - Depth: 5, 40, or 80 (mid-point depths in cm)
  - K: numeric value of saturated hydraulic conductivity (cm/s)