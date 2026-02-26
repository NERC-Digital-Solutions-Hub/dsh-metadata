# Sediment Geochemistry Methodology

- This document describes the data and methodologies used to collect, analyse, and structure sediment geochemistry data from the Rio Santa and Ranrahirca catchments, including data files, sampling, instrument analyses, and processing steps, along with references.

## Data assets and metadata

- Data files and their purpose:
  - sample_codes_and_coordinates.csv: listing sample codes, sampling dates, and GPS coordinates; notes indicate multiple samples at some points (e.g., A1.1).
  - xrf_riosanta.csv: XRF results for Rio Santa catchment samples; elements quantified in ppm via Protrace (major/minor) and semi-quant Omnian.
  - xrf_ranrahirca.csv: XRF results for Ranrahirca sub-catchment; similar elemental scope and software usage as Rio Santa.
  - particle_size_riosanta.csv: particle size data for Rio Santa samples; includes specific surface area (SSA) and sand/silt/clay fractions.
  - particle_size_ranrahirca.csv: particle size data for Ranrahirca sub-catchment; similar contents to Rio Santa.
  - organic_matter.csv: loss on ignition data (LOI) and total organic carbon (TOC) percentages.
- Data characteristics:
  - All XRF data reported in ppm.
  - Elements measured: Ca, Sc, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, Ga, As, Rb, Sr, Y, Zr, Nb, Mo, Ag, Cd, Sn, Sb, Cs, Ba, La, Ce, Nd, Hf, Ta, Pb, Th, U (via Protrace); Na, Mg, Al, Si, P, S, Cl, K (via Omnian).
  - Triplicate analyses (R1/R2/R3) for selected samples to assess precision.
- Data governance notes:
  - Sample types and coordinates are documented; decimal suffixes indicate repeated sampling at the same point.
  - Metadata supports discoverability and re-use, with explicit notes on analytical approaches and software.

## Sampling design and data collection governance

- Sampling scope and timing:
  - Rio Santa main stem and Tablachaca catchment samples collected November 2019; Ranrahirca sub-catchment samples collected November 2020 to capture land-use variation.
- Sampling approach:
  - At each site, 6–10 samples along transects to capture variability; minimum 400 g per sample to ensure adequate fine sediment.
  - In Ranrahirca, sampling selected to represent dominant land-use variability; minimum of three samples per site (except Bank1 due to sediment quantity).
  - GPS coordinates recorded for repeatability; plastic spatula used to minimize metal contamination.
- Sample handling:
  - Samples stored in zip-lock bags; representative sampling along transects to reduce bias.

## Sample preparation for analysis

- WD XRF preparation (for all samples):
  - Oven-dried, disaggregated, and sieved to <63 μm to standardize grain size and limit contamination.
  - Milling at 300 rpm for 3 minutes to achieve a uniform particle size.
  - Wax binder added and mixed; pellets pressed at ~150 kN to produce smooth surfaces for accurate XRF analysis.
- Instrumentation and data capture:
  - PANalytical Axias max XRF instrument.
  - Analyses run with Omnian (semi-quantitative) and Protrace (quantitative) software.
  - Triplicate analyses performed on a random subset of samples to assess accuracy and precision.

## Particle size analysis and surface area estimation

- Sub-sample preparation:
  - <63 μm material used for laser diffraction analysis (Malvern MS2000) after hydrogen peroxide digestion steps.
  - Digestion protocol includes sequential heating and additional peroxide to ensure complete reaction.
- Measurement and data handling:
  - Five runs per sample in wet suspension to capture coarse fractions; triplicate analyses for each sample.
  - SSA estimation assumes particle density 2.65 g/cm3 and sphericity; a particle absorption index of 0.775 used.
  - Sodium hexametaphosphate added to aid dispersion; extensive washing to minimize cross-contamination between samples.

## Loss on ignition and organic content

- LOI/TOC procedure:
  - 2–3 g of <1 mm material weighed per crucible.
  - Heating at 550°C for 3 hours to combust organic matter; masses recorded before and after to determine LOI/TOC.

## Data quality, replication, and validation

- Quality control measures:
  - Triplicate analyses for a subset of samples (R1/R2/R3) to assess instrument accuracy and precision.
  - Random selection of samples for triplicate pellet production to monitor reproducibility.
- Documentation supports traceability from sampling through processing to final geochemical data.

## Data standards, metadata, and reuse

- Data structure and reporting:
  - Elements and methods clearly documented; major vs. minor elements distinguished by Protrace and Omnian software.
  - Sample codes, sampling dates, and coordinates embedded in sample_codes_and_coordinates.csv to support reproducibility and spatial analyses.
- User needs and collaboration:
  - Data organization supports broader data system thinking, with clear pathways for data discovery and potential collaboration across teams or networks working on sediment geochemistry and provenance.
  - Metadata and method details facilitate reuse for fingerprinting, source attribution, or comparative studies.

## Practical considerations and challenges for data leadership

- Coordination and standards:
  - Ensuring consistent data standards across multiple catchments and sampling campaigns to enable cross-site comparisons.
- Data gaps and granularity:
  - Potential data gaps at required granularity if additional sites or repeated sampling are needed for policy-relevant analyses.
- Accessibility and governance:
  - Clear documentation and metadata are essential to overcome potential access limitations and to support long-term data discoverability and stewardship.
- Quality and provenance:
  - Maintaining traceability from sampling through analyses (including triplicate results and software versions) to ensure confidence in results used for decision-making.

## References

- Kitch, J.L., et al. 2019. Understanding the geomorphic consequences of enhanced overland flow in mixed agricultural systems: sediment fingerprinting demonstrates the need for integrated upstream and downstream thinking. Journal of Soils and Sediments.
- Laceby, J.P., et al. 2017. The challenges and opportunities of addressing particle size effects in sediment source fingerprinting: a review. Earth-Science Reviews.
- Smith, H.G. and Blake, W.H. 2014. Sediment fingerprinting in agricultural catchments: a critical reexamination of source discrimination and data corrections. Geomorphology.
- Walling, D.E. and Woodward, J.C. 1995. Tracing sources of suspended sediment in river basins: a case study of the River Culm, Devon, UK. Marine and Freshwater Research.