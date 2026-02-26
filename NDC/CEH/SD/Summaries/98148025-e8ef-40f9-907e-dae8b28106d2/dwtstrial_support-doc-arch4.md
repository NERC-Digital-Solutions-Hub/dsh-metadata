# Overview

- The dataset documents data from a continuous field trial of a decentralised, low-maintenance drinking water treatment system (DWTS) in the UK, as part of a UK-India Water Quality project.
- It includes:
  - Operational telemetry data (every 5 minutes) from the NINJA Drinking Water Treatment Platform (NINJA-DWTP) using PAqua 1000D-2 with ECAS disinfection.
  - Water quality reports from a UKAS-accredited laboratory (Wessex Water Scientific Centre) for three sampling locations.
- Trial period: 11 weeks from 25 November 2019 to 10 February 2020.
- Sampling locations: raw water (RW), header tank (HT), and potable water (PW).
- Purpose: establish and maintain long-term continuous operation of the modular off-grid DWTS to provide biologically safe drinking water; document system flow, quality parameters, and regulatory compliance.

## System and trial design

- DWTS hardware:
  - PAqua 1000D-2 water purification unit with ECAS biocide (PAqualyte) and ultrafiltration membranes (0.02 µm).
  - Pre-treatment to improve input water quality: two settlement tanks (1000 L) and two Turbidex™ 5 µm prefilter-ionisers.
  - Output water stored in a potable storage tank for sampling; backwashing and disinfection controlled automatically.
- Disinfection and monitoring:
  - ECAS produced by ELA-900 generator; monitoring of output by ORP and free chlorine sensors.
  - Backwashing every 30 minutes; enhanced clean when transmembrane pressure (TMP) thresholds are reached.
  - System activity monitored remotely via Grundfos Remote Management (GRM) telemetry (pumps, TMP, ORP, free chlorine).

## Telemetry data collection

- Data source: Grundfos Remote Management page; internet-based pump management and diagnostics.
- Parameters captured (file 1): 
  - Flow_min, Flow_max, Flow_average (5-minute window statistics).
  - TMP_average (ultrafiltration differential pressure).
  - ORP_min, ORP_max, ORP_average (treated output water).
  - FCl_min, FCl_max, FCl_average (free chlorine concentration in treated water).
  - Date_Time (Recorded by GRM).

## Water sampling and laboratory analysis

- Sampling regime:
  - Three locations per sampling event: RW (raw water), HT (header tank), PW (potable water).
  - Sampling frequency: weekly during the 11-week trial (two university closure weeks excluded).
  - Analysis performed by Wessex Water Scientific Centre (UKAS-accredited, ISO 17025).
- Analyzed parameters:
  - Microbiological: Escherichia coli, coliforms, Clostridium perfringens, Enterococci, plate counts (2- and 3-day), and related indicators.
  - Physicochemical: pH, colour (spectrophotometer and estimated), turbidity, electrical conductivity (EC), total hardness, non-carbonate hardness, alkalinity, TOC.
  - Inorganics and nutrients: sulfate, orthophosphate, chloride, silica, ammonium, nitrite, nitrate, alkalinity, various metals (Ca, Mg, Na, K, Al, Mn, Fe, Cu, Zn) and more.
  - Additional/extended analyses: various metals, fluorides, pesticides, PAHs, THMs, and other organics; subset parameters tested less frequently.
- Methods and limits:
  - DWI regulatory limits applied (e.g., E. coli and coliforms 0/100 mL; pH 6.5–9.5; turbidity 4 NTU; EC 2500 µS/cm; etc.).
  - Detailed methods per parameter documented (e.g., 3303, 3406, 2550, 2451, etc.).
  - Some parameters are optional or conditional within “Full/Standard/Basic” sampling suites.

## Data structure and file overview

- Four CSV files:
  - 1_DWTS_operational-parameters.csv (11 columns)
    - Date_Time; Flow_min; Flow_max; Flow_average; TMP_average; ORP_min/ORP_max/ORP_average; FCl_min/FCl_max/FCl_average.
    - Recorded by the Grundfos Remote Management system; five-minute window summaries.
  - 2_DWTS_RawWater_data-summary.csv (85 columns)
    - Date; Time; Coliforms_37; E-coli_37; Coliforms_44; E-coli_44; Count_2day_37; Count_3day_22; C-perfringens; Enterococci; pH; Colour_spec; Colour_est; Turbidity; EC; T_hardness; Non-CaCO3_hardness; Alkalinity; TOC; SO4; PO4_3-; Cl; Si; NH4; NO2; NO3; F; CN; FOG; Ca; Mg; Na; K; Al; Mn; Fe; Cu; Zn; and many other metals, pesticides, PAHs, THMs, etc. (detailed in Table 6).
  - 3_DWTS_HeaderTank_data-summary.csv (77 columns)
    - Similar parameter set as raw water, but for header tank (HT) samples.
  - 4_DWTS_Potable_data-summary.csv (85 columns)
    - Similar parameter set as raw water, but for potable water (PW) samples.
- Data quality and gaps:
  - Some parameters not collected at every sampling event; missing values labeled NA.
  - Variation in sampling regimes between “Full,” “Standard,” and “Basic” suites.
  - The data is a case-study dataset with comprehensive yet heterogeneous coverage across locations and parameters.

## Key considerations for data governance and use

- Regulatory and safety context:
  - Data aligns with Drinking Water Inspectorate limits for microbiological and certain chemical parameters; supports assessment of disinfection efficacy and compliance.
- Data governance and metadata:
  - Four-file structure with clear mapping between operational telemetry and water quality results; thorough parameter documentation and method references enable cross-system benchmarking.
  - Metadata includes sampling locations, sampling schedule, and instrumentation sources (GRM, s::can analysers).
- Data quality and interoperability for data leaders:
  - Useful for building end-to-end data products that fuse real-time system telemetry with laboratory-verified water quality results.
  - Highlights importance of standardizing suites (Full/Standard/Basic) to improve comparability and reduce missingness across datasets.
  - Demonstrates challenges in data completeness due to varying sampling regimes and selective parameter reporting, with explicit NA indicators.
- Potential applications for data strategy:
  - Design of cross-location data products and dashboards integrating operational performance (flow, TMP, ORP) with water quality outcomes.
  - Evaluation of data governance practices, metadata richness, and discoverability in multi-partner data collaborations.
  - Identification of data gaps and planning for standardized data collection across networks and partners.