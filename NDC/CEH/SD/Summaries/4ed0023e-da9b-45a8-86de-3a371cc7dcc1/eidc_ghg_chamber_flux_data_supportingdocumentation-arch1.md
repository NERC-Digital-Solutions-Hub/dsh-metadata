# Fluxes of carbon dioxide, nitrous oxide and methane from winter wheat treated with organic and inorganic fertilisers

- What the dataset contains
  - 2-hourly biogenic flux measurements of CO2, N2O, and CH4 from a winter wheat crop grown on mineral soil in the UK.
  - Three fertiliser treatments with three replicates each: i) inorganic fertiliser (IF); ii) pig slurry and inorganic fertiliser (PS); iii) pig slurry treated with plasma-induction and inorganic fertiliser (TPS).
  - Measurements span 83 days during the winter wheat growing season (20/03/2022–13/06/2022) using automated GHG flux chambers.

- Study site and experimental design
  - Location: University of Leeds Research Farm (temperate oceanic climate; soil: loamy calcareous brown earth).
  - Field history: continuous arable rotation since 1970.
  - Soil characteristics (0–30 cm): pH 6.9, bulk density 1.3 g cm-3, total soil carbon 39.5 g kg-1, total nitrogen 2.3 g kg-1.
  - Climate context: mean annual temperature ~9.5°C, annual precipitation ~885 mm.
  - Field management: rainfed; winter wheat planted 21/10/2021 at 440 seeds m-2; harvested 27/07/2022.
  - Treatments: IF, PS followed by IF, TPS followed by IF; all received 220–253 kg available N ha-1.
  - Experimental design: three replicates per treatment.

- Data collection and instrumentation
  - Instrumentation: Eosense eosAC-LT chambers and Picarro G2508 analyser.
  - Sampling frequency: every 2 hours from 20/03/2022 to 13/06/2022.
  - Output variables: CO2 (μmol CO2 m-2 s-1), N2O (nmol N2O m-2 s-1), CH4 (nmol CH4 m-2 s-1); all flux values are gap-filled where indicated.
  - File reference: data stored in GHG_chamber_flux_data.csv; includes Chamber_Number and Treatment identifiers.

- Data processing and quality control
  - Flux calculation: offline using eos-AnalyzeMX/AC V3.5.0; CO2 concentrations used to derive fluxes for all gases via linear fitting.
  - Outlier handling and uncertainty: employed a modified Elbers et al. (2011) approach to remove outliers; CO2 flux uncertainty quantified using threshold u*, plus measurement and flux-calculation uncertainties.
  - Replication and consistency: three replicates per treatment; field setup and timing described to support cross-treatment comparisons.

- Gap-filling and data completeness
  - N2O and CH4: gap-filled by linear interpolation.
  - CO2: gap-filled by linear regression with separate gap-filling for daytime and nighttime flux data.
  - Gap-filled indicator: Gap_Fill column (1 = observed, 2 = gap-filled).

- Data structure and metadata
  - Key variables in the dataset:
    - Date_Time: start of 2-hour measurement (dd/mm/yyyy HH:MM, GMT).
    - Chamber_Number: chamber identifier.
    - CO2, N2O, CH4: gap-filled flux values (units as above).
    - Gap_Fill: data origin flag (1 observed, 2 gap-filled).
    - Treatment: fertiliser treatment code (IF, PS, TPS).
  - The dataset is designed to support analyses of how GHG fluxes respond to different fertiliser strategies, with explicit metadata on sampling, processing, and gap-filling.

- Acknowledgements and references
  - Funding: Leeds-York-Hull NERC Doctoral Training Partnership (NE/S007458/1).
  - Acknowledged contributions from the University of Leeds Research Farm and named individuals for materials, assistance, and guidance.
  - Methodological references underpinning processing, gap-filling, and uncertainty assessment are cited in the accompanying references.

- Potential uses for analysts
  - Compare CH4, N2O, and CO2 flux responses across IF, PS, and TPS treatments.
  - Quantify temporal patterns (diurnal and seasonal) of GHG fluxes at 2-hour resolution.
  - Assess the impact of pig slurry and its treatment on soil-atmosphere GHG exchange under winter wheat.
  - Integrate with soil and climate data to model drivers of GHG fluxes and create predictive relationships.
  - Evaluate uncertainty and robustness of flux totals given gap-filled data and u*–based QC.