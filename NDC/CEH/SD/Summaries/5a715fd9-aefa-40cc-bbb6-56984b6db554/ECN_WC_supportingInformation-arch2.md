# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Overview
  - Long-term dataset of surface water chemistry from the UK Environmental Change Network (ECN) across multiple sites, sampled weekly using dip samples.
  - Data are produced and quality assured via a standard protocol and shared with clear quality control information.
  - Researchers are encouraged to acknowledge ECN and provide a reprint of publications citing ECN data.

- Data provenance and providers
  - Data originator: ECN Data Centre, CEH.
  - Data providers: ECN programme funded by a consortium of UK government departments and agencies (including DEFRA, Environment Agency, Natural England, Nuclear agencies, devolved administrations, etc.).
  - Acknowledgement and data citation: Required acknowledgment of ECN usage; return one reprint of any publication citing ECN data.
  - Protocol reference: surfaceWaterChemistryProtocol.pdf accompanying the dataset.

- Sampling protocol and QA
  - Sampling: weekly dip sampling of stream water chemistry.
  - Quality assurance: standard QC solution sent to laboratories to run alongside field samples; QC data included with the dataset.
  - Usage note: apply accompanying quality information when analyzing data.

- Data structure
  - Core data fields:
    - SITECODE: unique ECN site dataset identifier.
    - LCODE: site-specific replication/location code for core measurements.
    - SDATE: sampling date.
    - FIELDNAME: variable measured (e.g., ALKY, CALCIUM, NO3N, etc.).
    - VALUE: measured value.
  - Additional analytical information: ECN_WC2.csv includes sampling time details and lab metadata:
    - SHOUR, SMINS: sampling time.
    - LAB_NID: laboratory performing analyses.
    - PHDATE/PHHOUR/PHMINS: pH measurement timing.
    - FILTDATE/COMPDATE: sample filtration and analysis completion dates.

- Site codes and site details
  - Example sites and locations:
    - T02 Glensaugh (57° 54' 33.36" N, 2° 33' 12.14"W); date ranges from 1993–2012.
    - T04 Moor House - Upper Teesdale; multiple location codes with varying date ranges across 1992–2011.
    - T05 North Wyke; date ranges 1993–2012 (three location codes).
    - T06 Rothamsted; 1994–2012.
    - T07 Sourhope; 1993–2012 (locations 1–2).
    - T08 Wytham; several location codes spanning 1993–2012.
    - T11 Y Wyddfa – Snowdon; 1997–2012.
    - T12 Cairngorms; 1999–2012.
  - Each site has its own code (LCODE) and sampling point configurations; date ranges indicate data availability per location code.

- Fieldnames and units
  - Common chemical parameters include:
    - ALKY (Alkalinity) – mg/L
    - ALUMINIUM – mg/L
    - CALCIUM – mg/L
    - CHLORIDE – mg/L
    - COLOUR – absorbance (nM)
    - CONDY (Conductivity) – µS/cm
    - DOC (Dissolved Organic Carbon) – mg/L
    - IRON – mg/L
    - MAGNESIUM – mg/L
    - NH4N (Ammonium) – mg/L
    - NO3N (Nitrate-N) – mg/L
    - pH (pH units)
    - PHAQCS/PHACQU – pH (Aquacheck) – pH units
    - PO4P (Phosphate P) – mg/L
    - POTASSIUM – mg/L
    - SO4S (Sulfate S) – mg/L
    - SODIUM – mg/L
    - STAGE – stage reading of water level (mm)
    - TOTALN – mg/L
    - TOTALP – mg/L
  - Field names are standardized with corresponding units as listed.

- Quality codes and data quality
  - ECN quality codes are assigned by site managers from a standard list (plus 999 for unusual events requiring text explanation):
    - 100 No information available
    - 101 No sample/reading taken
    - 102 Sample lost or discarded
    - 103 Partial loss of sample
    - 105–119, 126–170, 182, 191, 200, 203, 207–211, 222, 229, 501–511: various site/field and laboratory issues (e.g., weather effects, debris, lab contamination, insufficient sample, equipment failure, unusual events)
    - 999 Unusual event – see accompanying quality text
  - Quality information accompanying the dataset should be consulted to interpret any affected measurements.

- Usage guidance for analysts
  - Leverage standardized methods and array of sites to assess environmental condition and policy performance over time.
  - Use the QA/QC information and ECN_WC2.csv metadata to interpret timing, lab, and data quality.
  - Store and share derived datasets via appropriate portals; cite ECN data and acknowledge usage as requested.

- Endnotes
  - The dataset emphasizes long-term environmental monitoring with standardized data structures, quality control, and explicit site-specific metadata to support robust environmental health assessments and policy evaluation.