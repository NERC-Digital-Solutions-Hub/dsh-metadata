# Purpose of study

## Objective
- Conduct a preliminary investigation into the interaction between turbulence and biofilms using particle image velocimetry (PIV) to obtain spatially- and temporally-resolved velocity fields in water under different flow configurations.

## Experimental facility and channel design
- Custom flow facility with four sections: flow conditioner, developing section, test section, and diffuser.
- Flow conditioner uses a perforated plastic sheet (4.8 mm thickness, 4.8 mm holes, 32% open area) plus three screens to reduce incoming turbulence.
- Developing section (1 m) ensures fully developed flow in the 50 cm test section, with float glass windows and top wall for optical access.
- Permeable bed made from a regular array of acrylic rods spanning channel width, forming a frame with holes to hold rods (peg-board like).
- Two porosity configurations for the bed: 35% and 45%.
  - Higher porosity (45%) achieved with 6.3 mm rods in a square array.
  - Lower porosity (35%) achieved by adding 3.2 mm rods at the center of each square cell, reducing porosity by ~10%.
- Flow rate controlled via pump frequency and measured with an insertion electromagnetic flow meter in a PVC pipe.

## Permeable bed configurations
- Porosity 35% and 45% are implemented within the same channel sections (developing and test sections).
- A 30 cm long region of the bed is used for biofilm development; the biofilm-covered bed is then placed in the test section for flow experiments.

## PIV instrumentation and imaging
- Laser: dual-head, pulsed, Evergreen Nd:YAG laser delivering up to 200 mJ per pulse to create a ~1 mm thick laser sheet in the x-y plane.
- Imaging: 16-bit, 5.5 MP sCMOS camera (2560 × 2160) with a Navitar long-distance microscope (NA ~0.012, 0.25× objective, 2× adapter, ~2× zoom).
- Field of view: approximately 18 mm × 15 mm.
- Biofilm development: biofilm is cultivated on the 30 cm permeable bed segment; the biofilm-covered section is then placed in the test section for flow experiments.
- Flow control during experiments: pump speed is varied using a variable frequency drive; data are collected at four distinct pump frequencies.

## Experimental protocol and boundary conditions
- Seventeen distinct experiments conducted, identified by data file numbers 1 through 17.
- Variation factors include:
  - Biofilm presence: with biofilm (Y) or without biofilm (N).
  - Bed porosity: 35% or 45%.
  - Pump frequency: 4.5 Hz, 8 Hz, 16 Hz, and 30 Hz (not all combinations present in every file).
  - Some experiments combine 45% developing region with 35% test region (noted as 45-35 in certain entries).
- Representative pattern:
  - Experiments 1–3: no biofilm, porosity 35%, frequencies 8–30 Hz.
  - Experiments 4–9: biofilm present, porosity 45%, frequencies 8–30 Hz (and 4.5 Hz in some cases).
  - Experiments 10–13: no biofilm, porosity 45-35 (45% developing, 35% test) with frequencies 4.5–30 Hz.
  - Experiments 14–17: biofilm present, porosity 45%, frequencies 4.5–30 Hz.
- Each file corresponds to a specific set of conditions; variables measured per file are listed below.

## Measured data and variables
For each experimental file, the following variables are recorded or derived:
- Y: Distance from the top of the cylinder (vertical position).
- U: Mean streamwise velocity.
- V: Mean wall-normal velocity.
- u', v': Fluctuating velocity components (streamwise and wall-normal).
- u'u', u'v', v'v': Reynolds stress components.
- Omega: Mean vorticity.
- omega_rms: RMS of vorticity fluctuations.
- Lci: Mean swirling strength.
- lci_rms: RMS of fluctuating swirling strength.

## Data organization and potential reuse
- Data are organized into 17 separate results files (named 1 through 17) corresponding to different combinations of biofilm presence, bed porosity, and pump frequency.
- The study provides a comprehensive set of velocity fields and turbulence metrics (including Reynolds stresses and vorticity/swirling measures) across multiple configurations, enabling analyses of how turbulence interacts with biofilms and how bed porosity influences flow characteristics.

## Relevance to data strategy and management
- Rich, multi-parameter data bundle: spatially and temporally resolved velocity fields plus derived turbulence statistics across several experimental scenarios.
- Clear metadata opportunities: explicit recording of biofilm status, bed porosity, pump frequency, and sectioning (developing vs test section) to support reproducibility and comparison.
- Data discoverability and quality considerations: multiple experimental conditions and derived metrics necessitate consistent naming, documentation of measurement units, and standardized metadata to facilitate reuse and cross-study integration.