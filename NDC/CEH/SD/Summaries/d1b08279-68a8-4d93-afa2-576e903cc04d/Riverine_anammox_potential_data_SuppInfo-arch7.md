# General information: This dataset contains results from slurry incubations with 15N-labelled substrates.

- Purpose and scope
  - Results from slurry incubations using 15N-labelled substrates to study nitrogen transformations in aquatic sediments.
  - Provides measurements relevant to anammox, denitrification, and related N2 production under both anoxic and oxic conditions.
  - Incubations performed with time-series sampling to infer potential activities rather than in vivo rates.

- Experimental design
  - Slurry types and conditions
    - Anoxic slurries in 3 mL gas-tight vials: 1 mL wet sediment + 1 mL synthetic river water; N2 headspace (N2) without oxygen.
    - Oxic slurries in 12 mL gas-tight vials: 2.5 mL wet sediment + 3 mL synthetic river water; air headspace.
  - Substrates and amendments
    - Various combinations of 14N (natural abundance) and 15N-labelled substrates.
    - N-amendments injected via septa (100 µL) with target post-injection nitrate or ammonium concentrations (e.g., 100 µM nitrate for clay, 300 µM for sand/chalk, 500 µM ammonium across sediments).
    - 15N-labelled tracers with ~98 atom % 15N.
    - Anoxic slurries pre-incubated overnight before adding 15N-labelled substrates to remove ambient 14N-nitrate.
  - Incubation and sampling
    - Incubations in the dark at room temperature.
    - Reference samples (no 15N substrate), control samples (biological activity inhibited with zinc chloride before adding 15N), and time-series samples (zinc chloride added at predetermined times after 15N addition).
    - Time points for some datasets include T0, T1, T2, T3, T4, T5 (0, 0.5, 1, 2, 3, 6 h post-15N addition for oxic series).
  - Spatial scope and replicates
    - Rivers in the Hampshire Avon catchment with three substrate-dominant sites each: Clay (Sem and tributaries), Sand (Nadder and Avon branches), Chalk (Ebble, Wylye, Avon branch).
    - 5 replicates per river (Replicate column indicates discrete sediment samples).

- Data structure and key measurements
  - Data table structure
    - Table with 42 columns and 46 rows (including headings); some values marked as BDL (below detection limit).
  - Core measurements and calculations
    - 15N-N2 production measurements to derive P29 and P30 (N2 with m/z 29 and 30) and p15N (15N-labelled N2).
    - Headspace and aqueous concentrations calculated from mass spectrometry data and standard equations (Thamdrup & Dalsgaard methodology).
    - Rates derived from time-series trends (slopes of N2 production versus time for 29N2 and 30N2).
    - Atotal: total anammox activity under anoxic 15N-nitrate conditions (based on Thamdrup & Dalsgaard equations).
    - ra: proportion of N2 production attributable to anammox (percentage of Atotal relative to Dtotal, the total denitrification estimate).
  - Isotope and mixing-model markers
    - FN-NH4+, FN-NOx, FN-N2: fractions of 15N in ammonium, NOx, and N2 pools, used in mixing models to partition N transformations.
    - P29-15A, P30-15A, P29-15A14N, P30-15A14N, P29-15N, P30-15N: specific production rates under different amendment conditions (ammonium with/without nitrate labels).
  - Reference concentrations and assays
    - AmmoniumRef and NOxRef: reference concentrations of ammonium and nitrate+nitrite in oxic slurries (microM), measured via colorimetry.
    - 15NOxT0 to 15NOxT5: concentrations of 15N-labelled NOx in oxic slurry time series (microM).
  - Additional parameters
    - Oxicp15N- and Oxicp15Nrpt- series: 15N-labelled N2 production in oxic slurries and repeated tests (with/without nitrification inhibition via allylthiourea in ATU tests).
    - O2Conc-T0 to O2Conc-T3: dissolved oxygen concentrations in oxic slurries at multiple timepoints.
    - Sample identifiers include site, river, and replicate details (e.g., Clay 1, Sand 2, Chalk 3 with specific latitude/longitude coordinates).

- Spatial and temporal context
  - Site metadata and coordinates
    - Clay 1–3: River Sem and tributaries (specific lat/long provided).
    - Sand 1–3: River Nadder and branches of the River Avon (specific lat/long provided).
    - Chalk 1–3: River Ebble, River Wylye, and east branch of the River Avon (specific lat/long provided).
  - Time-series emphasis
    - Time-resolved data for 15NOx and related N2 production across multiple timepoints, with emphasis on early (0–6 h) post-15N addition windows.
  - Dimensionality
    - Data captures both spatial variation across multiple rivers/sites and temporal dynamics within slurries.

- Data quality, limitations, and references
  - Results are “potentials” rather than actual in-situ rates.
  - Detection limits specified for N2 production and related species (e.g., approx. 0.03 nmol 29N2 g^-1 dry sediment h^-1; 0.4 nmol 30N2 g^-1 d.s. h^-1; 1.6 nmol 15N-N2 g^-1 d.s. h^-1).
  - Data include some values marked as BDL.
  - Analytical methods include automated colorimetry, Griess method with cadmium reduction, and mass spectrometry for 15N-N2 measurements.
  - Foundational references for methods and calculations:
    - Nielsen (1992); Jensen et al. (2011); Smart & Barko (1985); Thamdrup & Dalsgaard (2000, 2002).

- Practical GIS relevance
  - Rich metadata for geospatial mapping of nitrogen cycling processes across multiple stream types and locations.
  - Time-series and isotope-labeled data enable spatial-temporal comparisons of anammox vs denitrification contributions.
  - Clear documentation of measurement protocols, units, and detection limits supports data standardization and integration into GIS-informed decision-support or policy visuals.