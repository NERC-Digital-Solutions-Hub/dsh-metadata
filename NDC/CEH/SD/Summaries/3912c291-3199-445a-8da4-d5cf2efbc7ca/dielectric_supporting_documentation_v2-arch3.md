# Supporting documentation

## Overview
- This is a data-centric documentation of laboratory measurements linking apparent permittivity (dielectric constant) of granular media and soils to volumetric water content (VWC).
- Scope includes wetting, drainage, or both, across multiple materials and environments, collected over about a decade (1998–2006).
- Measurements were performed to understand how geometry, packing, temperature, particle size/shape, and aggregation influence dielectric response, enabling testing and calibration of moisture-detection models.

## Data Description and Scope
- Primary measured relationship: apparent permittivity as a function of VWC for porous media and soils.
- Materials: granular media (glass beads, quartz sand) and soils from Israel, Trinidad, and Utah, including specific soils (e.g., Hyrum, Kidman, Blacksmith Fork, Sawmill, Tony Grove, Wasatch, Sarid vertisol, Sarid sandy loam).
- Experimental breadth: wetting and/or drying paths; 8 distinct data sheets (CSV files) covering 1–3 phase systems, particle-size effects, temperature effects, anisotropy, and aggregate/soil structure.
- Data collection teams and sites: Volcani Center (Israel), University of the West Indies (Trinidad), Utah State University (USA); led by Shmulik Friedman (Israel), David Robinson (Trinidad), Scott Jones (USA).

## Methods and Instruments
- Time Domain Reflectometry (TDR):
  - Instrument: Tektronix TDR (models 1502B, 1502C).
  - Probes: parallel-plate transmission line configurations for uniform energy distribution.
  - Calibration: air-water method; t0 and Le calibrated (references include Heimovaara and de Water; Robinson et al.; WinTDR).
  - Temperature control: typically 22–25 °C range, with ±0.5–1 °C stability.
- Frequency Domain Analysis:
  - Instrument: Vector Network Analyzer (VNA, model HP 8753B) with open-ended dielectric probe (HP 85070B).
  - Frequency range: 1 MHz to 6 GHz; calibration using standard references.
- Sample preparation and cell design:
  - Purposive packing, drainage, and re-wetting protocols to achieve known porosity and stable water contents.
  - Cells fabricated to enable controlled drainage and wetting (rectangular and cylindrical geometries; inclusion of sintered membranes for base drainage in some setups).
  - Multiple materials included synthetic aggregates and natural soils; porosity and bulk densities independently verified.

## Datasets (8 CSV Sheets)
- 1_3_phase_measurements.csv: Permittivity vs water content for two natural Israeli soils (sandy loam and vertisol) across wetting/drying; includes phase information (2- and 3-phase systems) and mica-related tests in later sheets.
- 2_2_phase_measurements.csv: Two granular materials (glass beads and quartz grains) across two-phase mixtures; includes details on packing and porosity.
- 3_Particle_size_sand_glass.csv: Experiments with glass beads and quartz sand across size fractions; includes solid-phase permittivity estimation and particle-size distribution effects.
- 4_Temperature_sand_glass.csv: Temperature variation experiments ( Trinidad) exploring permittivity responses at different temperatures.
- 5_Mica_orientation.csv: Anisotropy study using phyllosilicate mica (anisotropy factor A) with two packing orientations relative to the electric field; solid permittivity determined via immersion method.
- 6_Aggregate_samples_and_properties.csv: Dielectric relationships in aggregated porous media (zeoponic, turface, profile, pumice) with focus on microstructural/configurational effects.
- 7_Soil_aggregates.csv: Similar aggregate-focused datasets applying the same methods as sheet 6 for soil aggregates.
- 8_Wasatch_soil.csv: Wasatch soil dataset; includes frequency-domain measurements; uses the VNA-based method described in sheet 6/7; was conducted with tight and loose packing to vary bulk density; temperature controlled around 25 °C.

## Data Structure and Units
- Common structure: 11 columns per sheet (12 columns in csv 8).
- Key fields:
  - ID number, Description of manipulation
  - VWC (cm3 cm-3)
  - Permittivity (dimensionless ratio)
  - Status_Orientation (Wetting/Drying)
  - Orientation (e.g., mica anisotropy direction in sheet 5)
  - Material (soil or granular material)
  - Particle size range (text)
  - Porosity (m3 m-3)
  - Particle density (g cm-3)
  - Bulk density (g cm-3)
  - Solid Permittivity (dimensionless)
  - Temperature (°C)
  - Frequency (GHz) for csv 8
- Missing values represented as NA.
- Data quality notes: measurements under tight QA; deionized water used; calibration against air/water; temperature control specified.

## Quality Control and Validation
- Calibration and verification:
  - TDR probes calibrated for effective length using deionized water and air.
  - VNA probe calibration with standard open-short-load references and known liquids.
  - Solid permittivity values derived via immersion methods or matching against known dielectrics (e.g., quartz 4.7, glass ~6.75–7.6 depending on calibration).
- Temperature control and moisture stability:
  - Experiments conducted at controlled temperatures (commonly 22–25 °C; some datasets at Trinidad lab conditions).
  - Drainage/rewetting protocols ensured stable VWC at measurement times.
- Reproducibility:
  - Multiple measurements per sample (e.g., 10 waveforms per calculation in some datasets); documented packing and weighing procedures to determine water-filled porosity and bulk density.

## Data Governance, Access, and Usage
- Data provenance and project context:
  - Funded and conducted across international collaborations (BARD, USDA, Utah Agricultural Experiment Station, UK-SCAPE/Natural Environment Research Council involvement).
- Metadata and openness:
  - Rich methodological metadata included (instrumentation, calibration, sample preparation, cell design, and environmental conditions).
  - Data structure and units clearly documented; 8 CSV data sheets with explicit experimental manipulations.
- Considerations for monitoring frameworks:
  - Provides calibrated relationships between dielectric properties and soil moisture under varied physical conditions (particle size, shape, aggregation, anisotropy, temperature, and packing density).
  - Highlights the importance of robust metadata, calibration standards, and governance to ensure data utility for moisture monitoring models.
  - The dataset exemplifies how to address data gaps and data quality challenges (e.g., need for standardized metadata, data sharing barriers, and surface-level harmonization across studies).

## Project Context and References
- Core publications underpinning methods and interpretation:
  - Friedman and Robinson (2002); Robinson et al. (2003, 2005); Blonquist et al. (2006, 2011); Topp, Davis, Annan (1980); Heimovaara (1993); WinTDR software references; and related dielectric mixing/modeling literature.
- Notable application areas:
  - Dielectric-based soil moisture sensing, calibrations for coarse-textured, layered soils, and anisotropic and aggregated porous media.
- Acknowledgments:
  - Projects and institutions spanning Israel, Trinidad, and Utah; contributions from multiple researchers and laboratories.