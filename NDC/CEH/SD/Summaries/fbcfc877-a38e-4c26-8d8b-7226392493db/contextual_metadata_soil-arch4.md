# Discovery metadata- Soil nutrients, soil pyrogenic carbon, soil bulk density and roots dry weight under different intensities of soil management in the Colombian Andes between 2019-2021

- Objective and scope
  - Generate databases describing soil nutrients, soil pyrogenic carbon, soil bulk density, and roots dry weight across disturbance gradients in Andean Colombia.
  - Assess how soil characteristics vary with forest perturbation and altitude to understand forest resilience and ecosystem functioning.
  - Data collected during 2019–2022 as part of the BioResilience project, funded by UK NERC.

- Study design and locations
  - Permanent monitoring plots: 27 plots, each 0.5 hectares.
  - Altitudinal gradient categories: lowlands (0–1200 m), midlands (1200–2200 m), highlands (2200–3200 m).
  - Disturbance gradient: low, medium, high perturbation with recovery times defined (more than 30 years, 20–30 years, less than 20 years).
  - Locations include Serranía de las Quinchas (lowlands), Pedro Palo and Encino (midlands), Encenillo and Martos (highlands).

- Datasets and key variables (four CSV files)
  - pyrogeniccarbonbr.csv
    - Variables: Plot_code, depth_range_cm, depth_upper_cm, depth_lower_cm, depth_mid_cm, Sample_Id, Project/Collected, %C_(Bulk), Lower_D13C_(pyc), Median_D13C_(pyc), Upper_D13C_(pyc), Cpyc_(%), %Cpyc/Cbulk, %OC.
    - Pyrogenic carbon metrics: TOC (%C_bulk), D13C bounds for pyrogenic carbon, Cpyc (%), Cpyc/Cbulk ratio, and %OC.
  - soilnutrientbr.csv
    - Variables: Plot_code, pH, p_available, tot_p, sand, clay, silt, Ca_ex, Mg_ex, K_ex, Na_ex.
    - Soil chemical and textural properties (pH, extractable nutrients, texture components, exchangeable cations).
  - bulkdensitybr.csv
    - Variables: Plot_code, Depth, Date_sample_taking, Municipio, Departamento, Farm, Land_use, Ecosystem, Bulk_density.
    - Bulk density measurements and associated metadata.
  - dryweigthbr.csv
    - Variables: Plot_code, Ecosystem, Land_use, Municipio, Departamento, Depth, Dry_weight.
    - Roots dry weight data across depths and sites.

- Data collection, transformation, and units
  - Pyrogenic carbon and TOC
    - TOC determined by elemental analysis (Costech ECS-4010).
    - Pyrogenic carbon quantified by hydrogen pyrolysis (HyPy); Cpyc%/Cbulk derived from HyPy results.
    - D13C values for pyrogenic carbon provided with lower/median/upper bounds.
  - Soil nutrients
    - pH measured in water.
    - Available P and total P determined via sequential extraction and acid digestion (Tiessen & Moir references).
    - Particle size by Bouyoucos method (sand, silt, clay).
    - Exchangeable Ca, Mg, K, Na by Ag-TU extraction.
  - Bulk density
    - Derived from pit samples; oven-dried to constant weight.
  - Dry weight
    - Roots dry weight measured per plot/depth.

- Calibration and quality control
  - Instrument calibration and reference value establishment prior to measurements.
  - External review of database structure, completeness, typing, duplicates, and metadata validity.
  - Rigorous quality control to ensure accuracy, completeness, and consistency of data and metadata.

- Data structure and documentation
  - Four CSV files with clearly defined columns and units as listed above.
  - Documentation includes column definitions, measurement units, valid ranges, and data provenance.
  - Coordinates and plot codes enable spatial linkage across datasets.

- Relevance for data strategy and governance (Data Leaders perspective)
  - Data completeness and granularity: fine-grained depth and plot-level data across a systematic altitude and disturbance gradient enable robust cross-site comparisons.
  - Data discoverability and provenance: clearly named files, standardized plot codes, and detailed methodological references support reuse and integration with other datasets (e.g., BioResilience).
  - Metadata and standards: explicit variable definitions, units, and QC processes facilitate data sharing, lineage tracking, and governance.
  - Collaboration and stewardship: multi-institutional collaboration (UNAD, INPA, James Cook University) with external funders; emphasizes consistent data handling across laboratories and sites.
  - Potential uses: analyzing drivers of soil variation under management and disturbance, informing forest resilience models, and supporting policy/management decisions in Andean ecosystems.
  - References provided for methodologies and validation to ensure methodological alignment and reproducibility.