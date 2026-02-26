# Supporting Information : Hydrogeochemical data for groundwater remediation systems in Bihar, India, 2018-2022

- Origin and purpose
  - Presents hydrogeochemical data from groundwater remediation systems in Bihar (Middle Gangetic Plain), collected in 2019 (31 remediation systems) with one additional system in Ballia District, Uttar Pradesh.
  - Data collected under a larger stratified random groundwater sampling effort (~300 tubewells); remediation systems were identified opportunistically at sampling locations.
  - Remediation is defined broadly to include point-of-use treatment and potential shifts to less-contaminated sources; samples include both untreated inlet water and treated outlet water where available.

- Study area and sampling strategy
  - Geographic coverage: Bihar across multiple districts (Patna, Buxar, Gaya, Katihar, Aurangabad, East Champaran, Nawada, Munger, Vaishali) plus one nearby site in Ballia, UP.
  - Sampling design: spot-checks conducted under typical operating conditions with owners unaware of impending sampling; reflects real-world remediation performance and system heterogeneity.
  - System representation: urban bias in Patna noted due to higher sampling density and prevalence of household water treatment systems.
  - Data scope: focused on remediation systems; paired inlet-outlet samples used for assessing remediation performance; more units exist beyond the paired dataset.

- Remediation system sampling & characterization
  - For each system: collected subsamples from (i) the untreated groundwater feed (inlet) and (ii) the corresponding finished product/outlet water.
  - Additional samples from local packaged water were collected when available, though inlet groundwater could not always be sampled for these.
  - Inlet samples sourced from handpumps or taps connected to the groundwater source; outlet samples from system outlets or nearest accessible point.
  - Sample handling: plastic beakers rinsed between samples; filtrations performed on collection (0.45 μm) for major/trace analyses; inlet/outlet paired data emphasized.

- Chemical analysis (laboratory)
  - Location: Manchester Analytical Geochemistry Unit (MAGU).
  - Techniques:
    - ICP-MS (Agilent 7500cx) for As, U, Zn.
    - ICP-AES (Perkin-Elmer Optima 5300 DV) for Fe, P, Ca, Mg, Mn, Na, K, Si.
  - Data treatment: samples filtered and acidified (2% HNO3) after transport; QA/QC details referenced to Richards et al. (2020).

- Nature and units of recorded values
  - Data file headers specify the measured parameters; key entries include System_ID, As_Retention_%, Tech_Type_Code, Setting_User_Type_Code, and inlet concentrations for Fe, P, As, Ca, Mg, Na, Si (and Ni noted in dataset).
  - As_Retention_%: calculated as (1 - (C_outlet,As / C_inlet,As)) × 100.
  - Tech_Type_Code: 1 = reverse osmosis or other membrane system; 2 = non-membrane remediation.
  - Setting_User_Type_Code: 3 = household; 4 = non-household.
  - Inlet concentrations provided in ppm or ppb for respective elements; below-detection values set to 0.1 ppb for As and 0.001 for Fe and P.
  - Data structure: 11 columns in the data spreadsheet, including selected inlet composition parameters (Fe, P, As, Ca, Mg, Na, Si, Ni).

- Data structure and content
  - Spreadsheet covers data for 31 remediation systems in Bihar, with columns detailing As retention, technology category, setting category, and inlet water composition.
  - Selected parameters include Fe, P, As, Ca, Mg, Na, and Ni; all relevant units and coding are described in the dataset documentation.

- Quality control
  - Quality assurance/quality control procedures are described in Richards et al. (2022); further methodological details available in Richards et al. (2020).

- Data access, contact, and references
  - Primary data contacts: Dr Laura L. Richards (laura.richards@manchester.ac.uk) and Prof. David Polya (david.polya@manchester.ac.uk).
  - Data identifier: 77700f8e-5da6-45ab-9c12-df1a7d20bc32.
  - Associated publications for full methodological context:
    - Richards et al. (2020) Distribution and Geochemical Controls of Arsenic and Uranium in Groundwater-Derived Drinking Water in Bihar, India. International Journal of Environmental Research and Public Health.
    - Richards et al. (2022) Household and community systems for groundwater remediation in Bihar, India: Arsenic and inorganic contaminant removal, controls and implications for remediation selection. Science of the Total Environment.

- Implications for data management and reuse (Data Leaders perspective)
  - Data asset: a structured set of inlet-outlet geochemical data for 31 remediation systems, enabling evaluation of arsenic retention and remediation technology performance.
  - Metadata and provenance: well-documented sampling strategy, instrumentation, and analysis methods linked to broader campaigns; notes on spot-check sampling and urban bias inform interpretation and generalizability.
  - Discoverability and interoperability: clear data fields (System_ID, retention %, tech/type codes, inlet water chemistry) facilitate integration with other Bihar groundwater datasets and remediation studies.
  - Limitations and considerations: paired inlet-outlet data are limited to 31 systems; sampling is opportunistic rather than fully randomized, which may affect extrapolation to wider populations.
  - Opportunities: use for meta-analysis of remediation options, assessment of technology effectiveness across settings, and informing data-sharing practices in groundwater remediation programs.