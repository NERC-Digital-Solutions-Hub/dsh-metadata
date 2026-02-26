# Overview

- Dataset scope: Key operational telemetry from a point-of-use drinking water treatment system (PAqua 1000D-2) operated continuously to deliver biologically safe drinking water, located at the University of the West of England (Frenchay Campus). Timeframe: 1 November 2019 to 29 September 2022 (34 months).
- System and technology: Ultrafilter-based treatment with in-situ electrochemically generated hypochlorous acid dosing for disinfection. Telemetry collected to diagnose maintenance issues and monitor function.
- Data source and collection: In-line sensors (s::can, Messtechnik GmbH) and Grundfos Remote Manager interface; data downloaded and interpreted by researchers at UWE Bristol. 5-minute rolling averages for all parameters.
- Data lineage and partners: Part of the NERC project “The development and implementation of sensors and treatment technologies for freshwater systems in India” (NE/R003106/1). Industrial partner Portsmouth Aqua Ltd setup telemetry monitoring; Grundfos provided the remote management platform.
- Data availability and gaps: Sporadic data between April–August 2020 due to a faulty SIM card; new SIM card resolved the issue. Missing values labeled as NA; zero values indicate the POU-DWTS not running.
- Recorded parameters and units: 
  - Date and Time (dd/mm/yyyy hh:mm)
  - Flow_Rate (m3/hr)
  - Discharge_Pressure (bar)
  - TMP (Transmembrane Pressure) (bar)
  - ORP (mV)
  - FAC (Free Available Chlorine) (ppm)
  - Filtration_Flux (m3 m^-2 h^-1)
  - UF_MP (UF Module Permeability) (m3 m^-2 bar^-1 h^-1)
- Calculation notes: Filtration_Flux and UF_MP derived/calculated in Microsoft Excel using specified formulas (as outlined in the dataset documentation).
- Data quality and governance: Weekly quality control checks on key parameters (pH, FAC, HOCl/ORP) and system produced water; periodic “health checks” by Portsmouth Aqua Ltd every 3–6 months; data integrity maintained through the Grundfos Remote Manager interface.
- Related publications and access: Detailed methodology and schematic in Clayton et al. (2024) and broader data context in Fox et al. (2022). Primary dataset reference: pou-dwts_operationaltelemetrydata_uk_nov2019-sep2022.csv; linked datasets available via the NERC Environmental Information Data Centre (EIDC).