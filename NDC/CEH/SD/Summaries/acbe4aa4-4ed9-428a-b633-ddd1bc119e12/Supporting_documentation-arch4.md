# Feather isotope ratios and sexing of oystercatchers breeding in Iceland

- Study scope and purpose
  - Longitudinal field study in Iceland (summer seasons 2013–2017) examining migratory strategies of oystercatchers (Haematopus ostralegus).
  - Adults were captured on nests, uniquely marked, and samples were taken for stable isotope analysis and molecular sexing to infer wintering ecology and sex composition.

- Data assets (two CSV files)
  - OystercatcherFeatherIstotopes.csv
    - Contains isotope data for 552 oystercatchers caught and sampled during breeding.
    - Key variables: Year (2013–2017), Individual ID, d15N, d13C, Status (Migrant, Unknown, or Resident), WinterLocation (country).
    - Isotopes reflect diet/habitat during the wintering period when chest feathers grew.
  - OystercatcherSexing.csv
    - Contains DNA-derived sex data for 321 oystercatchers caught and sampled during breeding.
    - Key variables: Individual ID, DNA-derived sex.

- Sampling and processing details
  - Feather sampling: 4–5 chest feathers per individual; feathers grown on wintering grounds.
  - Isotope analysis: feathers washed (2:1 chloroform/methanol), dried, cut, weighed (0.45–0.55 mg), wrapped in tin capsules, analyzed by a Costech elemental analyzer coupled to a Thermo Scientific Delta XP IRMS.
  - Isotope reporting: δ13C (V-PDB standard) and δ15N (AIR N2 standard), expressed in ‰.
  - Quality control: internal standard (collagen) replication yielded measurement errors of 0.2‰ for δ13C and 0.1‰ for δ15N.
  - Sexing method: DNA extracted from blood (ammonium acetate protocol) and sex determined using Fridolfsson & Ellegren (1999) universal molecular sexing method.

- Data structure and linkages
  - Each dataset uses Individual ID as the primary key, enabling linking isotopic data with sexing data for the same birds (where available).
  - Temporal coverage spans 2013–2017; geographic scope limited to lowland areas in southern and western Iceland for sampling.

- Data quality, gaps, and limitations
  - Spatial granularity: WinterLocation provided at country level rather than precise coordinates.
  - Status classification (Migrants, Unknown, Resident) depends on winter observations and may carry uncertainty.
  - Subsample for sexing (321 of 552); potential biases from non-overlapping samples between isotopes and sexing datasets.
  - Data reflect specific life-history periods (wintering phase for feather growth) and may not capture annual variation beyond the study window.

- Provenance and usage notes
  - Data contributed as supporting information for NEERC Grant NE/M012549/1: Environmental and demographic drivers of migratory strategies in birds.
  - Study design and analytical workflow detailed to support reproducibility and reuse in migratory ecology analyses.
  - Potential uses: integrated analyses of migratory strategies combining isotopic ecology with genetic sex data; cross-year comparisons; assessments of sex- and season-specific movement patterns; data integration with broader datasets on wintering grounds and migration timing.

- Relevance for data leadership and governance
  - Demonstrates clear data linkage across multiple data modalities (isotopes and molecular sexing) through a unique ID, enabling data product development (e.g., metadata-rich, linked datasets).
  - Highlights the need for explicit metadata on sampling context, measurement methods, quality controls, and data provenance to support discoverability, reuse, and cross-institution collaboration.
  - Illustrates typical challenges in ecological data (granularity, coverage gaps, and multi-source data fusion) that data leaders should address through standardized metadata, data dictionaries, and clear data stewardship practices.