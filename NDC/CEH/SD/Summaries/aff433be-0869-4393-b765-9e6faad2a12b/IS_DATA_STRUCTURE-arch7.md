# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview
- UK Environmental Change Network (ECN) dataset documenting spittle bug (Neophilaenus sp.) populations and adult colour morphs across multiple sites.
- Data are collected annually via standard protocols to enable cross-site comparability.
- Two main downloadable CSV files:
  - ECN_ISN.csv: nymph density data by site, location, date and species.
  - ECN_ISA.csv: adult colour morph data by site, location, date.
- Accompanying documentation and quality data files describe data quality and potential influencing factors.

## Datasets and Structure
- ECN_ISN.csv (nymph data)
  - Core fields per record: SITECODE (site code), LCODE (location ID within site), SDATE (sampling date), ISN_SPEC (nymph species code: P = Philaenus spumaris; N = Neophilaenus lineatus), FIELDNAME (variable measured; e.g., spittle counts in quadrats), VALUE (observed value).
  - Additional fields with suffixes 1 and 2 for multiple observations per row include NSPITCHK, MEANNYM, NMAL, NFEM, NTOT, and Q1–Q8 (quality codes).
  - Usage notes: data are recorded once per year; use accompanying quality information.
- ECN_ISA.csv (adult colour morph data)
  - Core fields per record: SITECODE, LCODE, SDATE, ISA_MORPH (adult colour morph), FIELDNAME, VALUE.
  - Additional fields with suffixes 1 and 2 for quality codes (Q1–Q8) and related metrics similar to the nymph dataset.
  - Usage notes: data are recorded once per year; use accompanying quality information.

## Site Codes and Locations
- Explanatory Information: Site Codes map T01–T12 to site names and exact coordinates.
  - Example entries include Drayton (T01), Glensaugh (T02), Hillsborough (T03), Moor House, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms.
- Location coordinates are provided for GIS mapping; full site details available via the ECN catalogue link:
  - https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

## Variable Descriptions
- FIELDNAME values for nymph data describe the number of spittles in quadrats 1–40 and related measurements (e.g., NSPITCHK, MEANNYM, NMAL, NFEM, NTOT).
- For adult data, ISA_MORPH codes define colour morphs (ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU).
- The dataset includes explanatory information for FIELDNAME values and the mapping of site codes and morph codes.

## Quality and Supporting Documentation
- ECN quality codes are provided in the data files (Q1–Q8 alongside each observation) to flag factors affecting data quality.
- Supporting quality text files provide detailed descriptions of unusual events or conditions:
  - ECN_ISN_qtext.csv (nymph data)
  - ECN_ISA_qtext.csv (adult data)
- Quality codes include a broad range (100–513, 999 for unusual events) with accompanying date ranges and ongoing flags (CONTINUING).
- Purpose: to enable GIS specialists to assess data reliability and annotate maps with quality considerations.

## Explanatory Information
- Site Codes: mapping between site codes (T01–T12) and site names, plus precise coordinates.
- Variable Descriptions: detailed definitions for FIELDNAME entries (e.g., number of spittles per quadrat) and measurement units.
- Quality Codes: long list describing common data quality issues and environmental/plot conditions that may impact measurements.

## Usage and Attribution
- ECN requests acknowledgment of data usage to gauge dataset utilization and demonstrate value for environmental change research.
- A reprint of any publication citing ECN data should be sent to ECN.

## Access and Documentation
- Data download: ECN_ISN.csv and ECN_ISA.csv, plus quality-related and explanatory documentation.
- Protocols: ECN maintains standard operating procedures to ensure comparability across sites; see accompanying is.pdf for collection methodology.
- Additional site information and metadata available at the ECN and CEH catalogues:
  - ECN site information: ECN_ISN_qtext.csv and ECN_ISA_qtext.csv
  - ECN catalogue: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

## Summary for GIS Specialists
- Rich, geolocated dataset ideal for map-based analytics of spittle bug populations and adult morph distributions across UK ECN sites.
- Two primary data streams (nymph density and adult colour morphs) with annual temporal resolution and site-level coordinates suitable for choropleth, heatmap, or presence-absence visualizations.
- Data quality is integrated at the observation level via Q1–Q8 codes and explanatory text; unusual events are captured in ECN_ISN_qtext.csv and ECN_ISA_qtext.csv.
- Site metadata (site codes, names, and coordinates) enables precise spatial joins and map rendering.
- Proper use requires adherence to ECN protocols, acknowledgment in publications, and access to accompanying documentation for field definitions and quality context.