# Discharge dataset (4 files), details as follows: and Surface water chemistry dataset (4 files)

- Purpose and scope
  - Provide time-series records of river discharge and surface water chemistry for four sites (Ebble, Avon, Nadder, Sem).
  - Enable environmental monitoring and analysis of hydrology and water-quality trends over the specified periods.

- Datasets overview
  - Discharge data (4 files)
    - CE_Discharge_data.csv: From 24- Sept-20 to 02- Sept-20; average daily discharge (m3/s) from stage data (15-min intervals) using Solinst pressure transducers; River Ebble; OS Grid SU05598 25343.
    - GA_Discharge_data.csv: From 18- Jun-2013 to 01- July-2015; average daily discharge (m3/s) from stage data (15-min intervals) using a Manta sonde; River Avon; OS Grid SU09723 57824.
    - GN_Discharge_data.csv: From 26- Jun-2013 to 29- Sept-2015; average daily discharge (m3/s) from stage data (15-min intervals) using HOBO pressure transducers; River Nadder; OS Grid ST92380 27376.
    - AS_Discharge_data.csv: From 18- Jun-2013 to 20- Aug-2015; average daily discharge (m3/s) from stage data (15-min intervals) using a Manta sonde; River Sem; OS Grid ST92346 27381.
  - Surface water chemistry data (4 files)
    - CE_surfacewater_chemistry.csv: 06- Jun-2013 to 02- Jun-2014; surface water chemistry from grab samples collected at 09:00 GMT; River Ebble; OS Grid SU05598 25343.
    - GA_surfacewater_chemistry.csv: 06- Jun-2013 to 02- Jun-2014; grab-sample chemistry at 09:00 GMT; River Avon; OS Grid SU09723 57824.
    - GN_surfacewater_chemistry.csv: 06- Jun-2013 to 02- Jun-2014; grab-sample chemistry at 09:00 GMT; River Nadder; OS Grid ST92380 27376.
    - AS_surfacewater_chemistry.csv: 06- Jun-2013 to 02- Jun-2014; grab-sample chemistry at 09:00 GMT; River Sem; OS Grid ST92346 27381.

- Data collection and instrumentation
  - Field instrumentation
    - HOBO U20-001-01 (Onset), Levelogger Edge (Solinst), Manta 2 devices used to log water stage and discharge.
  - Fieldwork operations
    - Stage-discharge relationships developed from regular (fortnightly when possible) manual discharge measurements using velocity-area method (available on request).

- Quality control and analytical methods
  - Hydrological quality control
    - Stage measured with pressure transducers at sites AS, GA, GN (HOBO U20-001-01) and CE (Levelogger Edge) at 15-min intervals.
  - Analytical chemistry quality control
    - Suspended Sediment Concentration (SSC): filtration (GF/C) and gravimetric analysis.
    - Anions/cations: chloride, nitrate, sulfate by ion chromatography with specified columns and reagents; LODs and RSDs provided; CRM materials used for accuracy checks.
    - Major ions (K, Mg, Na, Ca, Si, Sr) by ICP-OES with acidification; LODs and RSDs provided; CRM materials used for accuracy checks.
    - Total Phosphorus: autoclave digestion followed by Skalar Auto Analyser; LOD and CRM checks provided.
    - Dissolved Organic Carbon (DOC): non-purgeable organic carbon method; LOD and CRM checks provided.
  - Data quality notes
    - Comprehensive method details and accuracy metrics (LOD, RSD, CRM performance) are documented; any dataset queries should be directed to Kate Heppell.

- Data structure and format
  - Discharge datasets
    - Each file contains two columns: Date (dd/mm/yyyy) and Average daily discharge (m3/s).
  - Surface water chemistry datasets
    - Each file contains 14 columns: Site, Date (dd/mm/yyyy), SSC (mg/L), Cl (mg/L), NO3 (mg/L), SO4 (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), DOC (mg C/L).

- Access and contact
  - For dataset queries or data access, contact: Kate Heppell (c.m.heppell@qmul.ac.uk).