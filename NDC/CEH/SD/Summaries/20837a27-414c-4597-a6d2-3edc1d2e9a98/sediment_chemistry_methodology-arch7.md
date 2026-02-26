# Sediment Geochemistry Methodology

## Overview
- Presents a geochemical dataset framework for sediment samples from the Rio Santa and Ranrahirca catchments.
- Produces map-ready, geochemically rich data: element concentrations (ppm), particle size metrics, and organic matter indicators to support spatial analysis and interpretation.

## Datasets and Files
- Sample_codes_and_coordinates.csv
  - Contains sample codes, sample type, date of sampling, and coordinates; notes indicate multiple samples at some points (e.g., A1.1).
- xrf_riosanta.csv
  - XRF results for Rio Santa sediments; elements quantified via Protrace (major/minor) and Omnian (semi-quantitative); units in ppm.
  - Triplicate analyses for accuracy (randomly selected samples).
- xrf_ranrahirca.csv
  - XRF results for Ranrahirca sub-catchment; same element set as Rio Santa; includes Hg in this dataset.
- particle_size_riosanta.csv
  - Particle size data for Rio Santa samples; includes specific surface area (SSA) and sand/silt/clay fractions.
- particle_size_ranrahirca.csv
  - Particle size data for Ranrahirca samples; includes SSA and sand/silt/clay fractions.
- organic_matter.csv
  - Loss on ignition (LOI) data; includes TOC as a percentage.
- All datasets are linked by sample codes and coordinates for GIS integration.

## Sampling Strategy
- Sites along the Rio Santa main stem and the Tablachaca catchment were selected to capture lithologic and soil variability.
- Rio Santa sampling conducted November 2019; Ranrahirca subcatchment sampling November 2020.
- At each site: 6–10 samples along a transect to minimize bias; total sample weight targeted >400 g where possible.
- Ranrahirca sampling emphasized land-use representation; minimum of three samples per site; exception at Bank1 due to sediment quantity.
- GPS coordinates recorded for repeatability and spatial analyses.

## Laboratory Methods

- WD XRF sample preparation
  - Oven-dry and disaggregate; screen to <63 μm to standardize grain size and focus on suspended-sediment range.
  - Mill at 300 rpm for 3 minutes to homogenize.
  - Add polypropylene wax binder (Ceridust 6050M S1000); mix 3 minutes at 300 rpm to ensure even distribution.
  - Pelletize to ~150 kN using a pellet press to reduce surface roughness and shadowing during analysis.
- XRF analysis
  - Instrument: PANalytical Axias max WD XRF.
  - Data processed with Omnian (semi-quantitative) and Protrace (quantitative) software.
  - Triplicates performed for a random subset of samples to assess accuracy and precision (three pellets per sample for at least six random samples).

## Particle Size Analysis

- Sub-sample (<63 μm) used for laser diffraction (Malvern MS2000) analysis; analyzed in triplicate.
- Preparation
  - 3 g material with 3 ml hydrogen peroxide (6%) at room temperature; 24 h reaction.
  - Heat treatment at 80°C for 4 hours; repeat addition of hydrogen peroxide for complete reaction.
  - Run five times per sample in wet suspension to obtain 15 measurements, enhancing inaccuracy mitigation for coarser fractions.
  - Use 10 ml sodium hexametaphosphate to aid dispersion.
- SSA calculation
  - Assumes particle density 2.65 g/cm³ and particle absorption index 0.775; SSA computed assuming spherical particles.
- Quality control
  - Analysis performed in triplicate per sample; two-cycle wash between vials and triple-cycle wash after all vials analyzed to minimize cross-contamination.

## Loss on Ignition (LOI) / Organic Matter

- LOI procedure for organic content
  - 2–3 g (<1 mm material) weighed; heated at 550°C for 3 hours; cooled and re-weighed.
  - LOI expressed as percentage; TOC included in LOI interpretation as an organic matter indicator.

## Data Quality and GIS Readiness

- Data linked by sample codes and coordinates to enable spatial mapping of geochemical signatures.
- Multiple sampling at each site supports robust spatial statistics and interpolation.
- Replication (triplicates) and cross-checks (Omnian vs. Protrace) support reliability of element concentrations.
- Standardized grain-size fraction (<63 μm) and documented processing steps facilitate comparability across sites and datasets.

## References
- Kitch, J.L., et al. 2019. Understanding the geomorphic consequences of enhanced overland flow in mixed agricultural systems.
- Laceby, J.P., et al. 2017. Challenges and opportunities of addressing particle size effects in sediment source fingerprinting.
- Smith, H.G. and Blake, W.H. 2014. Sediment fingerprinting in agricultural catchments.
- Walling, D.E. and Woodward, J.C. 1995. Tracing sources of suspended sediment in river basins.