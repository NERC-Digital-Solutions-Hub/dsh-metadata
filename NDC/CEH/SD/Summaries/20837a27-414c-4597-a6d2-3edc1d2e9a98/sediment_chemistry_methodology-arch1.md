# Sediment Geochemistry Methodology

## Overview
- Describes the methodology for collecting, preparing, and analyzing sediment samples from the Rio Santa and Ranrahirca catchments.
- Produces datasets on geochemical composition (XRF), particle size, and organic matter (LOI) to support analyses of sediment sources, transport, and environmental implications.

## Sampling and Data Files
- Sampling dates:
  - November 2019: Rio Santa main stream and Tablachaca catchment.
  - November 2020: Ranrahirca subcatchment.
- Site and sampling approach:
  - Samples taken at river edges where sediment had recently deposited.
  - 6–10 samples per site along transects; each sample >400 g when possible.
  - GPS coordinates recorded for repeatability.
  - Sample_codes_and_coordinates.csv lists sample codes, types, dates, and coordinates; decimal points in codes indicate multiple samples at the same point.
  - Ranrahirca sampling aimed to capture land-use variation; minimum three samples per site (Bank1 exception).

## Laboratory Sample Preparation
- Pre-analysis processing:
  - Oven-dried, disaggregated; sieved to <63 μm to standardize grain size and focus on suspended-sediment range.
  - Milled at 300 rpm for 3 minutes to achieve homogeneous particle size.
  - Wax binder added, mixed, then pressed into aluminum cups at ~150 kN to form smooth pellets.
- Purpose:
  - Reduces contamination and shadowing effects during XRF analysis; ensures uniform surface for WD XRF.

## Wavelength Dispersive X-ray Fluorescence (WD XRF) Analysis
- Instrument and data:
  - PANalytical Axias max WD XRF instrument.
  - Data reported in ppm; analyses performed with Omnian (semi-quantitative) and Protrace (quantitative) software.
- QA/replicates:
  - Triplicate pellets produced for at least six randomly selected samples to assess accuracy and precision.
  - Triplicate analyses included as part of quality assurance.

## Particle Size Analysis
- Sub-sample and preparation:
  - Sub-sample of <63 μm material used for laser diffraction (Malvern MS2000) analysis.
  - Digested in hydrogen peroxide (6%) in steps to ensure complete reaction; samples prepared in triplicate.
  - Suspensions analyzed in five runs per sample (30 s each) to obtain 15 measurements per sample.
- SSA calculation:
  - Specific surface area (SSA) estimated from laser results using particle absorption index 0.775 and density 2.65 g/cm³, assuming spherical particles.
- Dispersal and contamination control:
  - Sodium hexametaphosphate added as a dispersant.
  - Extensive washing cycles between analyses to minimize cross-contamination.

## Loss on Ignition (LOI)
- Organic matter content measured via LOI:
  - 2–3 g of <1 mm material placed in crucibles; initial weights recorded.
  - Samples heated to 550°C for 3 hours; post-heating weights recorded after cooling.
  - LOI expressed as a percentage based on weight loss.

## Datasets and Outputs
- Data files:
  - sample_codes_and_coordinates.csv: sample codes, types, dates, locations.
  - xrf_riosanta.csv: XRF results for Rio Santa samples (ppm; major/minor elements via Omnian and Protrace).
  - xrf_ranrahirca.csv: XRF results for Ranrahirca samples (ppm; major/minor elements via Omnian and Protrace).
  - particle_size_riosanta.csv: particle size data for Rio Santa samples (including SSA, % sand/silt/clay).
  - particle_size_ranrahirca.csv: particle size data for Ranrahirca samples (including SSA, % sand/silt/clay).
  - organic_matter.csv: LOI and TOC data (percentages).
- Data interpretation:
  - XRF data provide elemental concentrations (ppm) for major and minor elements.
  - Particle size and SSA data aid in understanding sediment transport and surface area-related processes.
  - LOI/TOC data indicate organic matter content in sediments.

## References and Method Justifications
- Kitch et al. 2019; Laceby et al. 2017; Smith & Blake 2014; Walling & Woodward 1995 underpin method choices for:
  - Grain-size standardization (<63 μm) to compare suspended sediments.
  - Pellet preparation and XRF analysis to minimize measurement biases.
  - Particle size analysis and SSA estimation methodologies.
  - LOI as a proxy for organic matter content in sediments.