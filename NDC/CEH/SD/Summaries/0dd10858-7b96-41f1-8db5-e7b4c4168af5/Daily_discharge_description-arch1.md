# Discharge dataset (4 files), details as follows:

## Overview
- Four discharge datasets (CE, GA, GN, AS) with average daily discharge (m3/s) derived from 15-minute stage data collected using various pressure transducers.
- Four surface water chemistry datasets accompany the discharge data, using grab samples collected at 09:00 GMT.
- Sites correspond to rivers Ebble, Avon, Nadder, and Sem (specified OS grid references).
- Time spans cover mid-2013 through 2015 (exact From/To dates provided for each dataset; overall multiple-year periods).

## Datasets at a glance
- Discharge datasets (one file per site):
  - CE_Discharge_data.csv (River Ebble)
  - GA_Discharge_data.csv (River Avon)
  - GN_Discharge_data.csv (River Nadder)
  - AS_Discharge_data.csv (River Sem)
- Surface water chemistry datasets (one file per site):
  - CE_surfacewater_chemistry.csv
  - GA_surfacewater_chemistry.csv
  - GN_surfacewater_chemistry.csv
  - AS_surfacewater_chemistry.csv
- Each discharge file contains two columns: Date (dd/mm/yyyy) and Average daily discharge (m3/s).
- Each water chemistry file contains 14 columns: Site, date (dd/mm/yyyy), SSC (mg/L), Chloride (mg/L), Nitrate (mg/L), Sulphate (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), DOC (mg C/L).

## Field instrumentation and QA
- Field instruments:
  - HOBO U20-001-01 (Onset) at AS, GA, GN
  - Levelogger Edge (Solinst) at CE
  - Manta 2 (Eureka Water Probes) used as alternative instrumentation
- Hydrological quality control:
  - Stage measured at 15-minute intervals using the above transducers in perforated stilling wells.
  - Regular fortnightly manual discharge measurements via velocity-area method to establish stage-discharge relationships (available on request from Prof A Binley).
- Hydrological QA notes:
  - Data intended for time-series analyses; stage-discharge relationships underpin discharge calculations.

## Analytical chemistry quality control
- Suspended sediment concentration (SSC): filtration and gravimetric analysis.
- Anions (Chloride, Nitrate, Sulphate): Ion chromatography with detailed instrument setup; reported limits of detection and precision; CRM material used for accuracy checks.
- Cations (K, Mg, Na, Ca) and Si, Sr: ICP-OES with detailed detection limits and precision; CRM material used for accuracy checks.
- Total Phosphorus (Total P): autoclave digestion followed by Skalar Auto Analyser; LOD and CRM accuracy reported.
- Dissolved Organic Carbon (DOC): non-purgeable organic carbon method; LOD and CRM accuracy reported.
- Queries about datasets: contact Kate Heppell (email provided).

## Data structure and metadata
- Discharge datasets: 4 MS Excel spreadsheets; columns are Date (dd/mm/yyyy) and Average daily discharge (m3/s).
- Surface water chemistry datasets: 4 MS Excel spreadsheets; columns are Site, date (dd/mm/yyyy), SSC (mg/L), Chloride (mg/L), Nitrate (mg/L), Sulphate (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), DOC (mg C/L).
- Location references:
  - River Ebble: SU05598 25343
  - River Avon: SU09723 57824
  - River Nadder: ST92380 27376
  - River Sem: ST92346 27381

## Access and contact
- Any queries about these datasets should be sent to Kate Heppell (c.m.heppell@qmul.ac.uk).