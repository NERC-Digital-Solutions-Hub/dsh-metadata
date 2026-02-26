# Dataset Description - ECN Data Centre Macrolepidoptera Insect Survey Data

- Overview
  - Dataset originates from the ECN Data Centre (Centre for Ecology and Hydrology) and is part of the UK Environmental Change Network (ECN) effort.
  - Focuses on Macrolepidoptera (moths) collected via standard light-trap methodology, using Rothamsted Insect Survey procedures.
  - Data are collected nightly and include accompanying quality information to support data usability and comparability.

- Governance and provenance
  - Dataset Owners: UK government departments and agencies participating in environmental change research (e.g., Defra, Natural England, Environment Agency, NERC councils, Scottish/Welsh governments, etc.).
  - ECN requests acknowledgement of data use and one reprint of publications citing the data.
  - Protocols exist to ensure data comparability across sites.

- Data collection protocol
  - Standard operating procedures ensure cross-site comparability; follow Rothamsted Insect Survey methodology.
  - Data collection via light traps, with nightly recordings and site-specific open/operating periods (documented in ECN_IM2.csv).
  - Site managers assess data quality using a standardized quality coding system (ECN_IM_qtext.csv provides codes and textual notes).

- Data structure and fields
  - Data download schema uses:
    - SITECODE (unique ECN Site code)
    - LCODE (location ID within site)
    - FROMDATE / SDATE (trap/set dates and sampling dates)
    - SPERIOD_D (period over which traps were set, in days)
    - YEAR / WEEK (sampling year and week)
    - FIELDNAME / VALUE (variable measured and its value)
  - Primary variables are coded in FIELDNAME, with a long mapping to species (e.g., Q1–Q8 representing multiple species codes and common names).
  - Explanatory Information provides extensive species code mappings (e.g., thousands of entries linking numeric codes to Macrolepidoptera species and common names). Notable notes:
    - Some codes refer to species pairs that cannot be separated without dissection (e.g., Mesapamea secalis/didyma; Amphipyra berbera berbera).
    - Some species codes may also appear under alternative numbers (e.g., 3394 can appear as 2507); historical subspecies classifications have been consolidated.

- Quality control and metadata
  - ECN_IM2.csv: Documents trap period (days) for each record; mostly PERIOD = 1 (daily) but may vary.
  - ECN_IM_qtext.csv: Site-managed quality codes (Q1, Q2, etc.) and associated text explaining data quality issues; code 999 indicates an unusual event requiring textual context.
  - Quality codes cover a wide range of data quality factors (e.g., sample loss, equipment issues, environmental interferences, contamination, etc.) and laboratory handling notes (codes 501–507, 999, etc.).

- Site coverage and metadata
  - Explanatory information includes a list of site codes (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, T04 Moor House, T05 North Wyke, T06 Rothamsted, T07 Sourhope, T08 Wytham, T09 Alice Holt, T10 Porton Down, T12 Cairngorms) with precise geographic coordinates.
  - Additional site metadata and access to broader site information are available via the ECN catalog (link provided in the documentation).

- Access, usage, and attribution
  - Data are downloadable with the structured code schema described above.
  - Users should reference ECN data provenance and acknowledge the data source per ECN guidance; one reprint of publications citing the data should be sent to ECN authors.
  - Supplemental quality information should be consulted to interpret data properly (ECN_IM_qtext.csv and ECN_IM2.csv).

- Caveats and notable issues
  - Large, complex species code dictionary; exact species identification may require domain expertise.
  - Some species are represented by single codes that combine or imply subspecies distinctions; certain pairs require dissection for separation.
  - Data interpretation should account for potential quality issues flagged by site managers (quality codes and accompanying descriptions).

- Practical implications for data leadership
  - Provides a standardized, cross-site macrolepidoptera dataset suitable for environmental change analyses, long-term trend assessment, and cross-network collaboration.
  - Emphasizes the importance of data governance (provenance, attribution, and quality documentation) and clear metadata for reliable reuse.
  - Highlights potential data access and interpretation challenges due to scattered data, variable availability, and complex species coding; mitigated by using the accompanying ECN_IM2.csv and ECN_IM_qtext.csv.