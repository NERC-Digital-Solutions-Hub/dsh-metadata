# Metadata for data associated with dataset 'Measurements of carbon cycling processes in tropical forest soils varying in soil abiotic and biotic properties' (13C_Peru_fluxes.csv, 13C_Peru_soils.csv and 13C_PLFA_incorporation.csv)

- Purpose of the dataset
  - Documents measurements and analyses of carbon cycling processes in tropical forest soils across an elevational gradient, focusing on how soil abiotic and biotic properties influence microbial processing of carbon inputs and priming effects.
  - Includes data on soil properties, microbial community composition (PLFA), respiration rates, and incorporation of 13C-labeled substrates into PLFAs.

- Data files and key variables
  - 13C_Peru_fluxes.csv
    - ActualFlux: basal and substrate-induced respiration (CO2-C, µg g-1 soil dry weight day-1)
    - Basal24/48/168: basal respiration after 24, 48, and 168 hours
    - Subs24/48/168: substrate-derived respiration after 24, 48, and 168 hours
    - Prime24/Prime168: primed SOM-derived respiration after 24 and 168 hours
    - Substrate and SubsName: substrate identity (1=control, 2=xylose, 3=glycine, 4=vanillin, 5=hemicellulose)
    - 13C-related fields (e.g., 13C_SUBSTRATE-derived respiration portions) embedded in calculations
  - 13C_Peru_soils.csv
    - Elevation (m above sea level)
    - Soil abiotic properties: pH, TotC (total carbon), TotN (total nitrogen), Cnratio (C/N), BulkDensity
    - Soil moisture/water holding characteristics (WHC-related) and related measurements
  - 13C_PLFA_incorporation.csv
    - PLFA concentrations and groupings (FPLFA, BPLFA, GP, GN, F:B, GP:GNB)
    - Total PLFA (totPLFA)
    - Substrate-derived 13C incorporation into PLFAs (e.g., FPLFA13C, BPLFA13C, GP13C, GN13C, Unspec13C, TotPLFA13C)
    - 13C incorporation metrics into microbial groups (e.g., fungal- vs bacterial-derived 13C)
    - 13CPLFA_PC: percentage of PLFA 13C labeling
    - PLFA δ13C values for selected PLFAs (relative to injection and derivatisation corrections)

- Study design and sampling
  - Location: ten sites along a tropical elevation gradient on the east flank of the Peruvian Andes (210–3400 m asl) with continuous forest cover.
  - Sampling framework: organic soil layer collected from 5 sub-plots within established 1-ha plots per site; samples stored at 4°C for subsequent experiments.
  - Field measurements: broad range of soil abiotic properties measured (pH, gravimetric moisture, bulk density, total C and N, maximum water holding capacity).
  - Microbial incubations: soils incubated with four 13C-labeled substrates (xylose, glycine, vanillin, hemicellulose) for 7 days at 20°C, with replicates across elevations.

- Substrate incubation and isotopic analyses
  - Substrates added to soils at 0.2 mg C g-1 soil (fwt), with 13C-enrichment to enable tracing.
  - Headspace sampling for CO2 and 13CO2 at 24, 48, and 168 hours; CO2 analyzed by GC-FID with a methaniser; 13CO2 analyzed by IRMS.
  - At experiment end: soils stored for PLFA extraction and δ13C analyses of PLFAs (via GC-MS and GC-C-IRMS).

- PLFA analysis and microbial group inferences
  - PLFAs used as proxies for microbial groups:
    - GP-associated fatty acids for Gram-positive bacteria
    - GN-associated fatty acids for Gram-negative bacteria
    - 18:2ω6,9 and 18:1ω9 for saprotrophic and ectomycorrhizal fungi
  - Calculated metrics:
    - Total PLFA (totPLFA)
    - Ratios: F:B (fungal to bacterial PLFAs) and GP:GN (Gram-positive to Gram-negative)
    - Proportions of individual PLFAs (mol%)
  - 13C labeling in PLFAs (FPLFA13C, BPLFA13C, GP13C, GN13C, Unspec13C, TotPLFA13C) used to determine substrate-derived carbon assimilation into microbial groups.

- Calculations and data processing
  - Isotopic enrichment expressed as δ13C (per mil) for CO2, PLFAs, and total PLFAs.
  - For CO2: percent substrate-derived C calculated using a mixing model that compares δ13C of respired CO2 from controls vs treated soils and the substrate’s δ13C value.
  - Primed SOM-derived C: difference between treated respiration and control respiration, after subtracting substrate-derived respiration.
  - 13C-PLFA calculations: estimate actual incorporation of labeled substrate into PLFAs; compute percent substrate-derived C within each PLFA; calculate microbial carbon-use efficiency (CUE) as the ratio of 13C assimilated into total PLFAs to 13C respired.
  - Data transformations and statistical analyses:
    - Analyses performed in R (version around 2.14.0)
    - Three-way ANOVA to assess effects of substrate, soil, and time on cumulative substrate-derived C and primed C
    - Data square-root transformed (with constant added for primed C)
    - Tukey HSD post-hoc for interactions
    - Two-way ANOVA for microbial incorporation of 13C substrates and effects on microbial groups
  - Quality controls: calibration with standards, blanks, replicate analyses, and daily instrument calibration for δ13C measurements; precision reported as ≥ ±0.2‰ for CO2 isotopes.

- Potential data products and insights for data-use and reuse
  - Data products enabling self-serve exploration:
    - Interactive dashboards linking soil properties and substrate response (substrate-derived respiration, priming magnitude, and CUE)
    - Tables and charts showing substrate effects by elevation and soil type
  - Analyses to reproduce or extend:
    - Three-way and two-way ANOVA results to assess drivers of priming and microbial uptake
    - Isotopic partitioning of respiration (substrate-derived vs native SOM) across substrates, times, and elevations
    - Microbial community response (F:B, GP:GN, PLFA-level shifts) in relation to substrate labeling
  - Guidance outputs:
    - Data dictionaries and transformation scripts to reproduce δ13C corrections, PLFA conversions, and CUE calculations
    - Documentation for replicating the mixing-model approach to partition respiration sources

- Context and references
  - Field site and methodological details align with Whitaker et al. 2014 and related literature on microbial substrate assimilation, PMF/PLFA proxies, and stable isotope methods.
  - Includes methodological references for soil analyses, PLFA identification, δ13C correction in PLFA analyses, and statistical approaches (ANOVA, post-hoc tests).

- Considerations and limitations
  - Data derive from a specific tropical elevation transect with 10 sites; generalizability may be bounded by site characteristics and substrate set.
  - Measurements rely on a fixed incubation period and specific incubation conditions (20°C, 75% WHC), which influence respiration dynamics relative to in-situ conditions.
  - Some line items in the metadata (e.g., Prime168 description mappings) indicate complex cross-references between priming timepoints; careful interpretation of variable labels is advised when linking datasets.

- Access and provenance
  - Metadata describes experimental design, data collection, analytical methods, and calculation workflows used to generate the 13C_Peru_fluxes.csv, 13C_Peru_soils.csv, and 13C_PLFA_incorporation.csv datasets.