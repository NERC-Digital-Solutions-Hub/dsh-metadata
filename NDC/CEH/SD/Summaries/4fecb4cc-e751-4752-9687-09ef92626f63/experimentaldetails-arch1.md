# Purpose of study

- Objective: A preliminary investigation into how turbulence interacts with biofilms using particle image velocimetry (PIV) to obtain spatially- and temporally-resolved velocity fields in water for different flow configurations.

## Experimental setup

- Flow facility design: Four sections
  - Flow conditioner with a perforated plastic sheet (4.8 mm thickness, 4.8 mm holes, 32% open area) and three screens to reduce incoming turbulence; two-dimensional contraction (inlet:outlet height ratio 8:1).
  - Developing section (1 m) to ensure fully developed flow in the 50 cm test section; side/top glass windows for optical access.
  - Test section.
  - Diffuser.
- Permeable bed geometry:
  - Regular array of acrylic rods spanning channel width, spanning both developing and test sections (each 30 cm long).
  - Two porosities: 35% and 45%.
  - Higher porosity: 1/4" (6.3 mm) rods in a square array; lower porosity: add 1/8" (3.2 mm) rods at the center of each square cell to reduce porosity by ~10%.
- Flow control and measurement:
  - Flow rate controlled by pump frequency; measured with an insertion electromagnetic flow meter (SeaMetrics EX810P) on a 1.5" PVC pipe.
- PIV and optical setup:
  - Dual-head, pulsed Nd:YAG laser (~200 mJ/pulse) to create a ~1 mm-thick laser sheet in the x-y plane.
  - 16-bit, 5.5 MP camera (2560 × 2160) with Navitar long-distance microscope (NA ~0.012) and ~2× zoom; field of view ~18 × 15 mm.
  - Biofilm developed on a 30 cm permeable-bed section; this biofilm-covered section placed in the test section for flow experiments.

## Experimental design and boundary conditions

- Total experiments: 17 distinct experiments.
- Variables varied across experiments:
  - Biofilm presence: Y/N (biofilm on in some runs).
  - Pump frequency: 4.5 to 30 Hz (four frequencies used per setup).
  - Bed porosity: 35% or 45% (with some tests using a 45% developing section and 35% test section configuration).
- Example configuration patterns:
  - Experiments 1–3: biofilm off; porosity 35%; pump frequencies 8, 16, 30 Hz.
  - Experiments 4–9: biofilm on; porosity 45%; pump frequencies 8, 16, 30 Hz and additional frequencies down to 4.5 Hz.
  - Experiments 10–13: biofilm off; porosity 45%–35% combined; biofilm not present.
  - Experiments 14–17: biofilm on; porosity 45%; pump frequencies 4.5, 8, 16, 30 Hz.
- Across developing and test sections, some 45% porosity in developing and 35% in test sections in certain runs.
- Data collection: Each experiment file is numbered 1 through 17 with corresponding setup details in the run notes.

## Measured variables and data structure

- Measured variables (per file):
  - Y: Distance from the top of the cylinder.
  - U: Mean streamwise velocity.
  - V: Mean wall-normal velocity.
  - u', v': Fluctuating velocity components (downstream and vertical).
  - Reynolds stresses: u'u', u'v', v'v'.
  - Omega: Mean vorticity.
  - omega_rms: RMS of vorticity fluctuations.
  - Lci: Mean swirling strength.
  - lci_rms: RMS of fluctuating swirling strength.
- Data organization:
  - 17 separate result files corresponding to the 17 experimental conditions, documenting the presence or absence of biofilm, bed porosity, and pump frequency.