# Discharge dataset (4 files), details as follows:

- Overview
  - A set of hydrological datasets comprising discharge measurements and surface water chemistry from four sites/rivers (Ebble, Avon, Nadder, Sem).
  - Data are organized as daily discharge and grab-sample chemistry, with 15-minute interval stage data used to derive average daily discharge.
  - Locations are identified by OS Grid References:
    - Ebble: SU05598 25343
    - Avon: SU09723 57824
    - Nadder: ST92380 27376
    - Sem: ST92346 27381

- Datasets and contents
  - Discharge data (4 files)
    - CE_Discharge_data.csv
      - Description: Average daily discharge (m3/s) from stage data (15 min intervals) using Solinst pressure transducers.
      - From = 24- Sept-20 13; To = 02- Sept-20 15.
      - Location: River Ebble (OS Grid SU05598 25343).
    - GA_Discharge_data.csv
      - Description: Average daily discharge (m3/s) from stage data (15 min intervals) using a Manta sonde.
      - From = 18- Jun-201 3; To = 01- July-201 5.
      - Location: River Avon (OS Grid SU09723 57824).
    - GN_Discharge_data.csv
      - Description: Average daily discharge (m3/s) from stage data (15 min intervals) using HOBO pressure transducers.
      - From = 26- Jun-201 3; To = 29- Sept-20 15.
      - Location: River Nadder (OS Grid ST92380 27376).
    - AS_Discharge_data.csv
      - Description: Average daily discharge (m3/s) from stage data (15 min intervals) using a Manta sonde.
      - From = 18- Jun-201 3; To = 20- Aug-201 5.
      - Location: River Sem (OS Grid ST92346 27381).
  - Surface water chemistry data (4 files)
    - CE_surfacewater_chemistry.csv
      - Description: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT on provided dates.
      - From = 06- Jun-201 3; To = 02- June-2014.
      - Location: River Ebble (OS Grid SU05598 25343).
    - GA_surfacewater_chemistry.csv
      - Description: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT on provided dates.
      - From = 06- Jun-201 3; To = 02- June-2014.
      - Location: River Avon (OS Grid SU09723 57824).
    - GN_surfacewater_chemistry.csv
      - Description: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT on provided dates.
      - From = 06- Jun-201 3; To = 02- June-2014.
      - Location: River Nadder (OS Grid ST92380 27376).
    - AS_surfacewater_chemistry.csv
      - Description: Surface water chemistry analysed from grab samples collected by automatic water sampler at 09:00 GMT on provided dates.
      - From = 06- Jun-201 3; To = 02- June-2014.
      - Location: River Sem (OS Grid ST92346 27381).

- Fieldwork instrumentation
  - HOBO U20-001-01 (Onset Corporation, USA)
  - Levelogger Edge (Solinst, Canada)
  - Manta 2 (Eureka Water Probes, USA)

- Hydrological quality control
  - Stage measured by pressure transducers (HOBO U20-001-01 at AS, GA, GN; Levelogger Edge at CE) in a perforated stilling well, logged at 15-minute intervals.
  - Fortnightly manual discharge measurements using velocity-area method (when possible) to build stage-discharge relationships (available from Prof A Binley on request).

- Analytical chemistry quality control
  - Suspended sediment concentration (SSC): Filtration (GF/C) + gravimetric analysis.
  - Chloride, nitrate, sulphate: Ion chromatography (0.45 μm filtered samples); LODs and RSDs provided; CRM with stated accuracy.
  - Major cations (K, Mg, Na, Ca), silica (Si), strontium (Sr): ICP-OES (axial) with reagent spike; LODs and RSDs provided; CRM with accuracy.
  - Total phosphorus: Autoclave digestion + Skalar Auto Analyser; LOD and CRM details provided.
  - Dissolved organic carbon (DOC): non-purgeable organic carbon method; LOD and CRM details provided.
  - Contact for queries: Kate Heppell (c.m.heppell@qmul.ac.uk).

- Data structure and format
  - Data package comprises 8 MS Excel/CSV spreadsheets:
    - Discharge: 4 spreadsheets
      - Each with two columns: Date (dd/mm/yyyy) and Average daily discharge (m3/s).
    - Surface water chemistry: 4 spreadsheets
      - Each with 14 columns: Site, date (dd/mm/yyyy), SSC (mg/L), Chloride (mg/L), Nitrate (mg/L), Sulphate (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), DOC (mg C/L).

- Access and provenance
  - Data quality controls, measurement methods, and analytical details are documented to support reuse.
  - Any queries about the datasets should be directed to Kate Heppell at the provided email.