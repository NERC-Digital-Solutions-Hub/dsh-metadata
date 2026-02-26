# Discharge dataset (4 files), details as follows: Surface water chemistry dataset (4 files), details as follows:

## Overview
- Describes two related environmental monitoring datasets: 
  - Discharge data (4 CSV files) from four sites/rivers.
  - Surface water chemistry data (4 CSV files) from the same sites.
- Timeframes:
  - Discharge: 2013–2015 (site-dependent).
  - Surface water chemistry: mid-2013 to mid-2014.
- Sites (by file prefix and river): CE (Ebble), GA (Avon), GN (Nadder), AS (Sem).

## Datasets and content
- Discharge dataset
  - Files: CE_Discharge_data.csv, GA_Discharge_data.csv, GN_Discharge_data.csv, AS_Discharge_data.csv.
  - Description: Average daily discharge (m3/s) derived from stage data (15-minute intervals).
  - Location references (OS Grid): CE SU05598 25343 (River Ebble); GA SU09723 57824 (River Avon); GN ST92380 27376 (River Nadder); AS ST92346 27381 (River Sem).
  - Time ranges provided per file (From/To dates).
- Surface water chemistry dataset
  - Files: CE_surfacewater_chemistry.csv, GA_surfacewater_chemistry.csv, GN_surfacewater_chemistry.csv, AS_surfacewater_chemistry.csv.
  - Description: Surface water chemistry analysed from grab samples taken at 09:00 GMT on dates provided.
  - Location references (OS Grid) as above for each site.
  - Time ranges provided per file (From/To dates).

## Measurement and instrumentation
- Field instrumentation
  - HOBO U20-001-01 (Onset, USA)
  - Levelogger Edge (Solinst, Canada)
  - Manta 2 (Eureka Water Probes, USA)
- Hydrological data collection
  - Stage measured with pressure transducers (HOBO U20-001-01 at AS, GA, GN; Levelogger Edge at CE) in a perforated stilling well, 15-minute intervals.
  - Fortnightly manual discharge measurements (velocity-area method) to construct site-specific stage-discharge relationships (available on request from Prof A Binley).

## Quality control and data governance
- Hydrological quality control
  - Regular stage-discharge relationship construction via manual measurements.
  - Stage-discharge relationships available on request.
- Analytical chemistry quality control
  - SSC: filtration with GF/C, gravimetric analysis.
  - Anions: chloride, nitrate, sulfate by Thermo Dionex Ion Chromatography; specified limits of detection and precision (LODs and RSDs).
  - Cations and others: ICP-OES analysis with specified detection limits and precision; certified reference materials used for accuracy checks.
  - Total phosphorus: autoclave digestion + Skalar Auto Analyzer; LOD and accuracy details provided.
  - Dissolved organic carbon (DOC): non-purgeable organic carbon method; LOD and precision details provided.
  - References to certified materials and accuracy figures for QA.
- Data provenance and contact
  - Queries about datasets: Kate Heppell (c.m.heppell@qmul.ac.uk).
  - Stage-discharge relationship data requests: Prof A Binley (a.binley@lancaster.ac.uk).

## Data structure and fields
- Discharge data
  - Spreadsheets: 4 MS Excel files, each with two columns: Date (dd/mm/yyyy) and Average daily discharge (m3/s).
- Surface water chemistry data
  - Spreadsheets: 4 MS Excel files, each with 14 columns: Site, date (dd/mm/yyyy), SSC (mg/L), Cl (mg/L), NO3 (mg/L), SO4 (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), DOC (mg C/L).

## Accessibility and metadata considerations
- Metadata and data governance
  - Some metadata (e.g., stage-discharge relationships) may require direct contact to originators.
  - Data sharing and openness are facilitated through designated contacts; potential barriers noted in monitoring frameworks (data access, metadata completeness, and data governance requirements).

## Implications for monitoring framework work
- Demonstrates integration of hydrological (discharge) and chemical (water quality) measurements across multiple sites.
- Emphasizes standardized temporal sampling (daily discharge from 15-minute stage data; fixed 09:00 GMT sampling for chemistry).
- Highlights robust QA/QC practices, including use of reference materials and documented LODs/RSDs.
- Shows explicit data structure for easy integration into dashboards or policy evaluation tools.
- Underlines practical data governance needs: metadata completeness, data sharing, and clear points of contact for data queries.