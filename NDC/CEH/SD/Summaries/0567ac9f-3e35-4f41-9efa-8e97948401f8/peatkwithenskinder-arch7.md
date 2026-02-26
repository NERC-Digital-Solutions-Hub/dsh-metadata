# Collection methods

- Study area and sampling locations
  - Two peatland sites in the Peak District, northern England: Withens Clough (Withens) and Kinder Scout peatlands.
  - Gullies sampled at each site: W1, W2, W3 (Withens) and K1, K2, K3 (Kinder).
  - Exact coordinates provided for each gully (W1: 53.4250, -1.8749; W2: 53.4246, -1.8754; W3: 53.4236, -1.8763; K1: 53.4032, -1.8918; K2: 53.4030, -1.8911; K3: 53.4014, -1.8898).

- Sampling design
  - At each gully, samples collected next to a gully dam (dammed area) and at a downstream, undammed area for comparison.
  - Sampling positions relative to gully edge: at the edge (0 m), 1 m from the edge, and 5 m from the edge.
  - Depths and sampling points:
    - At gully edge: 5 cm depth sample from surface; 40 cm and 80 cm depth samples from the gully face.
    - At 1 m and 5 m distances: samples from 40 cm and 80 cm depths.

- Timeframe
  - Sampling conducted between December 2021 and January 2022.
  
- Laboratory methods and measurement
  - Samples transported to the University of Leeds Geography laboratories.
  - Hydraulic conductivity (K) measured using a split cylinder method (for smaller samples to capture fine-scale variation).
  - Process: saturated samples, Mariotte regulator to create a hydraulic gradient, measurement of flow rate to compute K.
  - K calculation uses Darcy's law: K = (Q / A) × (ΔL / ΔH), with Q as flow rate, A cross-sectional area, ΔL sample length, ΔH head difference.
  - Three measurements per sample; reported value is the mean of the three.

- Data structure and units
  - Columns:
    - Area: Withens or Kinder
    - Gully: W1, W2, W3 (Withens) or K1, K2, K3 (Kinder)
    - Location: Block (near dam feature) or Down (near open gully area)
    - Distance from gully edge: 0 (edge), 1 (1 m in), 5 (5 m in)
    - Depth: 5, 40, or 80 (mid-point depths in cm)
    - K: Saturated hydraulic conductivity (cm/s), numeric
  - Recorded unit for K: centimetres per second (cm/s)

- Quality control
  - All laboratory work conducted at the University of Leeds.
  - For each sample, three flow-rate measurements were taken; the mean of these three is reported.