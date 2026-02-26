# Overview

- Dataset from a continuous trial of a decentralised low maintenance drinking water treatment system (DWTS) in the UK, focused on monitoring and evaluating environmental health and policy-relevant performance over time.
- Field trial conducted 25 November 2019 to 10 February 2020 (11 weeks) at the University of the West of England, Bristol, using a PAqua 1000D-2 ultrafiltration-based DWTS (NINJA-DWTP) integrated with ECAS biocidal dosing.
- Aims to demonstrate long-term, biologically safe drinking water production from highly contaminated input water and to support sensing, treatment, and monitoring technologies.

## System description and context

- NINJA drinking water treatment platform (NINJA-DWTP) installs a PAqua 1000D-2 unit with ECAS disinfection (PAqualyte) and ultrafiltration, backed by ancillary equipment to reduce input contaminant load.
- Core flow: raw water → pre-filter → UF membranes → treated water tank → sampling → potable storage; ECAS dosing and backwash integrated, with remote monitoring via Grundfos Remote Management.
- Ancillary input pretreatment to improve efficiency: two 1000 L settlement tanks and two Turbidex 5 µm prefilter-ionisers.
- System automatically handles backwashing (UF membranes every 30 minutes) and enhanced cleaning when transmembrane pressure (TMP) thresholds are reached.

## Data collected and telemetry

- Telemetry data captured via Grundfos Remote Management and inline sensors (s::can) for remote diagnosis and monitoring.
- Operational parameters (file 1) include:
  - Flow_min, Flow_max, Flow_average (5-minute window)
  - TMP_average (ultrafiltration membrane differential pressure)
  - ORP_min, ORP_max, ORP_average (treated output water)
  - FCl_min, FCl_max, FCl_average (free chlorine in treated water)
- Output describes data collection frequency and instrumentation (Grundfos REM for pump data; s::can analysers for ORP and free chlorine).

## Water sampling and quality analysis

- Sampling at three sites: raw water, header tank (post-pre-filtration), and potable water (post-DWTP).
- Weekly sampling over 11 weeks (with a 2-week campus closure period); samples analyzed by Wessex Water Scientific Centre (UKAS-accredited) to ISO 17025 standards.
- Comprehensive water quality testing including:
  - Microbiological: E. coli, coliforms, Clostridium perfringens, Enterococci, plate counts
  - Physicochemical: pH, conductivity, turbidity, colour (spec and estimated), alkalinity, TOC, sulfates, orthophosphate, chlorides, silicates, hardness (total and non-carbonate), various metals, ammonia, nitrite, nitrate
  - Additional analyses: extended metals, hydrocarbons, PAHs, pesticides, THMs, volatile organics, pesticides, and other contaminants as detailed in Tables 3-4
- Regulatory compliance references: Drinking Water Inspectorate (DWI) limits (2010) applied for interpretation of results.

## Data structure and files

- Four CSV files comprising the dataset:
  - 1_DWTS_operational-parameters.csv (11 columns; 5-minute operational metrics)
  - 2_DWTS_RawWater_data-summary.csv (85 columns; raw water quality data)
  - 3_DWTS_HeaderTank_data-summary.csv (77 columns; header tank water quality data)
  - 4_DWTS_Potable_data-summary.csv (85 columns; potable water quality data)
- File 1 includes metadata on data capture (Date_Time, Flow_min/Flow_max/Flow_average, TMP_average, ORP_min/max/average, FCl_min/max/average).
- Files 2-4 align with sampling location and include a wide range of parameters, each with DWI limits and standard methods (e.g., pH, turbidity, conductivity, TOC, sulfates, orthophosphate, multiple metals, an extensive list of organic contaminants and pesticides).
- Data completeness notes: essential operational data in file 1; some parameters missing for certain samples due to sampling regime; missing values marked as NA.

## Sampling regimes and timeline

- Raw water sourced from an artificial water body on-campus; NINJA-DWTP on southeast bank.
- Trials spanned 11 weeks: weekly sampling (except during university closure) from 25/11/2019 to 10/02/2020.
- Analyzed by Wessex Water Scientific Centre; samples delivered within four hours; microbiological analyses within 24 hours.

## Compliance, standards, and data interpretation

- Parameters tested against DWI 2010 limits where applicable (e.g., E. coli, coliforms, pH, turbidity, conductivity, various metals, THMs, pesticides, PAHs).
- Tables in the dataset documentation enumerate which parameters are included in each sampling suite (Full, Standard, Basic) and associated methods.
- Treated water quality monitored continuously via UF membrane effluent and inline sensors to ensure output remains within regulatory and safety thresholds.

## Data usage and challenges for analysts

- Designed to provide a consistent, scrutinable view of environmental health and DWTS performance over time.
- Opportunities to increase data value by integrating these datasets with external datasets (e.g., site conditions, weather, or broader water quality datasets) and by enabling access to underlying data to support independent verification and policy evaluation.
- Completeness and sampling variation require careful handling of missing values and alignment of parameters across files.

## References and context

- Clayton, G.E., Thorn, R.M.S., Reynolds, D.M., 2019. Development of a novel off-grid drinking water production system integrating electrochemically activated solutions and ultrafiltration membranes.
- Drinking Water Inspectorate, 2010. The Water Supply (Water Quality) Regulations 2010.