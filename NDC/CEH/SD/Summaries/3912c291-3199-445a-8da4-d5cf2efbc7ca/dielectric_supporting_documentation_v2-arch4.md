# Supporting documentation

- The document describes a multi-lab dataset of the apparent permittivity (dielectric constant) of granular media and soils as a function of volumetric water content, including wetting and drainage experiments and materials with different particle shapes.
- Data were collected over roughly a decade (1998–2006) across Israel, Trinidad, and the USA, led by teams at Volcani Center, University of the West Indies, and Utah State University.
- The dataset is intended to test how physical factors (geometry, packing, temperature, grain shape, aggregation) influence dielectric response and to support models linking permittivity to water content.

## What the data contain

- Measurements of apparent permittivity as a function of volumetric water content for porous media and soils, under wetting and/or drying conditions.
- Instruments used include Time Domain Reflectometry (TDR) with Tektronix 1502B/Tektronix 1502C and a TRIME-FM/IMKO setup, as well as frequency-domain measurements with a Vector Network Analyzer (VNA).
- Materials include natural soils (various Utah soils, Sarid soils from Israel) and synthetic/granular media (glass beads, quartz grains, aggregated porous media such as zeoponics and pumice).
- Data describe a range of conditions: phase (2-phase and 3-phase systems), particle sizes, anisotropy (mica orientation experiments), temperature variations, and aggregate configurations.
- Each data sheet includes meta-information such as material, particle size range, porosity, densities, solid permittivity, temperature, and, where relevant, frequency for VNA measurements.

## Data collection methods and instrumentation

- Time Domain Reflectometry (TDR)
  - Probes: parallel-plate transmission line design for uniform field distribution.
  - Calibration: air/water length calibration; 25°C ±0.5°C temperature control.
  - Measurement cells: custom plexiglass containers (rectangular and cylindrical) with drainage and rewetting capability; designed to control packing density and water content.
  - Temperature control and monitoring during measurements.

- Frequency Domain Analysis (VNA)
  - Instrument: Vector Network Analyzer (Model 8753B) with open-ended dielectric probe (HP 85070B).
  - Frequency range: 1 MHz to 6 GHz.
  - Calibration standards used: air, deionized water, shorting block, and standard calibration kit.
  - Purpose: derive complex permittivity from reflection (S11) measurements in clays and clayey soils.

- Materials and sample preparation
  - Soils: multiple Utah soils and Sarid soils, with details on texture and origin.
  - Granular media: glass beads and quartz grains with controlled size fractions; solid phase permittivity measured via immersion methods.
  - Aggregates: various stabilized ceramic and natural aggregates.

- Experimental protocol highlights
  - Reproducible water content steps from saturation to oven-dry states with careful control of packing density and drainage.
  - Temperature-controlled environment to minimize thermal effects on permittivity.
  - Anisotropy experiments (mica) to quantify directional dependence of permittivity.

## Data structure and units

- There are 8 CSV sheets, each with a common structure (11 columns; 12th column present in the last sheet).
- Core fields include:
  - ID number, Description
  - Volumetric Water Content (VWC, cm3 cm-3)
  - Permittivity (apparent, dimensionless)
  - Status/Orientation (wetting/drying; orientation details for anisotropy)
  - Material (type of material)
  - Particle size range
  - Porosity (m3 m-3)
  - Particle density (g cm-3)
  - Bulk density (g cm-3)
  - Solid Permittivity
  - Temperature (°C)
  - Frequency (GHz) for VNA data (only in csv 8)
- Missing values are represented as NA.

## Datasets included (files)

- 1_3_phase_measurements.csv
- 2_2_phase_measurements.csv
- 3_Particle_size_sand_glass.csv
- 4_Temperature_sand_glass.csv
- 5_Mica_orientation.csv
- 6_Aggregate Samples and Properties.csv
- 7_Soil_aggregates.csv
- 8_Wasatch_soil.csv

## Data quality, provenance, and reproducibility

- Calibrations and measurement protocols are documented in detail, including electrode calibration, travel-time corrections, and solid permittivity determinations.
- Temperature control and calibration against standard references ensure data comparability across experiments and sites.
- Data were produced under multiple projects and funding sources (e.g., BARD IS-2839-97, USDA, UK-SCAPE NE/R016429/1), underscoring cross-institutional collaboration and long-term data collection discipline.
- The dataset supports testing and calibration of water-content–permittivity models, including physically derived calibrations for coarse-textured, layered soils.

## Implications for data strategy and governance (Data Leaders perspective)

- Strengths to leverage
  - Rich, multi-lab provenance with careful calibration, enabling cross-site comparability and model testing.
  - Comprehensive metadata and standardized data schema across 8 CSV files, aiding discoverability and reuse.
  - Explicit documentation of experimental conditions (temperature, packing, porosity, solid permittivity) to support reproducibility and advanced modeling.
  - Availability of both wetting and drying stages, anisotropy experiments, and various aggregate types broadens applicability.

- Data management considerations
  - Ensure consistent metadata standards (units, definitions, calibration methods) to maintain interoperability across datasets and future reuse.
  - Maintain versioning and provenance trails, given multi-site data collection over many years.
  - Address potential data gaps or inconsistencies due to heterogeneous lab setups by preserving lab-specific notes and calibration records.
  - Plan for data integration with broader soil physics or hydrology platforms, given the relevance to soil moisture sensing, vadose zone studies, and material dielectric models.

- Potential uses and value
  - Calibration and validation of dielectric-based soil moisture models across different textures, packing densities, and temperatures.
  - Development of robust, transferable water content estimation tools for porous media and soils.
  - Benchmarking of anisotropy effects (mica) and aggregate configurational effects on dielectric response for improved sensor interpretation.

## References and project context

- Key publications informing methods and models:
  - Dielectric relationships in aggregated porous media and anisotropy investigations (Blonquist et al., 2006; 2011)
  - Temperature and particle-size effects on permittivity (Robinson & Friedman; Robinson et al.)
  - Dielectric spectroscopy and mixing models for clays and clays minerals (González-Teruel et al., 2020)
  - TDR methodology and calibration practices (Heimovaara; Robinson et al.; Topp et al.)
- Projects and funding sources:
  - BARD (Project IS-2839-97) and contributions from Volcani Center
  - USDA/NRI and Utah Agricultural Experiment Station support
  - UK-SCAPE programme (NE/R016429/1)