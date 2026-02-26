# Metadata for data associated with dataset 'Measurements of carbon cycling processes in tropical forest soils varying in soil abiotic and biotic properties' (13C_Peru_fluxes.csv, 13C_Peru_soils.csv and 13C_PLFA_incorporation.csv)

- Overview
  - Metadata and methods describe a study on microbial processing of carbon inputs in tropical forest soils along an elevation gradient in the Peruvian Andes.
  - Field sampling occurred in January 2012 across ten sites with elevations from 210 to 3400 m above sea level.
  - The project investigates how abiotic soil properties and microbial community composition influence carbon mineralization, priming, and carbon-use efficiency (CUE) using 13C-labelled substrates.
  - Data originate from the Maximum Prime study by Whitaker et al. (2014).

- Datasets Included
  - 13C_Peru_fluxes.csv: presumably contains CO2 flux measurements and 13C-derived flux data over time.
  - 13C_Peru_soils.csv: presumably contains soil abiotic properties and substrate-related measurements.
  - 13C_PLFA_incorporation.csv: presumably contains PLFA-based 13C incorporation data for microbial groups.
  - Metadata fields accompany these datasets to describe variables, units, and meanings.

- Data Variables and Metadata (examples of key fields)
  - Location and sampling context
    - Elevation (UNITS = m_asl; DESCRIPTION = metres above sea level)
    - Replicate (DESCRIPTION = replicate)
  - Abiotic soil properties
    - pH (UNITS = soilpH)
    - TotC (Total Carbon, UNITS = %)
    - TotN (Total Nitrogen, UNITS = %)
    - Cnratio (C/N; UNITS = dimensionless)
    - BulkDensity (UNITS = g_cm-3)
    - Total soil moisture and related properties
  - Microbial and PLFA indicators
    - totPLFA (Total PLFA concentration; UNITS = µg_g-1_dwt)
    - FPLFA, BPLFA (Fungal and Bacterial PLFA concentrations)
    - FB (F:B ratio), GP, GN (Gram-positive/Gram-negative bacterial PLFA concentrations)
    - GPGN (GP:GN ratio)
    - Substrate (Substrate; indicates substrate type: 1=control, 2=xylose, 3=glycine, 4=vanillin, 5=hemicellulose)
    - SubsName (Substrate name)
  - Gas measurements and respiration
    - ActualFlux (CO2-C flux; UNITS = µg g-1 soil dwt day-1)
    - Basal24, Basal48, Basal168 (basal respiration after 24, 48, 168 hours)
    - Subs24, Subs48, Subs168 (substrate-derived respiration after 24, 48, 168 hours)
    - Prime24, Prime168 (primed SOM-derived respiration after 24 and 168 hours)
  - Isotopic and PLFA-derived data
    - 13CPLFA13C (13C in PLFAs; UNITS = ng_13C_PLFA-C_g-1_soil_dwt)
    - FPLFA13C, GP13C, GN13C, Unspec13C (13C-labelled PLFA fractions for specific groups)
    - TotPLFA13C (Total PLFA13C)
    - PLFA_RESPC (ratio; carbon-use efficiency indicator for PLFA-derived data)
  - Derived calculations and corrections
    - δ13C values for CO2 and PLFAs
    - Percent substrate-derived C in CO2 and PLFAs
    - Primed C (difference between treated and control respiration minus substrate-derived respiration)
    - 13C incorporation into PLFAs (actual and proportional by microbial group)
    - Microbial carbon-use efficiency (CUE) based on 13C incorporation vs. respiration

- Study Design and Field Sampling
  - Ten sites along an elevation gradient (210–3400 m) with continuous forest cover and diverse vegetation.
  - Organic soil layer collected from 5 sub-plots within each site (1 ha plots), mixed, and stored at 4°C for up to 6 weeks before experimentation.

- Abiotic Analyses and Soil Characterization
  - pH (soil:water, 1:2.5 w:v), gravimetric moisture, bulk density.
  - Total C and N content measured with CN analyzer.
  - Maximum water holding capacity (WHC) calculated from composites of 5 sub-plots per site.

- Microbial Experiments and Substrate Treatments
  - Soils incubated with four 13C-labelled substrates (xylose, glycine, vanillin, hemicellulose) and a sterile water control.
  - Substrates used at 0.2 mg C g-1 soil fwt, with a 75% WHC adjustment and headspace flushed before incubation.
  - Incubation: 7 days at 20°C in the dark.
  - Headspace sampling at 24, 48, and 168 hours for CO2 and 13CO2; soils frozen for PLFA and δ13C analyses.

- Analytical Methods
  - CO2 and 13CO2 quantified by GC-FID; 13CO2 isotopes measured by GC-IRMS.
  - PLFA extraction and analysis by GC-MS; identification of fungal and bacterial markers; calculation of F:B and GP:GN ratios.
  - δ13C values corrected for methylation; PLFA δ13C used to determine substrate-derived C incorporation into microbial groups.

- Isotopic Calculations and Derived Metrics
  - δ13C enrichment used to compute substrate-derived CO2 and PLFA assimilation.
  - Mixing-model approach to partition CO2 respired between substrate-derived and baseline sources.
  - Priming effect calculated as change in total respiration minus substrate-derived respiration.
  - 13C incorporation into PLFAs expressed as both absolute (µg 13C g-1 soil dwt) and as percent of total PLFA, across microbial groups (fungi, GP, GN).
  - CUE calculated as the ratio of 13C assimilated into PLFAs to that respired.

- Statistical Analyses
  - Performed in R (version 2.14.0).
  - Three-way ANOVA to assess main and interaction effects of substrate, soil, and time on cumulative substrate-derived C and primed C.
  - Data transformations (square-root; constant added to primed C).
  - Tukey's HSD for post-hoc comparisons.
  - Two-way ANOVA to examine how microbial community composition affects 13C assimilation (substrate x soil), using metrics such as actual incorporation, relative distribution among microbial groups, and CUE.

- Data Quality, Validation, and Provenance
  - Calibration and quality control for CO2 and δ13C measurements include standards, blanks, and duplicate analyses.
  - Isotopic corrections for preparation steps (e.g., methylation) applied to δ13C PLFA data.
  - Study links to Whitaker et al. (2014) and other cited methodological references for context and reproducibility.
  - Metadata provides explicit units, descriptions, and variable meanings to facilitate discovery and reuse.

- Data Use and Governance Considerations for Data Leaders
  - Rich, well-annotated metadata supports discoverability, reuse, and cross-study comparisons of carbon cycling, priming, and microbial assimilation across elevational gradients.
  - Structure enables integration with broader soil biogeochemistry and microbial ecology datasets.
  - Potential data challenges: complexity of isotopic calculations, need for careful handling of corrections and calibration, and context-specific interpretations tied to tropical montane/lowland soils.
  - Recommended governance actions: assign a DOI, ensure clear data licenses, maintain provenance, and document data standards and ontologies to enable cross-network collaboration and longer-term stewardship.