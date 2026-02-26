# Supporting documentation

## Overview
- Dataset of measurements for soluble, adsorbed, and organically bound 99Tc concentrations in soils after laboratory contamination with 99TcO4 and incubation for 897 days.
- Addresses long-term bioavailability of Technetium-99 (half-life ~213,000 years) in aerobic soils under temperate conditions.
- Aims to quantify transformation kinetics as a function of soil properties and land use (arable, grassland, moorland/woodland) to inform environmental fate models.

## Data scope and experimental design
- 20 topsoil samples (0–15 cm) from central England; multiple locations per soil type.
- Land uses represented: arable, grassland, moorland, woodland.
- Soils characterized for pH (CaCl2 extraction) and organic carbon content (C content via CNS analyzer); a detailed table lists location, coordinates, organic C %, and pH.
- Soils contaminated with NH499TcO4 to ~108 µg 99Tc per kg dry soil; mixed uniformly and distributed into three microcosms per soil.
- Microcosms incubated in darkness at 10.0 ± 1.0 °C for 897 days (Nov 2014–May 2017).

## Sequential extraction and data structure
- At each sampling time, ~4 g soil subjected to a three-step sequential extraction to partition 99Tc into pools:
  - Soluble Tc: extracted with 20 mL 0.01 M KNO3 (mimics pore water).
  - Specifically adsorbed Tc: extracted with 20 mL 0.16 M KH2PO4 (competes for adsorption sites on Fe/Al/Mn oxides).
  - Organically bound Tc: dissolved with 10% tetramethylammonium hydroxide at 90 °C for 14 h (targets Tc associated with humic/fulvic acids).
- Results reported as concentrations in µg 99Tc per kg dry weight (DW) for each pool; data may have missing values (denoted by -).

## Analytical methods
- ICP-MS (iCAP-Q) with collision-cell using He; 10 ms dwell time, 150 scans per sample.
- Sample introduction via autosampler with ASXpress and PFA-ST nebuliser.
- Internal standards: Ge, Rh (10 µg/L) and Ir (5 µg/L) in 2% HNO3; additional Ir and Re (5 µg/L) in 1% TMAH.
- Calibration with radioactive standard NIST SRM 4288B (99TcO4− in 0.001 M KOH) at 0.5, 1, 5, 10, 25 µg/L.

## Data provenance and metadata
- Time points correspond to incubation days after contamination.
- Tables (Table 1: soil details; Table 2: extraction scheme) accompany the data, providing context for interpretation and cross-site comparisons.
- All measurements tied to specific soil IDs and their corresponding land use and physico-chemical properties.

## Data uses and implications
- Enables modeling of long-term 99Tc bioavailability in aerobic soils under temperate conditions.
- Facilitates understanding of how soil properties (e.g., pH, organic carbon) and land use influence Tc speciation and mobility.
- Supports comparative assessments of radiochemical partitioning across soil types and management practices.

## Data quality, limitations, and reuse considerations
- Standardized contamination, incubation, and fractionation protocols enhance reproducibility.
- Long duration and finite sample set (20 soils) may limit generalizability; some data are missing.
- Clear documentation of procedures and analytical calibration supports reuse, cross-study comparisons, and model development.