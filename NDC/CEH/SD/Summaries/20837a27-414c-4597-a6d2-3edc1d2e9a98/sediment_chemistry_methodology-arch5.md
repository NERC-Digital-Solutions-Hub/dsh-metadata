# Sediment Geochemistry Methodology

## Aim and scope
- Ensure standardized, well-documented geochemical sediment data from the Rio Santa and Ranrahirca catchments are usable, storable, shareable, and discoverable.
- The dataset includes sample metadata, XRF geochemistry, particle size, and organic matter analyses, with attention to metadata completeness, data formats, and reproducibility.

## Data assets (files and what they contain)
- Sample_codes_and_coordinates.csv
  - List of sample codes, sample types, dates, and sampling locations; notes on multiple samples per site identified by decimals (e.g., A1.1).
- xrf_riosanta.csv
  - XRF results for Rio Santa samples; all data in ppm.
  - Elements: Ca, Sc, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Rb, Sr, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, Ba, La, Ce, Nd, Hf, Ta, Pb, Th, U (Protrace, quantitative) and Na, Mg, Al, Si, P, S, Cl, K (Omnian, semi-quantitative).
  - Triplicate analyses for selected samples (R1/R2/R3 notation).
- xrf_ranrahirca.csv
  - XRF results for Ranrahirca sub-catchment; units in ppm.
  - Same element set as Rio Santa (with minor additions like Hg noted in certain elements).
  - Triplicate analyses as above.
- particle_size_riosanta.csv
  - Particle size data for Rio Santa samples; includes specific surface area (SSA) and percentages of sand, silt, and clay.
- particle_size_ranrahirca.csv
  - Particle size data for Ranrahirca sub-catchment; includes SSA and grain-size fractions.
- organic_matter.csv
  - Loss on ignition data; LOI and total organic carbon (TOC) as percentages.

## Sampling and study design
- November 2019: Samples collected along the Rio Santa main stream and Tablachaca catchment; at river edge to capture recently deposited sediment; multiple samples per site (6–10 per transect); target >400 g per sample; GPS coordinates recorded for repeatability.
- November 2020: Ranrahirca subcatchment sampling; selected to represent variation in land use; minimum of three samples per site (Bank1 exception due to sediment quantity).
- Sampling codes may indicate duplicates or triplicates (e.g., A1.1).

## Sample preparation and analysis workflow
- WD XRF preparation
  - Oven-dry, disaggregate, and sieve samples to <63 μm to standardize grain size and minimize contamination.
  - Mill to uniform particle size (300 rpm, 3 minutes); mix with polypropylene wax binder (Ceridust 6050M S1000) for homogenization.
  - Pelletize at ~150 kN using a pellet press to produce smooth surfaces and reduce shadowing during analysis.
- XRF measurement
  - Analysis on PANalytical Axias max instrument.
  - Data acquired with Omnian (semi-quantitative) and Protrace (quantitative) software.
  - Triplicate measurements for a random selection of samples to assess accuracy and precision.
- Particle size analysis
  - Sub-sample <63 μm used for laser diffraction (Malvern MS2000) analysis.
  - Digestion in hydrogen peroxide (6%) with acid pre-treatment; multiple cycles and a 24-hour reaction period to ensure complete digestion.
  - SSA calculated assuming spherical particles, using particle density 2.65 g/cm3 and a particle absorption index of 0.775.
  - Analyses run in triplicate with five 30-second measurements per run; extensive washing between samples to minimize cross-contamination.
  - Sodium hexametaphosphate added at analysis start to improve dispersion and reduce particle-particle interactions.
- Organic matter and LOI
  - Loss on ignition (LOI) performed on 2–3 g of <1 mm material.
  - Samples heated to 550°C for 3 hours; LOI expressed as percentage of initial weight; TOC included as percentage in organic matter dataset.

## Data governance, quality assurance, and lineage
- Metadata and data provenance are captured within the described files (sample codes, coordinates, sampling dates, and site details).
- QA measures include triplicate analyses for XRF and repeated particle-size measurements, along with replicates indicated by R1/R2/R3.
- Data are prepared to be uploaded to appropriate portals and catalogues; documentation and dataset updates should reflect data availability, limitations, and any embargoes.

## Data availability and stewardship considerations
- Data publishers should adopt a publishing mindset: ensure datasets meet user needs, with clear metadata, standardized units (ppm for XRF data; SSA and particle-size fractions for size data), and transparent limitations (e.g., incomplete samples, triplicate coverage).
- Clearly document any data handling notes (e.g., Bank1 exception, decimals in sample codes, and replication status) to facilitate discoverability and reuse.

## References (methodology guidance)
- Kitch et al. 2019
- Laceby et al. 2017
- Smith & Blake 2014
- Walling & Woodward 1995