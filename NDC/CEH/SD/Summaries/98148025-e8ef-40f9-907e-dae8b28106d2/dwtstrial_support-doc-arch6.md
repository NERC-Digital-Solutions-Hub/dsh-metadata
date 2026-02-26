# Overview

- The document describes a dataset from a continuous trial of a decentralised low maintenance drinking water treatment system (DWTS) in the UK, focusing on a PAqua 1000D-2 unit integrated into the NINJA-DWTP on the University of the West of England campus. The trial ran from November 2019 to February 2020 and supports a UK-India Water Quality project aimed at sensing and treatment technologies for monitoring and improving water quality.
- Data captured include:
  - Operational parameters recorded every 5 minutes (file 1).
  - Water quality reports from a UKAS-accredited laboratory for three sampling locations (files 2-4).
- The dataset is intended to enable analysis of long-term, continuous operation to provide biologically safe drinking water from a heavily contaminated source, with modular, off-grid decentralised treatment leveraging ultrafiltration and ECAS biocidal dosing.

## Data context and aims for data use

- Purpose: to enable data-driven exploration of data quality, system performance, and water quality outcomes; to support development of data products (dashboards, self-service analyses) and inform better data creation and sharing.
- Relevance to data support professionals:
  - Demonstrates end-to-end data collection: field measurements, telemetry, laboratory analyses, and data structuring.
  - Highlights data integration challenges (multiple data streams, varying completeness, and different sampling regimes).

## System description (NINJA-DWTP)

- PAqua 1000D-2 water purification unit integrated with ECAS disinfection (PAqualyte) and ultrafiltration membranes (0.02 µm).
- Input water is heavily contaminated; system includes:
  - Two settlement tanks (1000 L each) and two Turbidex™ prefilters (5 µm) to reduce sediment and particulates before UF.
  - Potable storage tank (1000 L) feeding a water softener and brine tank to operate ECAS.
  - UF permeate monitored for ORP and free chlorine; excess above thresholds rejected to wastewater.
  - Treatment output stored in a potable tank and then delivered as potable water after rejuvenation.
- Automation and remote monitoring:
  - Grundfos Remote Management (GRM) system for remote monitoring, diagnostics, and control of pump activity, UF transmembrane pressure (TMP), and inline free chlorine/ORP data.
  - Regular UF backwash every 30 minutes; enhanced clean triggered by TMP thresholds (0.6 bar) during operation.
- Telemetry and sampling locations:
  - Three sampling locations within the system for data capture (RW, HT, PW) with samples sent to Wessex Water Scientific Centre for analysis.

## Telemetry data (file 1)

- Collected via Grundfos Remote Management and in-line sensors (s::can, Messtechnik GmbH).
- Parameters and data characteristics (Table 2):
  - Flow rate: m3/hr; 5-minute window; values include average, min, max.
  - Differential pressure across UF membrane: bar; 5-minute window; average value.
  - ORP: mV; 5-minute window; average, min, max (measured post UF).
  - Free chlorine: ppm; 5-minute window; average, min, max (post UF).
- Data design supports remote diagnosis and performance assessment of pumps, TMP, and disinfection indicators.

## Collection of water samples (sampling plan)

- Three sampling locations (Figure 2):
  - RW: Raw water source.
  - HT: Header tank water (post pre-filtration, pre-UF).
  - PW: Treated potable water (pipeline to potable storage).
- Sampling method:
  - Use clean HDPE bottles; rinse prior to sampling; flush taps for 10 seconds before sample collection.
  - Samples delivered to Wessex Water Scientific Centre within four hours; microbiological analyses within 24 hours per UKAS/ISO procedures.
- Sampling timeline:
  - 11-week field trial, weekly sampling with a two-week campus closure.
  - Full parameter suites aligned with the sampling schedule (Appendix/Table 1) to capture microbiological and physicochemical variables.

## Water quality analysis (lab methods and parameters)

- Primary regulatory focus: Drinking Water Inspectorate (DWI) 2010 limits and methods.
- Microbiological parameters (all three locations; weekly):
  - Escherichia coli, Coliforms, Clostridium perfringens, Enterococci, plate counts (2-day and 3-day counts at specified temperatures).
- Physicochemical and other parameters:
  - pH, conductivity, turbidity, colour (spec and estimated), alkalinity, TOC, orthophosphate, sulfate, chloride, silica, ammonium, nitrite, nitrate, hardness (total and non-carbonate), various metals (Al, Mn, Fe, Cu, Zn, etc.), and other compounds.
- Expanded chemical testing (less frequent) included fluorides, cyanides, fats/oils/grease, pesticides, PAHs, THMs, chlorinated solvents, bromates, chlorites, and related compounds (Table 4).
- Data structure emphasizes compliance parameters and suite selection (Full, Standard, Basic) per sampling regime.

## Data structure and files

- Four CSV files:
  - File 1: 1_DWTS_operational-parameters.csv (11 columns)
  - File 2: 2_DWTS_RawWater_data-summary.csv (85 columns)
  - File 3: 3_DWTS_HeaderTank_data-summary.csv (77 columns)
  - File 4: 4_DWTS_Potable_data-summary.csv (85 columns)
- Key column themes (examples):
  - File 1: Date_Time, Flow_min/Flow_max/Flow_average, TMP_average, ORP_min/ORP_max/ORP_average, FCl_min/FCl_max/FCl_average.
  - File 2: Date, Time, Coliforms_37, E-coli_37, Coliforms_44, E-coli_44, Count_2day_37, Count_3day_22, C-perfringens, Enterococci, pH, Colour_spec, Turbidity, EC, T_hardness, Non-CaCO3_hardness, Alkalinity, TOC, SO4, PO4_3-, Cl, Si, NH4, NO2, NO3, F, CN, FOG, Ca, Mg, Na, K, Al, Mn, Fe, Cu, Zn, As, B, Cr, Sb, Ba, Cd, Pb, Ni, Hg, Se, Benzene, and many others with corresponding units and DWI limits.
  - File 3 and 4: Similar parameter families across header tank and potable outputs; each includes date/time plus regulatory, chemical, and microbiological measurements with defined limits and methods.
- Data completeness:
  - Essential operational data included in file 1; some data from Grundfos RM is condensed and not fully representative of trial-wide performance.
  - Not all water quality parameters are available for all samples; missing values are coded as NA.
  - Variability in sampling regime and parameter inclusion across Full/Standard/Basic suites is documented (Appendix/Table details).

## Completeness, data quality, and caveats

- Completeness:
  - Essential operational data is captured, but some telemetry and ancillary data are not uniformly available across the entire trial.
  - Water quality datasets (files 2-4) contain many parameters, but not every parameter is measured at every sampling event; some infrequent analyses are noted as supplementary.
- Data quality:
  - Analyses performed by UKAS-accredited Wessex Water Scientific Centre; methods and limits reflect DWI standards.
  - Data structured with explicit DWI limits and standard methods for traceability and QA.
- Limitations for users:
  - Patchy data across different datasets and sampling regimes require careful alignment and cleaning.
  - Variation in the sampling schedule (full/standard/basic suites) may affect cross-location and cross-time comparisons.
  - Some operational datasets from remote management systems may be condensed or not directly comparable to full trial-wide datasets.

## Potential data products and use cases for Data Support

- Data products:
  - Dashboards showing real-time-like monitoring of flow, TMP, ORP, and free chlorine, correlated with water quality outcomes at RW/HT/PW.
  - Self-service analyses comparing pre-treatment (RW) versus post-treatment (PW) microbiological and physicochemical indicators.
  - Time-series analyses of backwash events, TMP thresholds, and ECAS dosing in relation to water quality metrics.
  - Compliance-oriented reports tracking DWI-limit adherence across sample points and time.
- Use cases for data exploration:
  - Assessing the impact of input water quality on UF performance and treatment efficiency.
  - Evaluating stability of disinfection indicators (ORP, free chlorine) and their relationship to microbiological results.
  - Investigating the effectiveness of settlement tanks and Turbidex filtration in reducing loading to the DWTP.
  - Designing data pipelines to merge file 1 (operational) with files 2-4 (water quality) for integrated analytics.

## References

- Clayton, G.E., Thorn, R.M.S., Reynolds, D.M., 2019. Development of a novel off-grid drinking water production system integrating electrochemically activated solutions and ultrafiltration membranes. J. Water Process Eng.
- Drinking Water Inspectorate (DWI), 2010. The Water Supply (Water Quality) Regulations 2010.