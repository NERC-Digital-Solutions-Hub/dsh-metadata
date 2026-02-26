# Details of Cleaned UK Rainfall Chemistry Data (1986 - 2011)

- Source and scope
  - Based on UK-AIR rainfall chemistry database for Defra.
  - Subset of 20 sites with the longest continuous data records from 1986 to 2011.
  - Rainfall samples collected weekly or biweekly from bulk collectors across the UK; analysed centrally.

- Data quality issues and cleaning
  - Raw data may be contaminated by bird droppings or wind-blown dust; some samples missing for other reasons.
  - Quality checks:
    - Ion balance: acceptable ranges -10% to +20% (adjusted to -10% to +30% when total ion concentration < 200 µeq/L).
    - Contamination rules: remove samples with phosphate > 10 µeq/L; examine NH4 > 100 µeq/L; remove samples with Ca > 50 µeq/L when Ca > Na (dust contamination). This is conservative; some dust-contaminated samples may remain, especially if sample volume was very low.
  - After cleaning, missing data are estimated using GENSTAT MULTMISSING across time and space.
  - Final datasets include accepted and estimated values with appropriate data flags.

- Data content and structure
  - Datasets are named per site, matching UK-AIR identifiers, with corresponding data files (e.g., AlltaMharcaidh.csv, Bannisdale.csv, etc.).
  - Each sample row includes:
    1) sample start date
    2) sample end date
    3) Ca2+ (µeq/L)
    4) Cl− (µeq/L)
    5) H+ (µeq/L)
    6) K+ (µeq/L)
    7) Mg2+ (µeq/L)
    8) NH4+ (µeq/L)
    9) NO3− (µeq/L)
    10) Na+ (µeq/L)
    11) PO4 3− (µeq/L)
    12) SO4 2− (µeq/L)
    13) non-sea SO4 2− (µeq/L; calculated from Na+ using average sea-salt composition)
    14) conductance (µS/cm)
    15) precipitation depth (mm)
    16) flag (0 = no sample; 1 = contaminated and omitted; 2 = sample volume but not analysed; 3 = missing data replaced by estimates; 4 = contaminated data replaced by estimates; -1 = raw data OK)
  - Units: ions and conductance in µeq/L and µS/cm; precipitation in mm.
  - Data can be converted to deposition by multiplying concentration by rainfall depth (mm) to obtain deposition in µeq/m².
  - Converting deposition to mass requires multiplying equivalents by the appropriate mass per equivalent (e.g., 16 for sulfur).
  - NA denotes “no analysis” for chemical species or conductance; no value in precipitation_depth indicates no sample; NA in precipitation_depth indicates a sample where rain volume was not recorded.

- Data use and interpretation
  - The dataset provides standardized, quality-assured rainfall chemistry data suitable for long-term environmental monitoring and policy performance assessment.
  - Outputs can be used to generate deposition estimates, trend analyses, and spatial representations (maps, charts).

- Site list (20 UK sites)
  - Allt a’Mharcaidh; Bannisdale; Barcombe Mills; Bottesford; Eskdalemuir; Flatford Mill; Goonhilly; High Muffles; Hillsborough; Loch Dee; Lough Navar; Preston Montfort; Pumlumon; Stoke Ferry; Strathvaich; Thorganby; Tycanol Wood; Wardlow Hay Cop; Whiteadder; Yarner Wood
  - For each site: latitude, longitude, UK-AIR id, data file name (e.g., AlltaMharcaidh.csv, Bannisdale.csv, etc.)

- Access and repository context
  - Data are stored within the UK-AIR database on behalf of Defra.
  - Cleaned and flagged data are prepared for sharing through appropriate portals; underlying data are preserved for reuse and cross-dataset analyses.

- Relevance to monitoring and data sharing (analytical perspective)
  - Emphasizes quality assurance, transparent contamination handling, and documentation of data flags.
  - Demonstrates a workflow for extending data utility by estimating missing values and preparing deposition-compatible outputs.
  - Aligns with the goal of enabling access to underlying data and promoting standardized, comparable environmental indicators over time.