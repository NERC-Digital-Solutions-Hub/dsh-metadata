# Supporting documentation

## Overview
- Data set comprises laboratory measurements of apparent permittivity (dielectric constant) of granular media and soils as a function of volumetric water content (VWC), including wetting and/or drainage.
- Measurements were collected over a 10-year period using Time Domain Reflectometry (TDR) and, for a subset, a Vector Network Analyzer (VNA) in frequency-domain dielectric tests.
- Aimed to quantify how physical factors (geometry, packing, temperature, particle size/shape, aggregation) influence dielectric response and to support testing of models relating permittivity to water content.

## Data content and scope
- Measurements cover granular media and soils with varying shapes and textures, including natural soils from Israel, Trinidad, and the USA (Utah State University).
- Temperature controlled experiments (generally around 25°C; some datasets at other temps such as Trinidad ~5–25°C) and careful calibration procedures.
- Data organized into eight CSV sheets, each representing different experimental conditions or material systems.
- Missing values are recorded as NA.

## Experimental methods and instruments
- Time Domain Reflectometry (TDR)
  - Equipment: Tektronix TDR (model 1502B or 1502C) with rod or parallel-plate probes.
  - Probes calibrated for effective length using deionized water and air; temperature control typically at 25°C ± 0.5°C.
  - Common measurement cells: custom plexiglass containers with parallel-plate transmission lines to improve energy distribution and measurement uniformity.
  - Data processing: waveform analysis with software by Heimovaara and de Water (1993) and Or et al. (2003); WinTDR used in some datasets.
- Frequency-Domain Analysis
  - Instrument: Vector Network Analyzer (VNA; HP 8753B) with open-ended coaxial dielectric probe (HP 85070B; frequency 1 MHz–6 GHz).
  - Calibration: open, short, load standards; post-processing to extract complex permittivity from S11.
  - Used for clay minerals and clayey soils; calibration against known standards (air, water, short) and probe-specific corrections.

## Materials and sample design
- Porous media
  - Artificial media and natural aggregates described (e.g., zeoponic, turface, profile, pumice).
  - Emphasis on how microstructure and phase configuration affect water-content–permittivity relationships.
- Soils and samples
  - Israel: Sarid vertisol and Sarid sandy loam; Bet Dagan sandy loam in natural contexts.
  - Utah, USA: Hyrum loamy sand, Kidman sand, Blacksmith Fork, Sawmill, Tony Grove, Wasatch Front soils.
  - Trinidad: Soil samples from University of the West Indies.
- Representative soil properties
  - Soil classifications and basic properties (particle density ~2.65 g/cm3; some soils with different textures).
  - For some datasets, solid-phase permittivity determined via immersion-method calibration.

## Data structure and fields
- Eight CSV sheets, each with a consistent basic data structure.
- Common columns (11, 12 in CSV 8)
  - ID number (text)
  - DESCRIPTION (text): experimental manipulation ID
  - VWC (cm3 cm-3)
  - Permittivity (ratio)
  - Status_Orientation (text): wetting or drying status
  - Orientation (text): mica or other anisotropy orientation when applicable
  - Material (text): material type (soil or granular)
  - Particle size range (text)
  - Porosity (m3 m-3)
  - Particle density (g cm-3)
  - Bulk density (g cm-3)
  - Solid Permittivity (ratio): solid-phase permittivity from immersion measurements
  - Temperature (°C) (CSVs 1–7; optional in CSV 8)
  - Frequency (GHz) (CSV 8 only)

## Quality control and calibration
- Multiple calibration steps for TDR probes (air-water method; length corrections t0 and Le).
- Temperature-controlled measurements to minimize thermal effects.
- Deionized water and high-purity standards used; balances calibrated.
- Replicate measurements conducted; some data explicitly noted as not included in the main dataset.
- For mixed materials and aggregates, careful packing and drainage procedures to achieve known porosity and saturated conditions; porosity confirmed against measured densities with high accuracy.

## Datasets (summary of contents)
- 1_3_phase_measurements.csv
  - Permittivity vs. VWC for two natural Israeli soils (sandy loam and vertisol) under wetting and drying; includes measurements with TRIME-FM TDR and notes on swelling/cracking in clayey samples.
- 2_2_phase_measurements.csv
  - Two granular materials (glass beads and quartz grains) with different particle sizes; includes TDR-based permittivity measurements in a coaxial cell.
- 3_Particle_size_sand_glass.csv
  - Experiments with glass beads and quartz sand; multiple size fractions and binary mixtures; detailed packing and water-content determination; includes dry bulk density and water-filled porosity calculations.
- 4_Temperature_sand_glass.csv
  - Temperature-controlled permittivity measurements for sand and glass spheres with equilibrated moisture content.
- 5_Mica_orientation.csv
  - Anisotropy-focused measurements using phlogopite mica; two orientations (vertical/horizontal) to quantify anisotropy in permittivity vs. water content.
- 6_Aggregates.csv
  - Aggregated porous media (zeoponic, turface, profile, pumice) with parallel-plate TDR cells; includes both porosity and bulk densities, plus calibration and sampling details.
- 7_Soil_aggregates.csv
  - Similar aggregation-focused data for soils; methods aligned with 6_Aggregates.
- 8_Wasatch_soil.csv
  - Wasatch soil dataset with tie-ins to frequency-domain measurements (VNA); multiple bulk densities and moisture contents achieved by compaction and drainage; includes standard TDR procedures and analysis.

## References and provenance
- Key methodological and modeling references spanning TDR calibration, dielectric mixing models, and anisotropy measurement techniques.
- Projects funded and collaborations across Israel, Trinidad, and the USA; part of broader initiatives (e.g., BARD, USDA, UK-SCAPE/NERC).

## Usage and potential analyses
- Correlation analysis: relate apparent permittivity to volumetric water content across materials, textures, and packing densities.
- Model testing: evaluate mixing models and physically derived calibrations for coarse-textured, layered, and aggregated porous media.
- Anisotropy assessment: use mica-oriented datasets to quantify directional dependence of dielectric response in aligned pore networks.
- Temperature effects: study how temperature shifts influence permittivity as a function of moisture in different media.
- Application potential: calibrate soil-moisture sensing algorithms, improve interpretation of TDR/VNA measurements in lab settings, and test predictions of dielectric response under varying microstructures.