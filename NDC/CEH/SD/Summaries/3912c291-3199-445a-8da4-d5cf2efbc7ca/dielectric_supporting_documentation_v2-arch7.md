# Supporting documentation

## Overview
- A dataset describing laboratory measurements of apparent permittivity (dielectric constant) of granular media and soils as a function of volumetric water content (VWC), including wetting, drainage, or both.
- Measurements made with Time Domain Reflectometry (TDR) and, in some cases, a Vector Network Analyzer (VNA) for frequency-domain dielectric properties.
- Data collected over approximately 1998–2006 by teams in Israel (Volcani Center), Trinidad (University of the West Indies), and the USA (Utah State University).
- Includes natural soils (e.g., Kidman, Hyrum, Blacksmith Fork, Sawmill, Tony Grove, Wasatch, Sarid vertisol, Sarid sandy loam) and various granular media and aggregate materials; used to study how geometry, packing, temperature, particle size/shape, aggregation, and disturbance affect dielectric response and its relationship to water content.

## Data content and scope
- Eight CSV sheets containing dielectric data in a consistent schema, spanning 11 variables (12 in csv8) with missing values represented as NA.
- Variables include: ID, Material, Particle size range, Porosity, Particle density, Bulk density, Solid permittivity, Temperature, VWC (volumetric water content), Permittivity (apparent), Status/Orientation (wetting or drying), and for csv8 also Frequency (GHz).
- Data cover multiple experimental configurations:
  - 1_3_phase_measurements: 3-phase (unsaturated) and related measurements for Israeli soils and granular media.
  - 2_2_phase_measurements: 2-phase measurements for granular materials (glass beads, quartz sand) with a coaxial cell.
  - 3_Particle_size_sand_glass: binary mixtures of glass beads and quartz sand across size fractions and mixing ratios.
  - 4_Temperature_sand_glass: temperature-controlled permittivity measurements on sand/glass samples.
  - 5_Mica_orientation: anisotropy-focused measurements in mica packing with orientational dependencies.
  - 7_Soil_aggregates and 8_Wasatch_soil: aggregate media and soils with multiple bulk densities and water contents; Wasatch soil includes frequency-domain measurements.
- Common measurement framework: TDR-based permittivity (and derived water content) calibrated against known references (air/water) and_temperature-controlled conditions; in some datasets, VNA measurements for complex permittivity over 1 MHz–6 GHz.

## Methods and measurement setup
- Time Domain Reflectometry (TDR)
  - Instrument: Tektronix TDR cable tester (model 1502B or 1502C) with parallel-plate transmission lines to ensure uniform field distribution.
  - Cell design: typically ~950 cm3 volume, parallel stainless-steel plates, drainage/wetting via base assembly (ceramic cups or sintered membranes).
  - Calibration: air and deionized water calibrations to determine effective length and electrode characteristics; temperature controlled around 25°C (±0.5°C).
  - Procedures: samples repacked and drained/re-wetted under controlled conditions; water content inferred from sample mass and porosity verification; anisotropy studies (e.g., mica) used specific packing orientations.
- Frequency-domain dielectric measurements
  - Instrument: Vector Network Analyzer (VNA, e.g., HP model 8753B) with open-ended dielectric probe (HP 85070B) and a 3.17 cm3 sample holder.
  - Frequency range: 1 MHz to 6 GHz; calibration with standard open/short/load references.
  - Purpose: obtain complex permittivity from reflection measurements (S11) and derive solid-phase permittivity for materials like clays.
- Materials and samples
  - Porous media: synthetic/aggregate media (zeoponic, turface, profile, pumice) and other aggregate types with known porosities and densities.
  - Soils: a range of Utah and Israeli soils; detailed soil descriptions provided (e.g., Kidman soil as sand, Hyrum as loamy sand, Sarid vertisol/sandy loam).
- Quality control
  - Temperature control, calibrated instruments, deionized water usage, repeated measurements, and documented calibration procedures.
  - Notes on anisotropy and specific material behaviors (e.g., swelling/cracking in Sarid clayey soil) considered in interpretation.

## Data structure and units
- Eight CSV sheets with a consistent schema (11 columns, 12 columns in csv8).
- Key columns (examples across sheets):
  - ID number (text), Material (text), Particle size range (text), Porosity (m3/m3), Particle density (g/cm3), Bulk density (g/cm3), Solid Permittivity (ratio), Temperature (°C), VWC (cm3/cm3), Permittivity (ratio), Status/Orientation (text: Wetting/Drying), Frequency (GHz only in csv8).
- Data description fields accompany each variable (e.g., VWC meaning, Permittivity meaning, Orientation, etc.).
- Units summary:
  - VWC: cm3 cm-3
  - Permittivity: unitless ratio
  - Porosity: m3 m-3
  - Densities: g cm-3
  - Temperature: °C
  - Frequency (csv8): GHz
- Solid permittivity (for solids) determined via immersion calibration or material-specific methods.

## Spatial, temporal, and provenance context
- Sites and origins:
  - Israel (Volcani Center) datasets
  - Trinidad (University of the West Indies)
  - USA (Utah State University)
- Soils include multiple named local soils (e.g., Kidman, Hyrum, Blacksmith Fork, Sawmill, Tony Grove, Wasatch Front in Utah; Sarid soils in Israel).
- Timeframe of sample acquisition: 1998–2006.
- Data provenance includes detailed methodological descriptions and references to calibration and analysis papers; data compiled across international collaborations.

## Reuse in GIS and potential applications
- GIS-ready potential:
  - Use with GIS to map dielectric properties and derived volumetric water content across sites, soil types, and aggregate media.
  - Integrate with soil property layers (texture, bulk density, porosity) to model spatial variability of moisture and dielectric response.
  - cross-site comparisons to understand how geometry, packing, and temperature influence dielectric behavior and moisture estimation.
- Applications:
  - Calibrating remote sensing or in-situ dielectric-based moisture retrieval algorithms.
  - Informing soil moisture models and hydrological studies that rely on dielectric properties.
  - Supporting datasets for geospatial analyses of porous media and soil physics in GIS workflows.

## Access, data packaging, and metadata
- Data delivered as eight CSV sheets; missing data represented as NA.
- Each sheet shares a uniform data schema with documented column descriptions.
- Metadata includes measurement conditions (temperature, equipment, calibration) and sample descriptions to support reproducibility and cross-dataset comparability.

## References and credits
- Core sources and calibration/method references (selected):
  - Blonquist Jr. et al. 2006; 2011
  - Friedman 1998; Friedman & Robinson 2002
  - González-Teruel et al. 2020
  - Heimovaara 1993; Heimovaara & de Water 1993
  - Or et al. 2003; WinTDR software
  - Topp, Davis, and Annan 1980
  - Robinson 2004; Robinson & Friedman 2001; Robinson et al. 2003/2005
- Projects and funding:
  - BARD Project IS-2839-97 (Israel–USA collaboration)
  - USDA/ Utah Agricultural Experiment Station support
  - UK-SCAPE programme (NERC National Capability)

## Additional context and notes
- The datasets emphasize careful calibration, temperature control, and cell design to ensure reliable permittivity measurements, with explicit attention to anisotropy (notably in mica) and the effects of packing, particle size distribution, and aggregation on dielectric response.
- The collection provides a comprehensive platform for deriving relationships between dielectric properties and water content across varied materials and configurations, with explicit guidance on data structure to facilitate GIS-based integration and exploratory analysis.