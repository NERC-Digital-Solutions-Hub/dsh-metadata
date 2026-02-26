# NINJA Drinking Water Treatment Platform

## Overview
- Dataset from a continuous trial of a decentralised, low-maintenance drinking water treatment system (DWTS) in the UK, featuring the PAqua 1000D-2 unit within the NINJA-DWTP.
- Aimed at enabling biologically safe drinking water from a heavily contaminated source, using ultrafiltration and ECAS biocidal dosing for disinfection.
- Trial run from November 2019 to February 2020; water quality analyzed at three locations within the system; data gathered to assess long-term operation and performance.
- Sampling includes regulatory water quality parameters (as per the Drinking Water Inspectorate, DWI) plus extended metals and hydrocarbons analyses.

## System description
- Core platform: PAqua 1000D-2 water purification unit with ECAS disinfection (PAqualyte) and ultrafiltration membranes.
- Pre-treatment: settlement tanks and Turbidex prefilter-ionisers to reduce input sediment and particulates, improving UF efficiency and membrane longevity.
- Output handling: treated water stored in a 100 L tank, then supplied to a water softener/brine system and backwash loops; backwash water routed to wastewater drains.
- Monitoring: remote monitoring via Grundfos Remote Management (GRM) for pump activity, transmembrane pressure, and inline free chlorine/ORP data.
- Sampling locations: Raw water (RW), Header Tank (HT), and Potable water (PW) within the pipeline to potable storage.

## Telemetry data and collection
- Telemetry collected through Grundfos Remote Management and sensors (s::can) with 5-minute data windows.
- Key operational parameters (file 1) include:
  - Flow rate (min, max, average) in m3/hr
  - Ultrafiltration membrane differential pressure (TMP) in bar
  - ORP (min, max, average) in mV
  - Free chlorine concentration (min, max, average) in ppm
- Data are summarized and stored in four CSV files; linkage to hardware via programmatic backwashing schedules and enhanced cleaning when TMP thresholds are reached.

## Water quality testing and sampling
- Sampling conducted weekly over 11 weeks (Nov 25, 2019 – Feb 10, 2020), with two weeks during campus closure.
- Samples analyzed by Wessex Water Scientific Centre (UKAS-accredited) following ISO/UKAS procedures.
- Parameters tested include:
  - Microbiological: E. coli, coliforms, Clostridium perfringens, Enterococci, plate counts
  - Physicochemical: pH, colour (spec and estimate), turbidity, conductivity, alkalinity, TOC
  - Inorganics: sulfates, orthophosphates, chlorides, silica, ammonium, nitrite, nitrate, various metals (Ca, Mg, Na, K, Al, Mn, Fe, Cu, Zn, As, etc.)
  - Organic contaminants: FOG, total pesticides, THMs, PAHs, benzene and related chlorinated hydrocarbons, chlorate, chlorite, bromate, and other volatiles
- Sampling points:
  - RW: raw water source
  - HT: header tank output after pre-filtration
  - PW: potable water after delivery to storage
- Compliance references: DWI limits and methods (Tables 3–4 in the document); standard methods 3302, 3303, 3406, 3400, 3416, 2550, 2451, etc.

## Data structure and content
- Four CSV data files comprising four data streams:
  - 1_DWTS_operational-parameters.csv: 11 columns (Date_Time, Flow_min, Flow_max, Flow_average, TMP_average, ORP_min/max/average, FCl_min/max/average)
  - 2_DWTS_RawWater_data-summary.csv: 85 columns including Date, Time, Coliforms_37, E-coli_37, Coliforms_44, E-coli_44, Count_2day_37, Count_3day_22, C-perfringens, Enterococci, pH, Colour_spec, Colour_est, Turbidity, EC, T_hardness, Non-CaCO3_hardness, Alkalinity, TOC, SO4, PO4_3-, Cl, Si, NH4, NO2, NO3, F, CN, FOG, and extensive metals and organics data
  - 3_DWTS_HeaderTank_data-summary.csv: 77 columns (similar microbiological, chemical, and physical parameters as above, collected at header tank)
  - 4_DWTS_Potable_data-summary.csv: 85 columns (similar parameter set for potable water samples)
- Each parameter includes units, DWI limit, and standard method; many entries indicate whether a parameter is included in Full/Standard/Basic sampling suites.
- Data include explicit missing values marked as NA.

## Data quality, limitations, and notes
- Essential operational data (file 1) is present, but some data are missing for certain parameters (NA) due to sampling regime variations.
- Not all water quality parameters were collected at every sampling event; some were designated as indicators.
- Some data captured by the Grundfos Remote Management system were condensed and not useful for assessing overall trial performance.

## How Analysts can use this dataset
- Correlate input water quality and pre-treatment (RW to HT) with UF membrane performance (TMP, flow) and disinfection metrics (ORP, free chlorine) to assess treatment efficacy.
- Evaluate compliance performance against DWI regulatory limits across microbiological and chemical parameters for raw, header tank, and potable water streams.
- Develop predictive models of backwash frequency, membrane fouling, and disinfection dosing requirements under varying input water conditions.
- Compare microbiological trends (e.g., E. coli, coliforms, Enterococci) across locations to assess system protection against pathogens.
- Data structure supports reproducible QA and making datasets discoverable (metadata-rich uploads).

## References
- Clayton, G.E., Thorn, R.M.S., Reynolds, D.M., 2019. Development of a novel off-grid drinking water production system integrating electrochemically activated solutions and ultrafiltration membranes. J. Water Process Eng.
- Drinking Water Inspectorate, 2010. The Water Supply (Water Quality) Regulations 2010.