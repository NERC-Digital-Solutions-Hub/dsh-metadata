# Discharge dataset (4 files), details as follows:

- Datasets included
  - Discharge data (4 files)
    - CE_Discharge_data.csv: From 24- Sept-20 13 to 02- Sept-20 15; Average daily discharge (m3/s) calculated from stage data (15 min intervals) collected using Solinst pressure transducers; Location: SU05598 25343 (River Ebble).
    - GA_Discharge_data.csv: From 18- Jun-201 3 to 01- July-201 5; Average daily discharge (m3/s) calculated from stage data (15 min intervals) collected using a Manta sonde; Location: SU09723 57824 (River Avon).
    - GN_Discharge_data.csv: From 26- Jun-201 3 to 29- Sept-20 15; Average daily discharge (m3/s) calculated from stage data (15 min intervals) collected using HOBO pressure transducers; Location: ST92380 27376 (River Nadder).
    - AS_Discharge_data.csv: From 18- Jun-201 3 to 20- Aug-201 5; Average daily discharge (m3/s) calculated from stage data (15 min intervals) collected using a Manta sonde; Location: ST92346 27381 (River Sem).
  - Surface discharge data structure: 4 spreadsheets per file; each with Date (dd/mm/yyyy) and Average daily discharge (m3/s).

- Fieldwork instrumentation
  - HOBO U20-001-01 (Onset, USA)
  - Levelogger Edge (Solinst, Canada)
  - Manta 2 (Eureka Water Probes, USA)

- Hydrological quality control
  - Stage measured with pressure transducers (HOBO U20-001-01 at AS, GA, GN; Levelogger Edge at CE) in perforated stilling wells at 15-minute intervals.
  - Fortnightly manual discharge measurements via velocity-area method to create site-specific stage-discharge relationships (available on request from Prof A Binley).

- Analytical chemistry quality control
  - Suspended Sediment Concentration (SSC) via filtration and gravimetric analysis.
  - Chloride, nitrate, sulfate by ion chromatography with specified limits of detection and relative standard deviations; use of certified reference materials (CRMs) for accuracy checks.
  - Major ions (K, Mg, Na, Ca, Si, Sr) by ICP-OES with specified detection limits and RSDs; CRMs used.
  - Total Phosphorus by autoclave digestion with Skalar Auto Analyzer; LOD and CRM checks.
  - Dissolved Organic Carbon (DOC) by non-purgeable organic carbon method with LOD and CRM checks.
  - Queries about datasets: c.m.heppell@qmul.ac.uk.

- Data structure (content and format)
  - Discharge spreadsheets: 2 columns each — Date (dd/mm/yyyy) and Average daily discharge (m3/s).
  - Surface water chemistry spreadsheets: 14 columns — Site, date (dd/mm/yyyy), Suspended Sediment Concentration (SSC mg/L), Chloride (mg/L), Nitrate (mg/L), Sulfate (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), and Dissolved Organic Carbon (mg C/L).

- Metadata and provenance notes
  - Locations provided as OS Grid References for each site.
  - Temperature, sampling time (09:00 GMT for surface chemistry), and instrument types documented.
  - Data availability and update expectations implied by QC practices and site-specific stage-discharge relationships; contact for data curves: Prof A Binley (a.binley@lancaster.ac.uk).

- Governance and stewardship considerations
  - Standardized field methods and reporting formats support interoperability across sites.
  - Clear lineage from field measurements to processed discharge values and chemistry results.
  - Fixed column schemas facilitate cataloguing and discovery; ensure consistent date formatting and units across portals.
  - Recommended stewardship actions: verify metadata completeness, ensure consistent instrument calibration status, maintain the linkage between discharge and chemistry datasets, and apply the documented QC procedures to new updates.