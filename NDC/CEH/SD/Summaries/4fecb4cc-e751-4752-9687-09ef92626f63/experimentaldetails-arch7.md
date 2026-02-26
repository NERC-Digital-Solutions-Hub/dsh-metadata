# Preliminary Investigation on the Interaction Between Turbulence and Biofilms Using Particle Image Velocimetry

## Overview
- A preliminary study to understand how turbulence affects biofilms, using particle image velocimetry (PIV) to obtain spatially and temporally resolved velocity fields in water across different flow configurations.
- Aims to relate flow features to biofilm development and dynamics.

## Experimental Channel Design and Biofilm Setup
- Custom flow facility with four sections: flow conditioner, developing section, test section, and diffuser.
- Permeable bed made from an array of acrylic rods spanning channel width, enabling two porosities: 35% and 45%.
  - Higher porosity (45%) achieved with 6.3 mm rods in a square array.
  - Lower porosity (35%) achieved by adding central 3.2 mm rods, reducing porosity by ~10%.
- Flow conditioner reduces incoming turbulence using perforated sheet and screens; a 2D contraction section provides an 8:1 height ratio.
- Biofilm developed on a 30 cm permeable bed, then moved to the test section for flow experiments.
- Flow rate controlled via pump frequency; measured with an insertion electromagnetic flow meter.

## PIV Setup and Measurement Geometry
- PIV system: dual-head pulsed Evergreen Nd:YAG laser (~200 mJ/pulse) creates ~1 mm laser sheet illuminating seeding particles in the x–y plane.
- Imaging: 16-bit, 5.5 MP sCMOS camera (2560 × 2160), ~6.5 μm pixel size; Navitar long-distance microscope (NA ~0.012; ~0.25× objective, 2× adapter, ~2× zoom).
- Field of view: approximately 18 × 15 mm².
- Experimental section containing biofilm is 30 cm long; flow experiments conducted in the test section with flow rate varied by pump speed.
- Data collected at four different pump frequencies per experiment.

## Experimental Conditions (17 Experiments)
- Each experiment name corresponds to a results file numbered 1–17, with the following varying factors:
- Porosity and biofilm presence vary as follows (grouped by porosity and biofilm status):
  - Porosity 35% (experiments 1–3): no biofilm; pump frequencies 8, 16, 30 Hz.
  - Porosity 45% (experiments 4–9): biofilm present; pump frequencies 8, 16, 30 Hz (plus a 4 Hz-like condition in one instance).
  - Porosity 45–35% (experiments 10–13): no biofilm; developing section porosity 45% and test section porosity 35%; pump frequencies 4.5, 8, 16, 30 Hz.
  - Porosity 45% (experiments 14–17): biofilm present; pump frequencies 4.5, 8, 16, 30 Hz.
- Biofilm presence toggled between Y/N across experiments to compare flow with and without biofilm under varying porosities and flow rates.

## Measured Variables (per experiment)
- Y = distance from top of the cylinder.
- U = mean streamwise velocity; V = mean wall-normal velocity.
- u', v' = fluctuating velocity components; u'u', u'v', v'v' = Reynolds stress components.
- Omega = mean vorticity; omega_rms = RMS of vorticity fluctuations.
- Lci = mean swirling strength; lci_rms = RMS of fluctuating swirling strength.

## GIS-Relevant Implications for Data Visualization
- The study produces spatially and temporally resolved velocity fields and derived metrics (vorticity, swirling strength, Reynolds stresses) suitable for map-like visualization.
- Potential data products for GIS workflows:
  - Vector fields of U and V across the measurement plane for each experiment.
  - Scalar fields of vorticity, swirling strength, and Reynolds stresses.
  - Overlay of biofilm presence (Y/N) and bed porosity geometry to compare flow-biofilm interactions.
  - Time-resolved or frequency-variant visualizations across the four pump frequencies.
- Useful for layering experimental flow data onto geometries representing bed porosity and biofilm regions, enabling spatial analyses and policy/client-facing map visualisations.

## Data Handling and Reproducibility Considerations
- Data are organized into 17 result files corresponding to distinct experimental conditions.
- High-resolution 2D flow data with explicit documentation of porosity, biofilm status, and pump frequency facilitates cross-experiment comparisons.
- Consistency in measurement plane orientation and coordinate definitions is essential for integrating datasets into map-based analyses.