# Purpose of study

- A preliminary investigation of the interaction between turbulence and biofilms using particle image velocimetry (PIV), providing spatially- and temporally-resolved velocity fields in water for different flow configurations.

## Overview of study goals

- Establish how turbulence interacts with biofilms under controlled flow conditions.
- Acquire detailed velocity data (mean and fluctuating components) and derived metrics to analyze flow-biofilm interactions.

## Channel design and experimental facility

- Custom flow facility with four sections: flow conditioner, developing section, test section, and diffuser.
- Permeable bed comprised of an array of acrylic rods spanning channel width, enabling two porosity levels (35% and 45%).
- Porosity differences achieved by rod sizes and arrangement (6.3 mm rods for higher porosity; center-added 3.2 mm rods to reduce porosity by ~10% for the lower porosity scenario).
- Flow rate controlled via pump frequency; measured with an insertion electromagnetic flow meter.
- Biofilm developed on a 30 cm permeable bed segment and then placed in the test section for flow experiments.
- Optical access provided with float glass windows; design allows fully-developed flow in the 50 cm test section.

## PIV setup and imaging configuration

- Dual-head, pulsed Nd:YAG laser producing a ~1 mm-thick laser sheet to illuminate seed particles in the x-y plane.
- Imaging with a 16-bit, 5.5 MP sCMOS camera (2560 × 2160), using Navitar long-distance microscope (NA ~0.012) and a ~2× zoom lens; field of view ~18 × 15 mm^2.
- Data acquisition configured to capture velocity fields and related metrics from the illuminated plane.

## Experimental design and boundary conditions

- Seventeen distinct experiments labeled 1–17, each varying a combination of:
  - Biofilm presence (Y/N)
  - Pump frequency (Hz)
  - Bed porosity (35% or 45%)
- Notable patterns:
  - Experiments 1–3: no biofilm, porosity 35%, varying pump frequencies (8, 16, 30 Hz)
  - Experiments 4–9: biofilm present, porosity 45%, varying pump frequencies (8–30 Hz)
  - Experiments 10–13: no biofilm, porosity transitioning between 45% in the developing section and 35% in the test section
  - Experiments 14–17: biofilm present, porosity 45%, varying pump frequencies (4.5–30 Hz)
- Measurements include multiple boundary-condition permutations to assess the influence of biofilm, porosity, and flow rate on the flow field.

## Measured variables and data files

- For each experiment file (1–17), the following variables are recorded:
  - Y: distance from the top of the cylinder
  - U: mean streamwise velocity
  - V: mean wall-normal velocity
  - u’, v’: fluctuating velocity components
  - u’u’, u’v’, v’v’: Reynolds stress components
  - Omega: mean vorticity
  - omega_rms: RMS of vorticity fluctuations
  - Lci: mean swirling strength
  - lci_rms: RMS of fluctuating swirling strength

## Data management and governance implications for Data Stewards

- Data architecture and metadata
  - Use a clear, consistent experiment identifier (1–17) mapped to explicit boundary conditions (biofilm presence, pump frequency, bed porosity).
  - Capture instrument details and settings (PIV laser energy, camera model, field of view, optical setup) to support reproducibility.
  - Document bed geometry, porosity, and region of interest (ROIs) corresponding to measurements.
- Metadata schema recommendations
  - Experiment ID, biofilm_present (Y/N), pump_frequency_hz, bed_porosity_percent, developing_section_porosity_percent (if applicable), test_section_porosity_percent (if applicable), notes.
  - Measurement types and units for each variable (e.g., velocities in m/s, vorticity in 1/s, swirling strength units).
  - Equipment specifics (laser energy, camera resolution, field of view, calibration references).
  - Boundary and flow conditions (flow conditioner details, inlet/outlet geometry, flow meter calibration).
- Quality and provenance
  - Link each dataset to the exact experimental conditions and any preprocessing steps (e.g., velocity field derivation, filtering).
  - Maintain raw (images/fields) and processed data with versioning to support traceability.
- Data formats and interoperability
  - Prefer consistent, self-describing formats for raw and processed data; document units and coordinate conventions.
  - Provide a data dictionary mapping each variable to its physical meaning and calculation method.
- Access, sharing, and reuse
  - Ensure datasets (1–17) are discoverable in the data catalog with comprehensive descriptions.
  - Include documentation detailing the biofilm production method, porosity characteristics, and measurement limitations.
- Documentation and lineage
  - Archive notes for each experiment (e.g., anomalies, calibration events, deviations from plan) to aid reproducibility and secondary analyses.
- Practical considerations for the data steward
  - Anticipate potential interoperability needs with other flow-biofilm studies by adopting common PIV conventions and unit standards.
  - Prepare for future reuse by including complete boundary-condition matrices and explicit definitions for all derived metrics (e.g., Reynolds stresses, swirling strength).

## Key takeaways

- The study systematically varies biofilm presence, bed porosity, and pumping rate to explore turbulence-biofilm interactions using detailed PIV data.
- A specialized flow facility and careful optical/measurement setup enable high-resolution velocity fields and derived turbulence metrics within a 30 cm permeable bed region.
- The data collection framework yields seventeen well-documented experiments with explicit metadata, supporting rigorous analysis and reproducibility, with clear guidance on data governance and provenance for Data Stewards.