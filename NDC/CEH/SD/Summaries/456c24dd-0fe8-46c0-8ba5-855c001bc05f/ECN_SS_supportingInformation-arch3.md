# UK Environmental Change Network (ECN) soil solution chemistry data: 1992-2012

- Purpose and context
  - ECN soil solution chemistry data are collected to understand environmental change causes and consequences.
  - Data are provided by the ECN programme, sponsored by multiple UK government departments and agencies.
  - Users are asked to acknowledge data use and to send one reprint of any publication citing the data.

- Origin and providers
  - Dataset Originator: ECN Data Centre, Centre for Ecology and Hydrology (ECN)
  - Data Providers: UK government departments/agencies including Defra, Environment Agency, Natural England, Natural Resources Wales, Scottish Environment Protection Agency, Scottish Government, and others.

- Protocol and data collection
  - Suction samplers are used to measure soil solution chemistry; sampling occurs fortnightly.
  - Replacement of suction samplers is recorded with a new replicate ID (RID).
  - If insufficient samples are collected, days may be bulked and indicated by RID XXS (shallow) or XXD (deep).
  - Quality control: a standard QC solution is analyzed alongside field samples; QC data accompany the dataset.
  - Users should consult the accompanying quality information for proper usage.

- Data structure and core variables
  - Primary data fields: SITECODE, SDATE, RID, FIELDNAME, VALUE.
  - SITECODE = ECN site identifier; SDATE = sampling/record date; RID = replicate ID; FIELDNAME = measured variable; VALUE = measured value.

- Site codes and coverage
  - 12 ECN sites (Drayton, Glensaugh, Hillsborough, Moor House Upper Teesdale, North Wyke, Rothamsted, Sourhope, Wytham, Alice Holt, Porton Down, Snowdon, Cairngorms) with precise coordinates and dataset date ranges spanning 1992–2012 (varying by site).

- Variables and field names
  - Chemical and related measurements include: alkalinity (ALKY), aluminium (ALUMINIUM), calcium (CALCIUM), chloride (CHLORIDE), colour (COLOUR), conductivity (CONDY), dissolved organic carbon (DOC), iron (IRON), magnesium (MAGNESIUM), ammonium (NH4N), nitrate-nitrogen (NO3N), pH (PH) and Aquacheck pH readings (PHAQCS, PHAQCU), phosphate (PO4P), potassium (POTASSIUM), sulphate (SO4S), sodium (SODIUM), total nitrogen (TOTALN), total phosphorus (TOTALP), vacuum (VACUUM), volume (VOLUME), and quality codes (Q1–Q5).
  - Units are specified for each variable (e.g., mg/L, pH, microSiemens/cm, etc.).

- Additional analytical information
  - Additional dataset ECN_SS2.csv provides extended metadata:
    - Fields include site code, RID, deployment/debulk dates/times, sampling times, laboratory ID, pH measurement times, filtration date, and analysis completion date.

- Quality assurance and quality codes
  - ECN site managers assign standardized quality codes to denote data factors affecting quality; codes are selectable from a predefined list, with 999 for unusual events requiring textual notes.
  - Examples of quality codes cover data loss, sampling/equipment issues, sample integrity problems, weather-related impacts, laboratory issues (e.g., partial loss, contamination, missing samples), and non-standard sampling.
  - A comprehensive list includes codes 100–223, 501–511, and 999, each with a specific description.
  - Unusual events (999) may be accompanied by explanatory text in the quality information.

- Usage notes and supporting materials
  - Supporting documentation is available for the dataset, including a DOI link to the UK Environmental Change Network soil solution chemistry data (1992-2012).
  - Researchers are advised to consult accompanying metadata and quality information when using the data to ensure appropriate interpretation and integrity.