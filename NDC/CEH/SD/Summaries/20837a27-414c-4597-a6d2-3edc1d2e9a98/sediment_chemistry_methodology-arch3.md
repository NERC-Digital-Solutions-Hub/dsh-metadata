# Sediment Geochemistry Methodology

## Overview
- Describes how sediment geochemical data were collected, prepared, and analyzed to support environmental health monitoring and policy evaluation.
- Documents the data files, sampling design, laboratory methods, and quality assurance practices used to generate geochemical and particle-size datasets.

## Data files and contents
- Sample_codes_and_coordinates.csv: List of sample codes, sample type, date of sampling, and sample location coordinates; notes that some sites have multiple samples (e.g., A1.1).
- xrf_riosanta.csv: XRF results for Rio Santa catchment samples; elements measured with Protrace (major/minor) and Omnian (semi-quantitative) in ppm.
- xrf_ranrahirca.csv: XRF results for Ranrahirca sub-catchment; same element set and software as Rio Santa.
- particle_size_riosanta.csv: Particle size data for Rio Santa samples; includes specific surface area (SSA), and percentages of sand, silt, and clay.
- particle_size_ranrahirca.csv: Particle size data for Ranrahirca; same parameters as Rio Santa.
- organic_matter.csv: Loss on ignition (LOI) data and total organic carbon (TOC) percentages.
- All samples analyzed in triplicate at selected points to assess instrument accuracy.

## Sampling design and collection
- Sites chosen to reflect variability in local geology and soil type along the Rio Santa main stream and the Tablachaca catchment; Ranrahirca sub-catchment sampled to represent land-use variation.
- Temporal scope: November 2019 (Rio Santa/Tablachaca) and November 2020 (Ranrahirca).
- At each site: multiple samples collected along transects (6–10 per site where possible) to reduce bias; samples ≥400 g when possible.
- Sampling method: collected at the river edge from recently deposited sediment using a plastic spatula; GPS coordinates recorded for repeatability.
- Ranrahirca sampling emphasized land-use variation; minimum of three samples per site (except Bank1 due to limited sediment).

## WD XRF analysis (Geochemical composition)
- Preparation: oven-dry, disaggregate, and sieve to <63 μm to standardize grain size and focus on suspended sediment range.
- Milling: samples milled at 300 rpm for 3 minutes to homogenize particle size; a polypropylene wax binder added and mixed; pressed into aluminum cups at ~150 kN.
- Instrument: PANalytical Axias max WD XRF.
- Data processing: Omnian software provides semi-quantitative data; Protrace provides quantitative data; major and minor elements reported in ppm.
- Replicates: triplicate pellets produced for random samples to assess accuracy and precision; at least six random samples analyzed as triplicates.

## Particle size analysis
- Sub-sampling: a <63 μm sub-sample analyzed by laser diffraction (Malvern MS2000) in wet suspension; triplicate preparation per sample.
- Digestion: 3 g of material treated with 6% hydrogen peroxide (H2O2) at room temperature for 24 hours, then heated (80°C) with additional 3 ml H2O2 and further digestion as needed.
- SSA estimation: specific surface area calculated assuming spherical particles, density 2.65 g/cm3, particle absorption index 0.775.
- Measurements: five runs per sub-sample in wet suspension, yielding 15 measurements per sample; each sample analyzed in triplicate.
- Contamination control: two-cycle wash at the start and a triple-cycle wash after all three vials of a sample have been analyzed to minimize cross-contamination.
- Pre-treatment: sodium hexametaphosphate added to aid dispersion.

## Loss on ignition (LOI)
- Organic matter content determined by LOI: 2–3 g of <1 mm material weighed, heated to 550°C for 3 hours, then weighed after cooling.
- LOI percentage used to represent organic matter content (and TOC data captured where provided).

## Data quality, governance, and references
- Replication and standardized preparation steps employed to ensure reproducibility and comparability across sites and datasets.
- Data sources and methodological references support the interpretation of sediment geochemistry and particle-size characteristics:
  - Kitch et al. 2019; Laceby et al. 2017; Smith & Blake 2014; Walling & Woodward 1995.