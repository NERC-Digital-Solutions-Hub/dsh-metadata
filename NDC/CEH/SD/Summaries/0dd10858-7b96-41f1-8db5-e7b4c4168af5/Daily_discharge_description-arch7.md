# Discharge dataset (4 files), details as follows: Surface water chemistry dataset (4 files), details as follows

- Overview
  - Contains eight Excel spreadsheets: four discharge datasets and four surface water chemistry datasets from four sites (Ebble, Avon, Nadder, Sem) represented by OS Grid References.
  - Data supports map-based visualization of hydrological and water-quality variables across time and space.

- Discharge datasets (4 files)
  - Sites and locations
    - CE (River Ebble): OS Grid SU05598 25343
    - GA (River Avon): OS Grid SU09723 57824
    - GN (River Nadder): OS Grid ST92380 27376
    - AS (River Sem): OS Grid ST92346 27381
  - Time coverage and content
    - Average daily discharge (m3/s) derived from stage data using 15-minute intervals.
    - Each file covers a site-specific period (examples: CE from 24 Sept 2013/2020?; GA from 18 Jun 2013 to 01 Jul 2015; GN 26 Jun 2013 to 29 Sept 2015; AS 18 Jun 2013 to 20 Aug 2015).
  - Data structure
    - Each discharge spreadsheet: two columns — Date (dd/mm/yyyy) and Average daily discharge (m3/s).

- Surface water chemistry datasets (4 files)
  - Sites and locations
    - CE (River Ebble): OS Grid SU05598 25343
    - GA (River Avon): OS Grid SU09723 57824
    - GN (River Nadder): OS Grid ST92380 27376
    - AS (River Sem): OS Grid ST92346 27381
  - Time coverage and content
    - 2013–2014 period (14 June 2013 to 2 June 2014) for each site.
    - Analyzed via grab samples collected at 09:00 GMT on the date provided.
  - Data structure
    - Each water chemistry spreadsheet includes 14 columns: Site, date (dd/mm/yyyy), SSC (mg/L), Chloride (mg/L), Nitrate (mg/L), Sulphate (mg/L), Total P (mg/L), K (mg/L), Mg (mg/L), Na (mg/L), Ca (mg/L), Si (mg/L), Sr (mg/L), and DOC (mg C/L).

- Field instrumentation
  - Hydrological instrumentation used across sites: HOBO U20-001-01 (Onset), Levelogger Edge (Solinst), Manta 2 (Eureka Water Probes).

- Quality control and processing
  - Hydrological data
    - Stage measured with pressure transducers (HOBO U20-001-01 at AS, GA, GN; Levelogger Edge at CE) in a perforated stilling well at 15-minute intervals.
    - Fortnightly manual discharge measurements (when possible) to construct stage-discharge relationships per site (available on request from A. Binley).
  - Analytical chemistry quality control
    - SSC by gravimetric analysis after filtration.
    - Major ions (Cl−, NO3−, SO42−) by Ion Chromatography with specified limits of detection and precision (CRMs used for accuracy checks).
    - Major cations/Si/Sr by ICP-OES with detection limits and precision; CRMs used for accuracy.
    - Total Phosphorus by autoclave digestion and analysis with specified LOD and CRM checks.
    - Dissolved Organic Carbon by non-purgeable organic carbon method with specified LOD and CRM checks.
  - Data interpretation notes
    - Data consumers should account for differing data sources/resolutions and the documented QC procedures when integrating into GIS workflows.

- Access and contact
  - Inquiries about the datasets: Kate Heppell (c.m.heppell@qmul.ac.uk).
  - Stage-discharge relationships and related methodological details available from Prof A. Binley (a.binley@lancaster.ac.uk) on request.

- GIS considerations for use
  - Spatial referencing: OS Grid Coordinates provided for precise site locations; convert to preferred CRS (e.g., WGS84) for mapping.
  - Temporal alignment: Discharge data are daily averages (from 15-minute interval stage data) and surface chemistry data are 2013–2014, with hourly sampling times standardized to 09:00 GMT for chemistry; plan joins by Site and Date for time-series mapping.
  - Data integration: Combine across sites and variables (discharge, SSC, ions, DOC) to create multi-layer hydrological and water-quality maps; ensure handling of different data resolutions and QC levels.
  - Practical GIS tasks: data cleaning, missing value handling, reformatting to CSV/GeoJSON/Shapefile as needed, creating time-enabled maps and dashboards for stakeholders.