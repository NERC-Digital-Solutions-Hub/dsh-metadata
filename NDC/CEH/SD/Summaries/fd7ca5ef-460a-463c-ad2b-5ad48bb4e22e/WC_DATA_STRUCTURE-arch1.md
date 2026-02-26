# Dataset Originator ECN Data Centre

- Overview
  - Long-term dataset of stream water chemistry collected from ECN sites.
  - Dip samples collected weekly; data include lab analyses and quality control information.
  - Supporting metadata describes sites, variables, and quality codes to enable comparable analyses across sites.

- Data provenance
  - Data Originator: ECN Data Centre, Centre for Ecology and Hydrology (CEH)
  - Data Providers: UK Environment agencies and research bodies including DEFRA, Natural England, Scottish and Welsh agencies, NERC, and others listed in the document
  - Usage acknowledgement: Please acknowledge ECN data and send one reprint of any publication that cites the data

- Protocol and quality assurance
  - Standard operating procedures ensure comparability across ECN sites (refer to wc.pdf for data collection methods)
  - Weekly dip sampling of stream water chemistry
  - Quality control: a standard QC solution is analysed with field samples; use accompanying QC information
  - Quality information should be used in data analysis

- Data structure and download content
  - Primary download fields: SITECODE (ECN Site code), LCODE (location ID within site), SDATE (sampling date), FIELDNAME (measured variable), VALUE (measured value)
  - Supporting documentation: ECN_WC2.csv (lab analysis details)
  - Quality documentation: ECN_WC_qtext.csv (site manager quality notes with codes), ECN_QC1.csv and ECN_QC2.csv (QC solution data and lab analysis details)

- Site codes and locations
  - T02: Glensaugh (56° 54' 33.36" N, 2° 33' 12.14" W)
  - T04: Moor House - Upper Teesdale (54° 41' 42.15" N, 2° 23' 16.26" W)
  - T05: North Wyke (50° 46' 54.96" N, 3° 55' 4.10" W)
  - T06: Rothamsted (51° 48' 12.33" N, 0° 22' 21.66" W)
  - T07: Sourhope (55° 29' 23.47" N, 2° 12' 43.32" W)
  - T08: Wytham (51° 46' 52.86" N, 1° 20' 9.81" W)
  - T11: Snowdon (53° 4' 28.38" N, 4° 2' 0.64" W)
  - T12: Cairngorms (57° 6' 58.84" N, 3° 49' 46.98" W)

- Variables measured (FIELDNAME) and units
  - Examples include ALKY (Alkalinity, mg/L), ALUMINIUM (mg/L), CALCIUM (mg/L), CHLORIDE (mg/L), COLOUR (absorbance at 436 nm, nM), CONDUCTIVITY (µS/cm), DOC (mg/L), IRON (mg/L), MAGNESIUM (mg/L), NH4N (mg/L), NO3N (mg/L), PH (pH), PHAQCS/PHAQCU (pH measures), PO4P (mg/L), POTASSIUM (mg/L), SODIUM (mg/L), STAGE (mm), TOTALN (mg/L), TOTALP (mg/L), among others

- Quality codes and interpretation
  - Quality Codes cover data loss, sampling issues, lab issues, and unusual events
  - Examples include: 100 No information available; 101 No sample taken; 105 Snow in funnel; 200 Adverse weather; 501 Laboratory: No sample; 506 Equipment failure; 999 Unusual event (see associated quality text)
  - A full list of codes and meanings is provided to interpret data quality

- Usage notes and accessibility
  - Data are designed to be comparable across ECN sites; consult accompanying quality information to properly handle data
  - Site and variable metadata enable cross-site analyses and data unification
  - ECN provides a catalog entry for further site information and metadata: https://catalogue.ceh.ac.uk/id/813712d4-d162-4edeaff8-cf1c337bdc27

- End-to-end data lifecycle
  - Data collection, lab analysis, and QC are integrated through documented SOPs
  - Data cleaning and transformation are supported by the QC documentation
  - Datasets and metadata are intended to be discoverable and usable, with explicit data source tracking and usage guidelines

- Access considerations for analysts
  - Expect multiple linked files (core data, lab details, QC data, and quality codes)
  - Carefully incorporate quality flags and notes when performing analyses
  - Use site codes and coordinates to align with site-level context and boundaries
  - Where needed, refer to the accompanying PDFs/CSV documentation for detailed interpretation of fields and codes