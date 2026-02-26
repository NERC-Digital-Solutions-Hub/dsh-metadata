# Spatial datasets of radionuclide contamination in the Ukrainian Chernobyl Exclusion Zone

## Scope and Content
- Describes soil and particle contamination datasets around the Chernobyl Exclusion Zone (CEZ), Ukraine, with multiple interconnected data streams.
- Key components:
  - Soil sampling (approximately 1,200 sites, 1995–1997; grid-based, denser spacing (100–500 m) near the western fuel-particle trace).
  - Pu isotope measurements (82 samples along main release traces; 12 additional samples in 2000; some samples analyzed at depths).
  - Pu depth profiling (selected cores sectioned to multiple depth intervals up to 30 cm; one core to 110 cm).
  - Hot particles dataset (fuel and condensed particles; extensive historic collections from 1987–1996; burn-up values; additional particles from inside the reactor Shelter; data also includes Polish particles for comparison).
  - Soil sampling and preparation (115 samples; envelope sampling method; 0–30 cm depth; 90Sr and gamma-emitting nuclides measured).
  - Estimation of remaining fraction of fuel particles (D_FP) via exchangeable vs total Sr-90 fractions; use of 85Sr tracers; gamma analyses for co-measured nuclides; notes on data where 90Sr leaching is significant.
  - 15.20 etc. radionuclide activity concentrations by burn-up values (Table 3, dataset literature values).
  - Ivankiv region survey (2014): 3,389 grid-identified points; ambient dose-rate measurements at 1 m and 0.1 m heights; ~10 m GPS accuracy; 540+ soil samples; 90Sr and gamma analyses; natural radionuclide baselines provided.
- Geographic scope includes the Ukrainian CEZ, with additional data from Poland for cross-regional context.

## Spatial and Temporal Coverage
- Spatial:
  - CEZ around the ChNPP, including western fuel-particle trace, and northern/southern traces; Ivankiv region (Ivankiv district) survey.
- Temporal:
  - Soil sampling and radiochemical analyses conducted mainly 1995–1997.
  - Pu isotope sampling extended with data from 2000 and 2014 Ivankiv survey.
  - Hot-particle data span 1987–1996 (with supplementary Polish datasets and literature augmentation).
- Coordinate reference: GPS coordinates using WGS-84; typical accuracy around 100 m (with some systematic deviations noted).

## Data Quality, Methods and QA
- Analytical methods:
  - Gamma spectrometry with HPGe detectors; 1 L Marinelli geometry; calibration with spiked standards; typical counting times ~1 hour (longer for low-activity samples).
  - Radiochemical separation for 90Sr/90Y; use of low-background beta counting for 90Sr; removal of interfering Cs-137 via radiochemical cleanup.
  - Pu isotopes measured by alpha-spectrometry after chemical separation; use of tracers (236Pu/242Pu) to determine chemical yields.
  - Depth profiling uses layered sampling and consistent lab protocols across sites.
- Quality assurance:
  - Replicate sub-sample analyses; acceptance criterion (Cmax − Cmin)/(Cmax + Cmin) ≤ 0.15 for Cs-137 in sub-samples; if not met, bulked and reanalyzed.
  - ISO/IEC 17025 proficiency testing cited; QA procedures and standardized methods (e.g., ISO 18589-5:2009 for 90Sr analysis in soils).
  - Background corrections, calibration, and traceable standards documented.
- Data characteristics and handling:
  - Some negative values occur (treated as zero for practical use).
  - Uncertainties: target errors less than 30% (95% CI) for gamma measurements; radiochemical yields tracked with tracers.
  - Tables and depth-resolved data include multiple isotopes (e.g., 40K, 226Ra, 232Th, 137Cs, 90Sr, Pu isotopes, 154Eu, etc.) and fuel-particle specific metrics (burn-up values).

## Data Model, Variables and Units
- Core variables:
  - Radionuclide activities: typically in Bq/kg (soil) or Bq/g (fuel particle context); some 90Sr activity derived via 90Y equilibrium methods.
  - Depths for profiling: 0–2 cm, 2–4 cm, … up to 30 cm (and one core to 110 cm with 10 cm slices).
  - Spatial identifiers: sampling points with GPS coordinates (WGS-84).
  - Particle type: fuel vs condensed; burn-up values (MW·d/kg) for fuel particles.
  - Ratios and indicators: 90Sr:154Eu ratios used to infer leaching and fuel weathering; 90Sr leachability (D90Sr) and 85Sr exchange fractions (A_sol, A_res) feeding into remaining-fuel-particle estimates (D_FP).
- Datasets include numerous radionuclides and derived metrics (e.g., fraction of undissolved fuel particles, leaching fractions, depth-distribution data).

## Provenance, Standards and References
- Data assembled from a range of studies led by Kashparov and collaborators; extensive references spanning 1987–2017.
- Standards and methodologies cited include:
  - Gamma-ray spectrometry calibration and QA (HPGe detectors; efficiency calibrations).
  - Radiochemical separations and traceability (using tracers like 236Pu/242Pu, 85Sr; ISO/IEC 17025).
  - ISO 18589-5:2009 for 90Sr analysis in soils; general soil analysis standards (GOST equivalents cited in the text).
- Primary dataset published in a formal data centre entry (NERC Environmental Information Data Centre) with DOI: 10.5285/782ec845-2135-4698-8881-b38823e533bf (2017).

## Accessibility, Reuse and Licensing
- Data are curated and hosted within an established environmental data centre (NERC EIDC) and are presented in the context of a data paper with extensive methodological detail.
- Cross-referenced with published literature for broader spatial context (e.g., Poland, surrounding regions) to support comparative analysis.
- Documentation includes detailed methods, QA, and data dictionaries; suitable for reuse in radiological risk assessment, ecological exposure modelling, and historical contamination studies.

## Limitations, Uncertainties and Considerations for Data Stewards
- Data spanning multiple regions and timeframes may involve non-uniform measurement techniques and reporting units; careful harmonization needed for cross-dataset integration.
- Some measurements rely on inference (e.g., remaining-fuel-particle fraction D_FP) with assumptions about leaching and 90Sr distributions; users should consider uncertainty propagation in derived metrics.
- Negative values exist due to measurement and calculation limitations; recommended zero-imputation practices as noted in the data.
- GPS accuracy is site-dependent; systematic deviations (~300 m) were reported for the 100 m accuracy claim at some points; incorporate spatial uncertainty into analyses.
- Data provenance includes a mix of in-situ measurements, core slicing, historical hot-particle datasets, and literature augmentation; clear lineage and versioning are essential for reproducibility.
- Some datasets (e.g., Table 3 radionuclide activity values by burn-up) are historical and may require careful interpretation when combining with newer data.

## Data Stewardship Recommendations
- Maintain rich metadata and data dictionaries describing:
  - Sampling design, grid references, depths, and envelope sampling methodology.
  - Measurement techniques, QA procedures, detectors, calibration standards, and counting times.
  - Unit conventions, coordinate systems, and any conversions performed.
  - Provenance trails linking to source studies and ISO-compliant QA records.
- Preserve raw measurements alongside processed/derived values to enable reprocessing with updated methods.
- Implement stable, citable DOIs for each data stream and versioning to support long-term discoverability and reuse.
- Provide guidance on appropriate use cases, uncertainties, and recommended data integration approaches with other radionuclide datasets.
- Ensure licensing terms are explicit to support broad scientific reuse, including cross-border data sharing with Poland and other regions.