# Supporting documentation

## Data description
- The data set contains laboratory measurements of the apparent permittivity (dielectric constant) of granular media and soils as a function of volumetric water content, including wetting, drainage, or both.
- Measurements were collected over a 10-year period using Time Domain Reflectometry (TDR) with Tektronix equipment and additional measurements (8) with a network analyser.
- Sites include Israel (Volcani Centre), Trinidad (University of the West Indies), and the USA (Utah State University).
- Soils and porous media span Utah soils (Hyrum, Kidman, Blacksmith Fork, Sawmill, Tony Grove, Wasatch Front) and Sarid soils from Israel; materials include various granular media and aggregated porous media.
- The data address how dielectric response relates to factors such as geometry, packing, temperature, grain size and shape, aggregation, disturbance, and repacking.
- Datasets were compiled by teams led in Israel, Trinidad, and the USA.

## Project background
- Aiming to understand the relationship between dielectric properties and volumetric water content in porous media over about a decade.
- Core questions include: dielectric response during wetting/drying; effect of packing density in two-phase media; impact of particle size, temperature, grain shape/orientation; effects of aggregation and disturbance; and frequency-domain analyses for repacked soils.
- Measurement approaches include time-domain (TDR) and frequency-domain (VNA) techniques to capture permittivity across conditions and materials.

## Measurement methods and instruments
- Time Domain Reflectometry (TDR)
  - Equipment: Tektronix 1502B Metallic Cable Tester; waveguide with a 1 m RG-58 coaxial cable; PC for waveform capture and analysis (software by Heimovaara & de Water, 1993; Or et al., 2003).
  - Calibration: electrode length and travel time corrected using air and deionised water standards; temperature typically controlled around 25°C ±0.5°C.
  - Cell design: rectangular (8×8 cm) or cylindrical (9 cm diameter) plexiglass containers with parallel-plate electrodes (2.5 cm wide, 15 cm long, 2 cm spacing); includes drainage/wetting bases (ceramic cups or sintered membranes).
  - Representative datasets and methods described in associated publications.
- Frequency Domain
  - Equipment: Vector Network Analyser (VNA, Model 8753B) with open-ended coaxial dielectric probe (HP 85070B) and 3.17 cm sample holder; calibration with air, deionized water, shorting block; measurement frequency range 1 MHz–6 GHz.
  - Purpose: determine dielectric properties of clays and clayey soils via reflection (S11) measurements and convert to complex permittivity.
- Additional instruments
  - TRIME instrument used in data set 1.
  - Mica anisotropy experiments used a specialized cell and WinTDR software for waveform analysis.

## Materials, samples, and experimental setups
- Porous media
  - Artificial porous media descriptions and related publications provided.
  - Aggregated porous media included four types: zeoponic (clinoptilolite and apatite), turface, profile, and pumice with varying sizes.
- Soils
  - Utah soils: Kidman (sand), Hyrum (loamy sand), Blacksmith Fork, Sawmill, Tony Grove, Wasatch Front.
  - Israel soil: Sarid vertisol (heavy clay) and Sarid sandy loam (light textured).
- 1_3_phase_measurements.csv
  - Studies two natural Israeli soils (sandy loam and vertisol); preparation involved oven-drying, crushing, and sieving; moisture is applied via CaCl2 solution with redistribution periods.
  - Temperature maintained at 22–24°C; observations include swelling and cracking in the vertisol during drying.
- 2_2_phase_measurements.csv
  - Measures granular materials (glass beads and quartz grains) with different packing and sizes; TDR setup described.
- 3_Particle_size_sand_glass.csv
  - Experiments with two bead sizes (large 450–500 μm and small 45–53 μm) and mixtures; detailed packing and water distribution procedures to compute water-filled porosity and bulk density.
  - Similar procedures for quartz sand with alternate size fractions.
- 4_Temperature_sand_glass.csv
  - Trinidad-based temperature-controlled measurements on wetted sand and glass spheres.
- 5_Mica_orientation.csv
  - Anisotropy measurements using mica with orientation-dependent permittivity; custom cell with parallel-plate electrodes; two packing orientations (vertical and horizontal) to align mica crystals relative to the electric field.
  - Solid dielectric constant of mica determined via immersion methods (5.8).
- 6_Soil_aggregates.csv, 7_Soil_aggregates.csv
  - Measurements on aggregated porous media (zeoponic, turface, profile, pumice) and related soil aggregates; identical TDR-based water content and permittivity measurement approach with four aggregate types.
- 8_Wasatch_soil.csv
  - Wasatch soil measurements with TDR following the aggregate methodology; frequency-domain measurements performed with VNA as described in Section 3.
- Data structure note: All datasets use a consistent measurement framework with careful calibration, drying/wetting protocols, and temperature control.

## Details of data structure and units
- There are 8 CSV sheets; missing values are represented as NAs.
- Common data schema (11 columns; 12 columns for csv 8):
  - ID number
  - DESCRIPTION (identifies experimental manipulation)
  - VWC (cm3 cm−3)
  - VWC description
  - Permittivity (ratio)
  - Permittivity description
  - Status_Orientation (text)
  - Material (text)
  - Particle size range (text)
  - Porosity (m3 m−3)
  - Porosity description
  - Particle density (g cm−3)
  - Particle density description
  - Bulk density (g cm−3)
  - Bulk density description
  - Solid Permittivity (ratio)
  - Solid Permittivity description
  - Temperature (°C)
  - Temperature description
  - Frequency (GHz) [only in csv 8]
- This structure supports traceability from sample to measurement to metadata.

## Quality control and provenance
- Calibration and measurement integrity
  - TDR calibrations using air and deionised water; electrode length corrections applied.
  - Temperature control typically at 25°C ±0.5°C (and other controlled ranges in specific studies).
  - Deionised water used; balances calibrated; network analyzer calibrated with standard references.
- Reproducibility
  - Multiple measurements per sample; detailed procedures for packing, drainage, and re-wetting to achieve consistent water contents.
  - Documentation of cell designs, including dimensions and materials, to enable replication.
- Data provenance
  - Data originate from multiple sites (Israel, Trinidad, USA) and colleagues, associated with published works and project-funded research.

## References and project context
- Core publications underpinning methods and interpretation (examples):
  - Blonquist Jr. et al., 2006; 2011
  - Friedman, 1998; 2002
  - González-Teruel et al., 2020
  - Heimovaara, 1993; Robinson et al., 2003; 2004
  - Or et al., 2003; Topp et al., 1980; Robinson et al., 2003/2005
- Projects and funding
  - BARD Project IS-2839-97; 611/00 (Volcani Center, Israel)
  - USDA funding and Utah Agricultural Experiment Station support
  - UK-SCAPE programme (NE/R016429/1) as part of the UK-SCAPE National Capability

## Governance, sharing, and data stewardship considerations
- Data description and metadata provide rich context for discoverability and reuse; ensure metadata captures:
  - Study site(s), time frame (1998–2006), instruments (TDR, VNA), cell geometry, calibration procedures, sample preparation, and temperature control.
  - Detailed material descriptions (soil names, grain sizes, porosity, densities, solid permittivity) and measurement conditions (Wetting vs. Drying, orientation for anisotropy).
- Data standards and interoperability
  - Align units and definitions across datasets (VWC, Permittivity, Porosity, Densities, Temperature, Frequency).
  - Link to methodological papers for calibration and interpretation (for traceability and reproducibility).
- Data licensing and access
  - The document does not specify licensing; for ongoing sharing, assign a license and repository path to ensure clear reuse rights.
- Data quality management
  - Maintain calibration records, temperature logs, and instrument settings as part of the data package.
  - Provide lineage from sample to measurement, including cell design and packing methods to support replication and meta-analyses.
- Data curation actions recommended for Data Stewards
  - Consolidate a data dictionary that maps each column to its units, permissible values, and provenance notes.
  - Create crosswalks to standardize terminologies (e.g., VWC definitions, permittivity conventions).
  - Store original 8 CSV sheets with a readme detailing the measurement contexts, sample IDs, and site metadata.
  - Consider assigning DOIs or persistent identifiers for dataset components and link to the cited literature.

## Summary for reuse and discovery
- This collection provides a multi-site, multi-method dataset linking dielectric properties to volumetric water content across granular media and soils, including both natural soils and synthetic/aggregated media.
- Key value propositions for Data Stewards:
  - Rich methodological detail enabling reproducibility and cross-study synthesis.
  - Comprehensive metadata on materials, cell design, calibration, and environmental conditions.
  - Longitudinal scope (1998–2006) across diverse geographic sites.
- Potential use cases include validating dielectric mixing models, testing calibration approaches for coarse-textured soils, exploring anisotropy in permittivity (mica studies), and evaluating the influence of particle size distribution and packing on permittivity.