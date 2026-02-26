# ECN Data Centre – Soil Solution Chemistry Dataset

## Overview
- A dataset describing soil solution chemistry measurements collected by suction samplers across multiple ECN sites.
- Collected fortnightly; aims to support environmental change monitoring and policy evaluation.
- Standardised protocols and quality checks to enable cross-site comparability.

## Dataset Originator and Owners
- Originator: ECN Data Centre (http://data.ecn.ac.uk).
- Owners: UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies (e.g., DEFRA, Natural England, NERC, SEPA, etc.).
- Usage acknowledgement: ECN requests acknowledgement of data use and one reprint of any publication citing ECN data.

## Protocol and Data Quality
- Standard Operating Procedures (SOPs) ensure data comparability across sites; ss.pdf explains data collection methods.
- Quality control: a standard QC solution is analyzed alongside field samples; QC data are available and should be used when interpreting data.
- Replicate handling: samplers may be replaced (new replicate ID); insufficient sampling can lead to bulked samples with special replicate IDs (XXS for shallow, XXD for deep).
- Data governance: data are quality assured, cleaned, transformed, analysed, and presented in reports, charts, or dashboards; underlying data should be shared appropriately.

## Usage Notes (Measurement and Sampling Details)
- Suction samplers measure soil solution chemistry; sampling is fortnightly.
- Replacement of samplers triggers new replicate IDs.
- Bulk sampling is allowed when individual samplers yield insufficient samples, flagged by RID codes.
- Quality control: a standard QC solution is analyzed with field samples; QC data accompany the dataset.

## Data Download and File Schema
- Core dataset fields:
  - SITECODE: unique code for each ECN Site
  - SDATE: sampling date
  - RID: replicate ID
  - FIELDNAME: variable measured
  - VALUE: measured value
- Supporting data files provide deeper lab analyses and quality information (see below).

## Supporting Documentation

- ECN_SS2.csv
  - Lab analysis details for ECN samples
  - Fields include SITECODE, RID, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE
- ECN_SS_qtext.csv
  - Quality codes assigned by site managers with explanatory text for unusual events
  - Fields include SITECODE, FIELDNAME, FROM_DATE, TO_DATE, DATETYPE, CONTINUING
- ECN_QC1.csv
  - Quality control solution data for field samples
  - Fields: SITECODE, SDATE, FIELDNAME, VALUE
- ECN_QC2.csv
  - Additional laboratory analysis information for QC samples
  - Fields include SITECODE, FROMDATE, FROMHOUR, FROMMINS, SDATE, SHOUR, SMINS, LAB_NID, PHDATE, PHHOUR, PHMINS, FILTDATE, COMPDATE
- Site codes and locations
  - T01–T12 with site names and geographic coordinates (e.g., Drayton, Glensaugh, Hillsborough, Moor House – Upper Teesdale, etc.)
  - Link for further site information: https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27

## Variable Information (FIELDNAME) and Units
- Alkalinity (ALKY) — mg per litre
- Aluminium (ALUMINIUM) — mg per litre
- Calcium (CALCIUM) — mg per litre
- Chloride (CHLORIDE) — mg per litre
- Colour (COLOUR) — absorbance at 436 nm (nM)
- Conductivity (CONDY) — microSiemens per centimetre
- Dissolved Organic Carbon (DOC) — mg per litre
- Iron (IRON) — mg per litre
- Magnesium (MAGNESIUM) — mg per litre
- Ammonium (NH4N) — mg per litre
- Nitrate Nitrogen (NO3N) — mg per litre
- pH (PH) — pH scale 1-14
- Aquacheck pH measurements (PHAQCS, PHAQCU) — pH scale 1-14
- Phosphate Phosphorus (PO4P) — mg per litre
- Potassium (POTASSIUM) — mg per litre
- Sulphate Sulphur (SO4S) — mg per litre
- Sodium (SODIUM) — mg per litre
- Total Nitrogen (TOTALN) — mg per litre
- Total Dissolved Phosphorus (TOTALP) — mg per litre
- Vacuum (VACUUM) — bar
- Volume of sample collected (VOLUME) — ml
- Quality codes (Q1–Q5) — data quality indicators

## Quality Codes
- 100–104, 106, 108, 110, 111, 113, 115, 122–126, 137, 140, 160, 182, 200–223: various conditions affecting data quality (e.g., no information, sample issues, equipment, weather, unusual events).
- 501–507: laboratory-related issues (no sample, lost sample, contamination, insufficient sample, equipment failure, pre-filtered sample).
- 508–509: deposits on filter (black/brown material).
- 511: no separate acidified sub-sample for Al and Fe.
- 999: unusual event (see accompanying quality text).

## Site Information
- 12 ECN sites (T01 Drayton to T12 Cairngorms) with specific geographic coordinates provided in the documentation.
- Additional information about ECN sites available via the provided catalogue link.

## Relevance for Monitoring Framework Authors
- Provides a clear, standardized data structure with site-by-site comparability and documented protocols, essential for evaluating and comparing environmental health metrics across policy interventions.
- Emphasises the importance of metadata, quality control, and governance in datasets used to inform decisions.
- Highlights practical barriers and considerations for public data sharing, metadata completeness, timely access, and cross-organisational data silos.
- Demonstrates a workflow for data governance, including replication management, quality assessment, data assimilation, and dissemination through reports and dashboards.