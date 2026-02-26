# UK Environmental Change Network (ECN) precipitation chemistry data: 1992-2012

## Overview
- Dataset originator: ECN Data Centre (Centre for Ecology and Hydrology).
- Data providers: UK agencies and departments coordinating ECN, including DEFRA, Natural England, Natural Environment Research Council, Scottish Government, and others.
- Acknowledgement: Users should acknowledge ECN data and provide one reprint of any publication citing the data.
- Protocol highlights: Bulk collectors measure weekly precipitation chemistry; a standard QC solution is analysed alongside field samples for quality control; users should consult accompanying quality information.

## Data Provenance and Documentation
- Supporting documentation linked to: ECN precipitation chemistry data (1992-2012) with additional details in ECN_PC2.csv.
- Additional analytical information: ECN_PC2.csv provides detailed sampling and analysis timestamps (deployment, sampling, filtration, and analysis completion).

## Data Structure
- Primary data fields: SITECODE, SDATE (sample date), FIELDNAME (variable measured), VALUE (measured value); VOLUME (sample volume) is also recorded.
- Supplementary metadata: QUALITY codes (Q1–Q6) describing data quality or issues.
- Quality information: A quality code scheme is provided to flag data issues, with a separate text for unusual events (code 999).

## Sites and Temporal Coverage
- 12 ECN sites (Drayton, Glensaugh, Hillsborough, Moor House - Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms).
- Location coordinates are provided for each site.
- Date ranges vary by site; most sites span 1993–2012, with Porton Down having 1996–2000.

## Measured Variables (Fieldnames)
- Alkalinity (ALKY), Aluminium, Calcium, Chloride, Colour (absorbance), Conductivity (CONDY), Dissolved Organic Carbon (DOC), Iron, Magnesium, Ammonium (NH4N), Nitrate Nitrogen (NO3N), pH, Aquacheck pH readings (PHAQCS, PHAQCU), Phosphate Phosphorus (PO4P), Potassium, Sulphate (SO4S), Sodium, Total Nitrogen (TOTALN), Total Phosphorus (TOTALP).
- Sample and measurement details: Volume (ml); quality codes Q1–Q6 accompany measurements.

## Quality and Metadata
- Quality codes (100–999) indicate data reliability and potential issues (e.g., 100 No information; 101 No sample/readings; 501–506 laboratory issues; 999 Unusual event).
- Environment and sampling notes: Codes capture issues like snow, debris, weather interruptions, sampling timing, and lab-related problems.
- Quality context: Site managers assign codes; unusual events are documented in accompanying quality text.
- Importance for analysis: Use the accompanying ECN quality information to assess data suitability and filter questionable records.

## Additional Documentation and Access
- ECN_PC2.csv provides extended metadata on sampling deployment, timestamps, lab analyses, and processing steps.
- DOI link available for the ECN precipitation chemistry data documentation.
- Data use and integration: Data are designed to be discoverable with metadata; researchers are encouraged to couple chemical measurements with quality flags for robust analysis.

## Practical Considerations for Analysts
- Data at local/nested scales with potential gaps; expect missing values and quality-coded records needing filtering.
- Temporal coverage is extensive (1992–2012), but Porton Down ends in 2000; cross-site harmonization may require attention to QA/QC notes.
- Data come from multiple sites with standardized but site-specific quality codes; consult ECN_PC2.csv and quality code descriptions before modeling.
- Useful for correlation studies, trend analyses, and prediction of environmental change impacts, while ensuring data provenance and quality constraints are acknowledged.