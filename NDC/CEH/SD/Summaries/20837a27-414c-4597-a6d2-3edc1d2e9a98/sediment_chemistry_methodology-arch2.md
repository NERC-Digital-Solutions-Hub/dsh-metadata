# Sediment Geochemistry Methodology

- Purpose and scope
  - A standardized methodology to assess sediment geochemistry in the Rio Santa and Ranrahirca catchments for environmental monitoring and policy evaluation over time.
  - Emphasizes data quality, comparability, and transparent documentation to support long-term environmental health assessments.

## Files and data structure
- Sample_codes_and_coordinates.csv
  - Codes, sample types, collection dates, and coordinates; notes indicate multiple samples per site (e.g., A1.1) for repeatable sampling.
- xrf_riosanta.csv
  - XRF results for Rio Santa catchment; elements quantified with Protrace (ppm, major/minor) and Omnian (semi-quantitative).
- xrf_ranrahirca.csv
  - XRF results for Ranrahirca sub-catchment; elements quantified with Protrace and Omnian; includes Hg and other elements.
- particle_size_riosanta.csv
  - Particle size data for Rio Santa samples; includes specific surface area (SSA) and sand/silt/clay fractions.
- particle_size_ranrahirca.csv
  - Particle size data for Ranrahirca sub-catchment; includes SSA and grain fractions.
- organic_matter.csv
  - Loss on ignition data; includes LOI and total organic carbon (TOC) as percentages.

## Sample collection
- Timing and scope
  - Rio Santa main stem and Tablachaca catchment: November 2019; Ranrahirca subcatchment: November 2020.
  - Sites chosen to reflect local geology and soil variability; multiple samples per site to capture variability.
- Collection method
  - Samples at river edge where sediment deposited; collected with plastic spatula to minimize contamination; GPS coordinates recorded.
  - 6–10 samples along transects per site when possible; target weight >400 g for fine sediment analysis.
  - Ranrahirca: minimum of three samples per site to represent land use variation; exceptions noted (e.g., Bank1).

## Sample preparation and WD XRF analysis
- Preparation for XRF
  - Oven-dried, disaggregated, and sieved to <63 μm to standardize grain size and focus on suspended sediment range.
  - Milling at 300 rpm for 3 minutes to homogenize; wax binder added; pellets pressed at ~150 kN for smooth surfaces and reduced shadowing.
- XRF measurement
  - WD XRF on PANalytical Axias max instrument.
  - Data processed with Omnian (semi-quantitative) and Protrace (quantitative) software.
  - Triplicate analyses performed on randomly selected samples to assess accuracy/precision (three pellets per sample for at least six samples).
  - Reported in ppm; triplicates help quantify instrument performance and reproducibility.

## Particle size analysis
- Sub-sample handling
  - Sub-sample of <63 μm material used for laser diffraction analysis (Malvern MS2000) in triplicate; digestion with hydrogen peroxide (6%) following Smith and Blake (2014) protocol.
- Analysis and SSA estimation
  - Five measurements per run; total of 15 measurements per sample; SSA calculated assuming particle sphericity with a particle absorption index of 0.775 and density of 2.65 g/cm3.
  - Wet suspension method with 10 ml sodium hexametaphosphate; dispersion aids results and reduces agglomeration.
  - Cross-contamination control with multi-cycle wash: two-cycle wash, then triple-cycle wash after analyses.
- Data quality
  - SSA and grain-size distributions used to interpret sediment transport and surface area-related processes.

## Loss on ignition (organic matter)
- LOI procedure
  - 2–3 g of <1 mm material combusted for 3 hours at 550°C.
  - Organic content calculated as weight loss, providing LOI and, where applicable, TOC percentages.

## Quality assurance, data management, and references
- QA/QC practices
  - Triplicate measurements for XRF, replicate particle size analyses, and standardized sample preparation to ensure data reliability.
- Data management and accessibility
  - Data organized in standardized files with clear sample coding and coordinates to support reproducibility and potential data portal deposition.
  - Emphasis on storing and uploading created datasets to appropriate portals to enable broader use and data sharing.
- References
  - Methodological basis and validation drawn from key sediment fingerprinting and particle size literature (e.g., Kitch et al. 2019; Laceby et al. 2017; Smith & Blake 2014; Walling & Woodward 1995).