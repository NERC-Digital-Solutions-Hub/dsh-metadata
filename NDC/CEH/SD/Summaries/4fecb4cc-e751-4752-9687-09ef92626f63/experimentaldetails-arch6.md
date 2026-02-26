# Purpose of study

## Overview
- Preliminary investigation of turbulence–biofilm interaction using particle image velocimetry (PIV) to obtain spatially- and temporally-resolved velocity fields in water for different flow configurations.

## Channel design
- Custom flow facility with four sections: flow conditioner, developing section, test section, diffuser.
- Flow conditioner includes a perforated plastic sheet (4.8 mm thick, 4.8 mm diameter holes, 32% open area) and three screens to reduce incoming turbulence, plus a 2D contraction (inlet:outlet height ratio 8:1).
- Developing section is 1 m long to ensure fully-developed flow in the 50 cm test section; side/top walls are clear for optical access.
- Permeable bed comprised of a regular array of acrylic rods spanning channel width, installed in both developing and test sections (30 cm each).
- Two porosity configurations: 35% and 45% achieved by using 6.3 mm (1/4") rods alone (45%) or adding central 3.2 mm (1/8") rods to reduce porosity by ~10%.
- Flow rate controlled via pump frequency; measured with a insertion electromagnetic flow meter on a 1.5" PVC pipe.

## PIV setup
- Dual-head, pulsed Evergreen Nd:YAG laser generating ~1 mm thick laser sheet to illuminate seeding particles in the x–y plane.
- Imaging with a 16-bit, 5.5 MP sCMOS camera (2560 × 2160) and Navitar long-distance microscope (NA ~0.012); field of view ~18 × 15 mm².
- Biofilm developed on a 30 cm permeable bed section; biofilm-covered section placed in the test section for flow experiments.
- Flow rate varied by pump speed; data recorded at four pump frequencies.

## Boundary conditions and experiments
- Seventeen experiments (files named 1–17), each with specific settings:
  - Biofilm present (Y) or not (N).
  - Pump frequency (Hz): varies across experiments (e.g., 4.5, 8, 16, 30 Hz).
  - Bed porosity: 35% or 45% (with some cases 45–35% split across developing/test sections).
- Example configurations:
  - Experiments 1–3: no biofilm, porosity 35%, pump frequencies 8, 16, 30 Hz.
  - Experiments 4–9: biofilm present, porosity 45%, pump frequencies 8, 16, 30 Hz (and 4.5 Hz in some).
  - Experiments 10–13: no biofilm, 45–35% porosity split between developing/test sections; various pump frequencies.
  - Experiments 14–17: biofilm present across varying pump frequencies with 45% porosity.
- Notes indicate variations in porosity distribution across sections for certain runs.

## Data variables measured
For each experiment file, the following variables are recorded:
- Y = distance from top of the cylinder.
- U = mean streamwise velocity.
- V = mean wall-normal velocity.
- u', v' = fluctuating velocity components (downstream and vertical).
- u'u', u'v', v'v' = Reynolds stress components.
- Omega = mean vorticity.
- omega_rms = RMS of vorticity fluctuations.
- Lci = mean swirling strength.
- lci_rms = RMS of fluctuating swirling strength.

## Opportunities for data use and products (Data Support perspective)
- Build self-serve data products enabling exploration of flow physics under biofilm presence, bed porosity, and pump frequency.
  - Interactive dashboards to compare mean and fluctuating velocities and Reynolds stresses across experiments and positions Y.
  - Visualizations of mean vorticity and swirling strength distributions by condition (biofilm vs. no biofilm; porosity; pump frequency).
- Data integration and cross-analysis ideas:
  - Combine across the 17 experiments to assess how biofilm presence and bed porosity influence flow structure and turbulence metrics.
  - Correlate mean/ fluctuating velocities with bed porosity and pump frequency to identify regimes of significant biofilm impact on flow.
- Data products to consider:
  - Summary tables of U, V, Reynolds stresses, and vorticity metrics as a function of Y for each experiment.
  - Comparative charts showing changes in flow quantities with biofilm presence for each porosity level.
  - 2D field visualizations of velocity vectors and vorticity metrics to illustrate spatial patterns.
- Metadata and data management:
  - Maintain clear metadata for each file linking experiment number (1–17) to Biofilm, Pump freq, and Bed Porosity configurations.
  - Provide a data dictionary with defined variables (as listed) to support re-use and interpretation.
- Quality and accessibility considerations:
  - Ensure consistent units and coordinate conventions across all experiments.
  - Release early prototypes of dashboards to gather user feedback and iterate on data presentation and required derived metrics.

## Data management considerations
- Structure data with experiment identifier, configuration parameters (biofilm, porosity, pump frequency), and the measured variables for easy querying and cross-analysis.
- Include versioning and provenance to track any reprocessing or normalization steps applied to the PIV data.