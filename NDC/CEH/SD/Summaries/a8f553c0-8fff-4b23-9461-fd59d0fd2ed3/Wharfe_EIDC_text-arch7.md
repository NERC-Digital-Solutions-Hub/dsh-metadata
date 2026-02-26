# Faecal bacteria concentration in the River Wharfe from 2019 to 2021

- Dataset of faecal bacteria concentrations (total coliforms TC, Escherichia coli E. coli, and Intestinal enterococci IE) expressed as colony forming units per 100 ml (cfu/100 ml) from River Wharfe water samples and selected tributaries.
- Timeframe: irregular sampling from April 2019 to September 2021.
- geographic focus: sites mainly upstream and downstream of Ilkley Sewage Treatment Works (STWs) in West Yorkshire, with two datasets covering sites along the full river length.
- Purpose: raise awareness of faecal bacteria pollution, identify sources (upstream and near point sources), and support policy actions.

## Data content and geographic scope

- Sites listed downstream from the headwaters near Oughtershaw to the Wharfe–Ouse junction at Cawood; coordinates provided (latitude in column C, longitude in column D).
- Sampling at recreational hotspots or suspected sources of faecal bacteria (near STWs or inflowing tributaries); proxy sites used when a downstream site better represents conditions (column E).

## Data structure and columns (A–J)

- A: Site name.
- B: Site type (main river or tributary).
- C: Latitude.
- D: Longitude.
- E: Proxy site indicator (when applicable).
- F: Sample code for the iWharfe2020 project (sample code_iW_20).
- G: Sample code for the iWharfe_Upper project (sample code iW_Upp).
- H: Sample code for the iWharfe2021 project (sample code iW_21).
- I: Sample code for Wharfe Addingham Environment Group (sample code AEG).
- J: Sample code for Wharfe Ashlands (sample code Ashlands).
- Notes on sampling types: Duplicate samples marked with P (Primary) and D (Duplicate); one instance of a trampling (TS) sample to re-suspend sediment.

## Sampling methods and workflow

- Field collection conducted by trained volunteers using ~350 ml sterile bottles.
- Low-flow collection by wading; higher-flow collection via bottle on weighted rope or from river bank.
- Samples kept in a cool bag with ice packs and transported overnight to ALS Ltd lab in Coventry.
- Analysis started within 24 hours of collection using standard dilution, incubation, and counting methods; lab protocols available on the ALS Ltd website.

## Project provenance and data management

- Data collected as part of multiple projects with overlapping sites:
  - iWharfe2020 (iW_20)
  - iWharfe_Upper (iW_Upp)
  - iWharfe2021 (iW_21)
  - Wharfe Addingham Environment Group (AEG)
  - Wharfe Ashlands (Ashlands)
- Rick Battarbee designed the project and oversaw field sampling, transport, and interpretation.
- Malcolm Secrett helped organise field sampling, manage data, and interpret results.

## Temporal and data quality considerations for GIS use

- Temporal coverage: April 2019 to September 2021 with irregular sampling intervals; some sites have duplicate or proxy measurements.
- Data from multiple projects require careful harmonisation (e.g., aligning sample codes and project identifiers).
- Variants in sampling location (direct site vs. proxy site) and occasional special samples (TS, D) should be captured in GIS metadata.
- The dataset provides precise geographic coordinates enabling map-based visualization of contaminant concentrations along the River Wharfe and near potential pollution sources (STWs and tributaries).

## GIS applications and use cases

- Visualise spatial patterns of faecal bacteria concentrations along the river network.
- Analyze proximity and potential impact of STWs and tributaries on water quality.
- Compare concentration trends across different projects and over time.
- Integrate with policy or public health analyses to support Bathing Water designations or water quality management decisions.
- Use coordinates and site types to create layered maps (main river vs. tributary, proxy sites) and time-series charts by site.