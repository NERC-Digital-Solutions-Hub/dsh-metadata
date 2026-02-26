# Supporting documentation

## Data overview
- Dataset describes laboratory measurements of the apparent permittivity (dielectric constant) of granular media and soils as a function of volumetric water content (VWC).
- Measurements cover wetting, drainage, or both, using time domain reflectometry (TDR) and, for some samples, frequency-domain analysis with a network analyzer.
- Data collected over approximately 1998–2006 across multiple sites: Israel (Volcani Centre), Trinidad (University of the West Indies), and the USA (Utah State University).
- Goals include understanding how factors such as geometry, packing, particle size and shape, temperature, and aggregation affect dielectric response; data support testing models of the permittivity–water content relationship.

## Datasets included
- There are 8 CSV sheets, with 11 columns each (12 columns for csv8); missing values are NA.
- Common structure across sheets: ID, Description, VWC, Permittivity, Status/Orientation, Material, Particle size range, Porosity, Particle density, Bulk density, Solid Permittivity, Temperature, (and Frequency for csv8).
- Datasets represent a range of materials and conditions:
  - 1_3_phase_measurements.csv: Israeli soils (sandy loam, vertisol) and two natural soils tested during wetting/drying; 25°C ±0.5°C.
  - 2_2_phase_measurements.csv: Two granular materials (glass beads and quartz grains); shear cell and coaxial TDR setup.
  - 3_Particle_size_sand_glass.csv: Glass beads and quartz sand; various monosized and mixed-size fractions; parallel-plate TDR cell; detailed packing and water-content control.
  - 4_Temperature_sand_glass.csv: Temperature-controlled measurements at Trinidad; warming steps with repeated TDR readings.
  - 5_Mica_orientation.csv: Anisotropy study on phlogopite mica with measurements in two orientations; solid permittivity derived via immersion method.
  - 6_Aggregate Samples.csv: Four aggregated porous media (zeoponic, turface, profile, pumice); 950 cm3 cells; frequency-domain data optional (csv8).
  - 7_Soil_aggregates.csv: Similar methods to 6, focusing on soil aggregates.
  - 8_Wasatch_soil.csv: Wasatch soil; includes frequency-domain measurements via VNA; multiple bulk densities achieved by packing adjustments.

## Methods and instrumentation
- Time Domain Reflectometry (TDR)
  - Instrument: Tektronix 1502B (or 1502C) TDR; connected to PC; software: WinTDR or alternatives (Heimovaara and de Water, Or et al.).
  - Calibration: electrodes calibrated for effective length using deionized water and air; calibration parameters t0 and Le derived.
  - Temperature during TDR: typically 25°C ± 0.5°C; cell designs use parallel-plate transmission lines for uniform field distribution.
  - Measurement cells: rectangular or cylindrical plexiglass, ~950 cm3 volume; parallel-plate electrodes (2.5 cm x 15 cm; 2 cm spacing).
  - Wetting/drying: samples packed dry, then water added or drained; water content controlled by mass/volume; cells reused with careful packing and drainage.
  - Notable design details include methods to minimize air entrapment, use of ceramic cups or sintered membranes for drainage, and precise porosity verification.
- Frequency-domain measurements (VNA)
  - Instrument: Vector Network Analyzer (HP 8753B) with open-ended coaxial dielectric probe (HP 85070B) covering 1 MHz–6 GHz.
  - Calibration: standards including air, deionized water, short; calibration software per probe manual.
  - Data yield: complex permittivity derived from S11; supports comparison with TDR-based measurements.
- Solid-phase permittivity
  - Measured via dielectric immersion method to obtain solid permittivity values for materials (e.g., quartz 4.7; mica solid permittivity ~5.8).
- Materials and cells
  - Porous media include artificial aggregates (zeoponic, turface, profile, pumice) and natural soils (Kidman, Hyrum, Wasatch, Sarid soils, etc.).
  - Anisotropy studies (mica) required careful packing orientation to align the EM field with particle axes.

## Data structure and units
- Each data sheet uses a consistent layout with 11 columns (12 for csv8); NA indicates missing values.
- Key columns:
  - ID number, DESCRIPTION
  - VWC, VWC DESCRIPTION (cm3 cm-3)
  - Permittivity, DESCRIPTION (ratio)
  - Status_Orientation (wetting/drying; orientation for anisotropy in csv5)
  - Material (text)
  - Particle size range (text)
  - Porosity (m3 m-3)
  - Particle density (g cm-3)
  - Bulk density (g cm-3)
  - Solid Permittivity (ratio)
  - Temperature_oC (°C)
  - Frequency_GHz (GHz) (csv8 only)
- Data capture includes specific experimental conditions and contextual descriptors to support reproducibility and secondary analyses.

## Quality control and provenance
- Temperature control maintained (typical ±1°C or better).
- Deionized water used; calibration against air and water; length calibrations using standard methods.
- Repeated measurements and careful packing to ensure consistent sampling volume and density.
- Calibration and measurement procedures are described in associated references, ensuring traceability to established methods.

## Project background and funding
- Project scope: approximately 10 years investigating the dielectric response of porous media to water content and the influence of geometrical factors.
- Key questions addressed included dielectric response during wetting/drying, effects of packing density, particle size and shape, temperature effects, porosity changes due to aggregation, and disturbance/repacking.
- Funding and collaboration:
  - BARD (Binational Agricultural Research and Development Fund): Project IS-2839-97; contributions from Volcani Center (Israel).
  - USDA/NRI; Utah Agricultural Experiment Station; Utah State University (USA).
  - University of the West Indies (Trinidad) and UK-SCAPE programme (NE/R016429/1) supporting data compilation.
- Teams involved across Israel, Trinidad, and Utah, with leadership by Shmulik Friedman (Israel), David Robinson (Trinidad), and Scott Jones (USA).

## Potential uses and relevance for data support
- Supports modeling and validation of the permittivity–water content relationship in coarse-textured, layered, or aggregated porous media.
- Enables cross-comparison between time-domain and frequency-domain dielectric measurements.
- Allows exploration of anisotropy effects (mica study) and the impact of particle size distribution, aggregation state, and packing on dielectric properties.
- Provides a rich dataset for developing or testing mixing models and calibration curves for soil moisture sensing in diverse materials and conditions.
- Useful for data curation workflows requiring detailed metadata, calibration histories, and provenance for reproducibility and reuse. 

## References
- Blonquist Jr, J.M., Jones, S.B., Lebron, I. and Robinson, D.A., 2006.
- Blonquist Jr, J.M., Robinson, D.A., Humphries, S.D. and Jones, S.B., 2011.
- Friedman, S.P., 1998.
- Friedman, S.P. and Robinson, D.A., 2002.
- González-Teruel, J.D. et al., 2020.
- Heimovaara, T.J., 1993; Heimovaara, T.J., and E. de Water, 1993.
- Or, D. et al., 2003; Or et al., 2003.
- Topp, G.C. et al., 1980.
- Robinson, D.A. 2004; Robinson, D.A. and Friedman, S.P., 2001; Robinson, D.A. et al., 2003; Robinson, D.A. et al., 2005.
- Von Hippel, A.R., 1954.