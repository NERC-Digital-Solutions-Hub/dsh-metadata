# Discharge dataset and Surface water chemistry dataset

- Discharge datasets (4 files):
  - CE_Discharge_data.csv: Average daily discharge (m3/s) calculated from 15-minute stage data; data collected with Solinst pressure transducers; location SU05598 25343 (River Ebble); From 24-Sep-2013 to 02-Sep-2015.
  - GA_Discharge_data.csv: Average daily discharge (m3/s) calculated from 15-minute stage data; data collected with a Manta sonde; location SU09723 57824 (River Avon); From 18-Jun-2013 to 01-Jul-2015.
  - GN_Discharge_data.csv: Average daily discharge (m3/s) calculated from 15-minute stage data; data collected with HOBO pressure transducers; location ST92380 27376 (River Nadder); From 26-Jun-2013 to 29-Sep-2015.
  - AS_Discharge_data.csv: Average daily discharge (m3/s) calculated from 15-minute stage data; data collected with a Manta sonde; location ST92346 27381 (River Sem); From 18-Jun-2013 to 20-Aug-2015.

- Surface water chemistry datasets (4 files):
  - CE_surfacewater_chemistry.csv: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT; location SU05598 25343 (River Ebble); From 06-Jun-2013 to 02-Jun-2014.
  - GA_surfacewater_chemistry.csv: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT; location SU09723 57824 (River Avon); From 06-Jun-2013 to 02-Jun-2014.
  - GN_surfacewater_chemistry.csv: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT; location ST92380 27376 (River Nadder); From 06-Jun-2013 to 02-Jun-2014.
  - AS_surfacewater_chemistry.csv: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT; location ST92346 27381 (River Sem); From 06-Jun-2013 to 02-Jun-2014.

- Fieldwork instrumentation
  - HOBO U20-001-01 (Onset Corporation, USA)
  - Levelogger Edge (Solinst, Canada)
  - Manta 2 (Eureka Water Probes, USA)

- Hydrological quality control
  - Stage measured with 15-minute intervals using the specified instruments (HOBO at AS, GA, GN; Levelogger Edge at CE).
  - Fortnightly manual discharge measurements by velocity-area method to build stage-discharge relationships (available on request from a.binley@lancaster.ac.uk).

- Analytical chemistry quality control
  - Suspended sediment concentration (SSC) by filtration and gravimetric analysis.
  - Chloride, nitrate, sulphate measured by Ion Chromatography (IC) with specified columns and eluents; limits of detection and precision reported.
  - Major cations (K, Mg, Na, Ca), silica, and strontium measured by ICP-OES with specified limits of detection and precision; certified reference materials noted.
  - Total Phosphorus analyzed by autoclave digestion and Skalar Auto Analyzer; detection limit and CRM accuracy noted.
  - Dissolved Organic Carbon (DOC) measured by non-purgeable organic carbon method; detection limit and CRM accuracy noted.
  - All queries about these datasets should be sent to Kate Heppell (c.m.heppell@qmul.ac.uk).

- Data structure
  - Discharge datasets: 4 MS Excel spreadsheets, each with two columns - Date (dd/mm/yyyy) and Average daily discharge (m3/s).
  - Surface water chemistry datasets: 4 MS Excel spreadsheets, each with 14 columns - Site, date (dd/mm/yyyy), SSC (mg/L), Cl (mg/L), Nitrate (mg/L), Sulphate (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), and Dissolved Organic Carbon (mg C/L).

- Context and purpose
  - The datasets are designed to support analysis of discharge alongside water chemistry across four rivers (Ebble, Avon, Nadder, Sem) in the UK, enabling investigation of hydrological behavior and water quality through a self-service data approach.