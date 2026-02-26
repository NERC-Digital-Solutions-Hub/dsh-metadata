# UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012

## Overview
- ECN precipitation chemistry dataset collected by the ECN Data Centre, with data providers including multiple UK government departments and agencies.
- Weekly bulk-collector samples processed from 12 ECN sites (1992–2012, with varying end dates; some sites end earlier).
- Measurements cover a wide range of chemical constituents and related properties, suitable for GIS-based mapping and analysis of spatial and temporal trends.
- Data published with accompanying quality information and standard QA/QAQC procedures.

## Data Content and Scope
- Data structure: each record includes SITECODE (site identifier), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measurement).
- Sites: 12 sites labeled T01–T12 with site names, coordinates, and dataset date ranges (e.g., T01 Drayton, etc.).
- Fieldnames cover major chemical and physical parameters: alkalinity (ALKY), aluminium, calcium, chloride, colour (absorbance), conductivity, dissolved organic carbon (DOC), iron, magnesium, ammonium, nitrate nitrogen, pH, Aquacheck pH readings (PHAQCS, PHAQCU), phosphate, potassium, sulphate, sodium, total nitrogen, total phosphorus, sample volume, and quality codes (Q1–Q6).
- Supporting data: Additional metadata in ECN_PC2.csv with deployment and sampling timing (dates, hours, minutes) and laboratory information.

## Data Structure and Schema
- Primary table fields: SITECODE, SDATE, FIELDNAME, VALUE, plus VOLUME and associated quality codes (Q1–Q6).
- Quality codes accompany measurements to indicate data quality issues or anomalies as defined by ECN.

## Site Details
- T01–T12 sites with names, geographic coordinates, and the date range covered in the dataset (varies by site; e.g., T10 Porton Down has 1996–2000, others extend to 2012).

## Data Quality and Processing
- Bulk collectors used; weekly sampling with standard QA solution analyzed in parallel for quality control.
- Users should consult accompanying quality information to assess data suitability for analysis.
- Quality codes allow flags for issues such as sample loss, contamination, equipment problems, environmental interferences, or unusual events.

## Quality Codes Summary
- Standard ECN quality codes include numeric codes (100–133, 180, 182, 187, 191, 200, 222, 223, 501–507, 508–510, 511) plus 999 for unusual events described in accompanying quality text.
- Examples: 100 No information; 101 No sample/reading; 501–507 laboratory-related issues; 999 unusual event with explanatory text.

## Additional Documentation and Access
- Supporting documentation: UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012 (doi: http://doi.org/10.5285/0cd4abd2-1bc9-48bc-b5c2-cebdeaa23ceb).
- Additional metadata file: ECN_PC2.csv detailing deployment timing, sampling, and lab information.
- Data usage: ECN requests acknowledgement of data use and requests a reprint of any publication that cites the dataset.