# Purpose of study

- Objective: A preliminary investigation of how turbulence interacts with biofilms using particle image velocimetry (PIV), providing spatially and temporally resolved velocity fields in water for different flow configurations.
- Relevance: Demonstrates data collection and analysis capabilities to assess environmental fluid dynamics related to biofilm development and flow conditions.

## Experimental apparatus and channel design

- Custom flow facility with four sections: flow conditioner, developing section, test section, and diffuser.
- Flow conditioner features a 4.8 mm perforated plastic sheet, 4.8 mm holes, 32% open area, and screens to reduce incoming turbulence; includes a 2D contraction with inlet/outlet height ratio of 8:1.
- Developing section is 1 m long to produce fully developed flow in the subsequent 50 cm test section; optical access via float glass windows on two side walls and the top.
- Permeable bed comprised of a regular array of acrylic rods spanning channel width, housed in a frame with holes for rods; two porosity levels (35% and 45%): 45% achieved with 6.3 mm rods in a square array; 35% achieved by adding 3.2 mm rods at cell centers to reduce porosity by ~10%.
- Bed portions: developing section and test section each 30 cm long.
- Flow rate controlled by pump frequency; measured with an insertion electromagnetic flow meter on a PVC pipe.

## PIV setup and imaging

- Laser: Dual-head, pulsed Evergreen Nd:YAG laser (~200 mJ/pulse) creating a ~1 mm-thick laser sheet in the streamwise-wall-normal plane.
- Imaging: 16-bit, 5.5 MP camera (2560 × 2160) with 6.5 μm pixels, Navitar long-distance microscope (NA ~0.012; ~0.25× objective, 2× adapter, ~2× zoom).
- Field of view: ~18 × 15 mm².
- Biofilm development: Formed on a 30 cm permeable bed section; the biofilm-covered segment placed in the test section for flow experiments.
- Flow control: Pump speed adjusted by a variable frequency drive; data collected at four pump frequencies.

## Experiments and boundary conditions

- Total of 17 experiments with varying configurations (files named 1–17).
- Primary variables altered per run:
  - Biofilm presence: yes or no.
  - Pump frequency (Hz): e.g., 4.5, 8, 16, 30.
  - Bed porosity (%): 35% or 45% (or combinations across developing/test sections).
- Representative setups include:
  - No biofilm at multiple pump frequencies (e.g., 8, 16, 30 Hz) with 35% porosity.
  - Biofilm present at 45% porosity, various pump frequencies (4.5, 8, 16, 30 Hz).
  - Some runs with mixed porosity (45% in developing section and 35% in test section) for specific pump frequencies.

## Measured variables and data organization

- For each experiment/file, recorded variables include:
  - Y: distance from the top of the cylinder.
  - U: mean streamwise velocity.
  - V: mean wall-normal velocity.
  - u', v': fluctuating velocity components.
  - Reynolds stresses: u'u', u'v', v'v'.
  - Omega: mean vorticity.
  - omega_rms: RMS of vorticity fluctuations.
  - Lci: mean swirling strength.
  - lci_rms: RMS of swirling strength fluctuations.
- Data files (1–17) correspond to the specific boundary condition combinations described.

## Data considerations

- Study aims to establish baseline understanding of turbulence–biofilm interactions and to provide a dataset of velocity fields and turbulence metrics across different porosities and biofilm conditions.
- Optical access and permeable-bed geometry are visually supported by figures; measurements provide comprehensive turbulence descriptors for subsequent analysis or cross-study comparisons.