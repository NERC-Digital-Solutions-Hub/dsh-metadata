# Supporting documentation for data resource Scotland_SM_Surficial.csv

- Purpose and scope
  - Dataset title: Dry bulk density, loss on ignition and organic carbon content of surficial soils from Scottish salt marshes, 2018-2020.
  - Geographic scope: Scotland (excluding the Outer Hebrides and the Shetland Islands).
  - Temporal scope: Scottish portion of C-SIDE sampling program and CarbonQuest citizen science sampling, January 2018 – December 2019; no repeat sampling planned.
  - Context: Part of the Carbon Storage in Intertidal Environments (C-SIDE) project; funding by NERC (NE/R010846/1).

- Provenance and team
  - Project team and leadership: William Austin (Staff Responsible); researchers from University of St Andrews, University of Glasgow/Bangor University, Bangor University, and the Scottish Association for Marine Science; includes a C-SIDE Citizen Science Team.
  - Data resource description accompanies the dataset, with detailed methodological and QA information.

- Data content and structure
  - Data resource name: Dry bulk density, loss on ignition and organic carbon content of surficial soils from Scottish salt marshes, 2018-2020.
  - Observations and variables:
    - Dry bulk density (g cm-3)
    - Loss on ignition (LOI, % wt.)
    - Organic carbon content (OC, % wt.) measured by elemental analysis
    - Soil texture (Sandy / Not-Sandy)
    - Location: latitude and longitude in decimal degrees (WGS84); also OSGB36 grid references, X_easting, Y_northing
    - Sampling method: 50 ml syringe or 30 mm gouge corer
    - Depth: 10 cm (topsoil)
    - Site-level identifier: Saltmarsh_Name
  - Sample size and coverage: 471 surficial soil samples from 46 Scottish salt marshes
  - Data formats: CSV files (e.g., Scotland_SM_Surficial.csv)
  - Location metadata and validation: coordinates cross-checked against habitat maps and aerial imagery; multiple coordinate representations provided for interoperability

- Methods and quality assurance
  - Field collection:
    - Sampling depth: top 10 cm
    - Methods: 50 ml syringe or 30 mm gouge corer
    - GPS recording via mobile devices or RTK systems
    - Samples frozen at -20°C prior to analysis
    - Soil texture classification based on Ford et al. (2019) with expert judgement
  - Laboratory analyses:
    - Dry bulk density: derived from dried samples (60°C, 72 h) using initial volume
    - LOI: dried samples milled, combusted at 450°C for 4 hours
    - Organic carbon: using an Elemental Analyser (Elementar Vario EL Cube) after acidification with HCl to remove carbonates
    - Calibrations: Acetanilide; repeated analysis of standard (B2178) to ensure consistency
  - Data quality control:
    - Citizen Science samples visually QC’d by experienced salt marsh scientists before drying
    - GPS coordinates and locations cross-checked with habitat maps and aerial photos
    - Data fields include descriptive headers and clear data types; extensive metadata described for traceability

- Data governance, stewardship and accessibility
  - Data integration and sharing: dataset intended to be uploaded to relevant data portals and catalogues; metadata supports discoverability and reuse
  - Updates and maintenance: current documentation notes no planned repeat sampling; ongoing governance should address any future corrections, licensing, and access terms
  - Documentation and provenance: comprehensive methodological notes, calibration references, and QA procedures included to support reproducibility and data integrity

- Limitations and considerations for users
  - Scope limitations: geographic scope excludes Outer Hebrides and Shetland; no repeat sampling planned, which may affect long-term trend analyses
  - Interoperability: multiple coordinate systems provided (WGS84, OSGB36, grid references) require careful handling in analyses
  - Metadata completeness: while extensive, users should verify licensing and usage terms with data publishers if not included in the CSV metadata

- References (methodology and standards)
  - Craft et al., 1991; Dadey et al., 1992; Ford et al., 2019; Kennedy et al., 2005; Nieuwenhuize et al., 1994; Verardo et al., 1990 (as cited in dataset documentation)