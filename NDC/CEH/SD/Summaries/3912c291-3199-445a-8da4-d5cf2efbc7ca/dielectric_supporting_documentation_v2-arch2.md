# 1 Data description

## What the dataset contains
- Laboratory measurements of apparent permittivity (dielectric constant) of granular media and soils as a function of volumetric water content (VWC), including wetting and drainage scenarios.
- Data collected over about 10 years using Time Domain Reflectometry (TDR) and additional measurements with a network analyser (frequency domain).
- Datasets cover multiple soils and granular materials, with varying particle shapes and packing conditions.

## Where and when the data were collected
- Laboratories: Volcani Centre (Israel), University of the West Indies (Trinidad), and Utah State University (USA).
- Soils include Hyrum, Kidman, Blacksmith Fork, Sawmill, Tony Grove, Wasatch soils (Utah) and Sarid soils (Israel).
- Timeframe: 1998–2006.

## How the data were generated
- Time Domain Reflectometry (TDR) measurements using Tektronix TDR equipment and associated calibration procedures; temperature usually maintained near 25°C.
- Additional measurements with a Vector Network Analyzer (VNA) for frequency-domain dielectric properties (1 MHz–6 GHz) using open-ended coaxial probes.
- Detailed device calibrations, probe length adjustments, and standard references (air, deionized water, shorting block) were used to ensure measurement accuracy.
- Experimental cells and packing procedures were carefully constructed (parallel-plate transmission lines; specific container geometries; controlled drainage and saturation).

## Why the data were collected
- To determine how dielectric response relates to volumetric water content in porous media and soils, and how factors such as geometry, packing, particle size/shape, aggregation, temperature, and disturbance affect the dielectric properties.
- To test and develop models linking permittivity to water content in unsaturated and saturated conditions, using both time-domain and frequency-domain approaches.

## Who conducted and organized the work
- A collaboration across Israel (Volcani Center), Trinidad (University of the West Indies), and the USA (Utah State University), led by Shmulik Friedman (Israel), David Robinson (Trinidad), and Scott Jones (USA), with multiple supporting researchers.

## Project background and aims
- Central questions across about a decade of work:
  - How do geometrical factors affect dielectric response in two-phase (saturated/dry) and three-phase (partially wet) porous media?
  - How do wetting/drying, packing density, particle size, temperature, particle shape/orientation, aggregation, and disturbance influence dielectric properties?
- The research underpins the understanding and modeling of the water content–permittivity relationship in granular media and soils.

## Time domain Reflectometry (TDR) and frequency-domain instruments
- TDR: Tektronix 1502B/1502C cable testers, coaxial connections, PC-based waveform analysis (WinTDR/legacy software), calibrations using air and water, and controlled temperatures.
- Frequency domain: Vector Network Analyzer (HP 8753B) with an open-ended dielectric probe; calibration against standards; data used to extract complex permittivity.

## Porous media and soils studied
- Porous media: various aggregates and synthetic materials (e.g., Turface, profile aggregates, zeoponic material, pumice) with different sizes and textures.
- Soils: multiple Utah soils (Hyrum, Kidman, Blacksmith Fork, Sawmill, Tony Grove, Wasatch Front) and Sarid soils (vertisol and sandy loam) from Israel.

## Data files and structure
- Eight CSV sheets provided, each containing data on dielectric properties, water content, and experimental conditions.
- General data columns (11, with 12 in the last sheet) include:
  - ID, Description, Volumetric Water Content (VWC) with units, Apparent Permittivity, Status/Orientation, Material, Particle size range, Porosity, Particle density, Bulk density, Solid permittivity, Temperature, Frequency (only in CSV 8).
- Data cover several experimental setups:
  - 1_3_phase_measurements.csv: permittivity vs. VWC for two natural Israeli soils (sandy loam and vertisol) under wetting/drying.
  - 2_2_phase_measurements.csv: two granular materials (glass beads and quartz grains) with different packings.
  - 3_Particle_size_sand_glass.csv: experiments with glass beads and quartz sand across size fractions and mixtures; includes water content and porosity calculations.
  - 4_Temperature_sand_glass.csv: effect of temperature on permittivity during equilibration for Trinidad samples.
  - 5_Mica_orientation.csv: anisotropy measurements in mica using oriented dielectric setups; includes solid permittivity for mica.
  - 6_Aggregates.csv; 7_Soil_aggregates.csv; 8_Wasatch_soil.csv: additional aggregate/soil datasets with corresponding TDR and, for 8, frequency-domain data.
- Missing values are indicated as NA.

## Data quality, calibration, and controls
- Temperature controlled within narrow ranges during measurements.
- Deionized water and calibrated references used for TDR length and calibration.
- Short- and open-standard calibrations applied for VNA measurements.
- Careful cell design and packing procedures to minimize air entrapment and ensure representative sampling volumes.
- Reproducibility ensured through multiple measurements and consistent protocols.

## Details of data structure and units (summary)
- 11–12 columns per sheet:
  - ID, Description, VWC (cm3 cm-3), Permittivity (ratio), Status/Orientation, Material, Particle size range, Porosity (m3 m-3), Particle density (g cm-3), Bulk density (g cm-3), Solid Permittivity (ratio), Temperature (°C), Frequency (GHz) for CSV 8 only.

## References
- Key methodological and modeling references across TDR and dielectric studies, including:
  - Topp, Davis, Annan (1980); Robinson et al. various calibration and measurement method papers; Friedmann and Robinson modeling works; Blonquist et al. works on anisotropy and aggregates; González-Teruel et al. 2020; and related methodological guides (WinTDR, immersion methods, etc.).

## Projects and funding
- Primary support from BARD Project IS-2839-97 (Binational Agricultural Research and Development Fund) and USDA/National Capability programs.
- Collaborative funding across Israel, Trinidad, USA, and later UK-SCAPE programme (Natural Environment Research Council) for broader data compilation and usage.