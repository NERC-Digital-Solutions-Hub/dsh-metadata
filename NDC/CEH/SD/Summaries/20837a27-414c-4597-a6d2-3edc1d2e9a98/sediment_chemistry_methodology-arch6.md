# Sediment Geochemistry Methodology

- This document details sampling, preparation, and multi-method analysis of sediment samples from the Rio Santa and Ranrahirca catchments to generate geochemical, particle size, and organic matter datasets.

## Overview of Data and Files
- Data are organized into several CSV files with descriptions and notes:
  - sample_codes_and_coordinates.csv: list of sample codes, types, dates, and GPS coordinates; multiple samples per site identified by decimals (e.g., A1.1).
  - xrf_riosanta.csv: XRF results for Rio Santa samples (ppm).
  - xrf_ranrahirca.csv: XRF results for Ranrahirca samples (ppm).
  - particle_size_riosanta.csv and particle_size_ranrahirca.csv: particle size data including specific surface area (SSA), and sand/silt/clay fractions.
  - organic_matter.csv: loss on ignition (LOI) and total organic carbon (TOC) data (%).
- Sampling occurred November 2019 (Rio Santa) and November 2020 (Ranrahirca) with attention to represent variability in geology, soils, and land use.

## Sampling and Metadata
- Sites along the Rio Santa main stem and Tablachaca catchment; Ranrahirca sampling targeted land-use variation.
- Sampling method:
  - Edge-of-river collection with a plastic spatula to minimize metal contamination; GPS coordinates recorded.
  - 6–10 samples per transect at each site to reduce bias; each sample region weighed >400 g when possible.
  - Ranrahirca used a minimum of three samples per site; Bank1 excluded due to limited sediment.
- Sample handling:
  - Multiple samples per site; details encoded in sample_codes_and_coordinates.csv.

## Sample Preparation
- Size selection: oven-dry, disaggregate, and sieve to <63 μm to standardize the fraction representing suspended sediment.
- Milling and binding: milled at 300 rpm for 3 minutes; mixed with polypropylene wax binder; milled again; then pressed into aluminium pellets at ~150 kN to ensure smooth surface and reduce shadowing in XRF.

## WD XRF Analysis (Geochemical Data)
- Instrument: PANalytical Axias max, analyzed with WD XRF.
- Data processing:
  - Omnian: semi-quantitative elemental dataset.
  - Protrace: quantitative elemental dataset.
- QA/precision:
  - Triplicate analyses on a random subset to assess accuracy and precision; at least six samples analyzed in triplicate (three pellets per sample).
- Elements measured (ppm) include major and trace elements (examples listed in notes, such as Ca, Fe, Zn, Pb, U, etc.).
- Outputs: xrf_riosanta.csv and xrf_ranrahirca.csv containing element concentrations.

## Particle Size Analysis
- Sub-sample (<63 μm) used for laser diffraction (Malvern MS2000).
- Sample preparation:
  - 3 g material with 3 ml H2O2 6% at room temp for 24 h, then heat cycle up to 80°C with additional H2O2, then another 4-hour cycle.
  - Dispersion aided by 10 ml sodium hexametaphosphate.
  - Analysis performed in triplicate to improve representativeness; five measurements per run for a total of 15 measurements per sample.
- SSA estimation:
  - Assumes particle absorption index 0.775 and density 2.65 g/cm3, with spherical particle assumption.
- Instrument cleaning:
  - Two-cycle wash between samples, followed by a triple-cycle wash after analysis of all vials for a given sample to minimize cross-contamination.

## Loss on Ignition (Organic Matter)
- LOI/TOC assessment:
  - 2–3 g of <1 mm material heated to 550°C for 3 hours; weight loss recorded to determine organic matter content (LOI). 
  - TOC data reported alongside LOI in the organic_matter.csv.

## Data Products and Use
- Outputs enable cross-dataset analysis:
  - Geochemical fingerprinting (XRF) across catchments.
  - Particle size distribution and SSA data for sediment transport and surface area considerations.
  - Organic matter content (LOI/TOC) for sediment quality and carbon studies.
- Documentation supports reproducibility, data provenance, and potential re-use for broader data-driven exploration and policy support.

## Quality Assurance and References
- QA measures include triplicate analyses for XRF and particle size measurements to ensure data reliability.
- Methodological references underpinning particle size analysis and sediment fingerprinting:
  - Kitch et al. 2019; Laceby et al. 2017; Smith & Blake 2014; Walling & Woodward 1995.