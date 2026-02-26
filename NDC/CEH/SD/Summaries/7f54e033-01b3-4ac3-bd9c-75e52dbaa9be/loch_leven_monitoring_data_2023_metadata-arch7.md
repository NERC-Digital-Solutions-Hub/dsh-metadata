# Loch Leven long-term monitoring dataset

- A long-running data collection program from Loch Leven, Scotland (started 1968; ongoing). Includes water chemistry and crustacean zooplankton data collected as part of the UK-SCAPE WP7 LEVEN project.
- Data described include methods, data processing, and output format for the dataset.

## Spatial and temporal coverage

- Sampling cadence: generally fortnightly.
- Sites visited per sampling: two main sites – Harbour (H), Reed Bower (RB), and Sluices/Outflow (L). Reed Bower is boat-accessible; Sluices can be sampled by boat or from shore.
- Geographic reference: UK National Grid (EPSG:27700). Site coordinates (E/N) provided for Harbour, Reed Bower, and Sluices.
  - Harbour (H): Easting 312251, Northing 701670
  - Reed Bower (RB): Easting 313568, Northing 701141
  - Sluices (L): Easting 317004, Northing 699380
- Data are stored with reference dates, week of year, and site-specific measurements.

## Data collected and variables

- Water chemistry and lake conditions (site-specific; in CSV format with explicit units):
  - Conductivity (uS/cm)
  - Temperature (°C)
  - pH
  - Dissolved oxygen (DO) and DO percentage
  - Secchi depth (m) – measured at Reed Bower
  - Depth at site (not sampling depth)
  - Water level relative to harbour wall (cm) at Harbour
  - Cloud cover (eighths)
  - Wind direction (compass points) and wind force (Beaufort)
- Nutrients and pigments (laboratory analyses):
  - Total phosphorus (TP, μg P/L)
  - Soluble reactive phosphorus (SRP, μg P/L)
  - Total soluble phosphorus (TSP, μg P/L)
  - Chlorophyll a (chla, μg/L)
  - Dissolved oxygen temperature and pH-specific measurements
- Biological data (crustacean zooplankton) densities (ind/L) by taxa at each site, including:
  - Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Ceriodaphnia sp., Polyphemus pedicululus, etc.
- Data include replicate measurements (e.g., TP, SRP, TSP, chla) and converted counts to per litre for zooplankton.

## Sampling regime and site details

- Two main sampling sites each occasion; weather and resource constraints can limit sampling:
  - If boats are unsafe due to weather/ice, only Sluices may be sampled or neither site sampled.
- Sampling and sampling devices:
  - In situ measurements conducted at sites; duplicate 2 L water samples collected from each site.
  - Reed Bower: integrated water sample collected with a weighted PVC tube to sample the entire water column.
  - Sluices: bottle collected ~10 cm below the surface.
- Zooplankton sampling specifics:
  - Reed Bower: crustacean zooplankton collected with a 4 m angled net (120 μm).
  - Sluices: surface water passed through a 120 μm net (30 L volume).
  - Samples preserved in 4% formaldehyde; laboratory subsampling and identification performed to species level where possible.

## Data processing and quality assurance

- Processing workflow:
  - An R-based import script processes raw data into a database, applying sensible rules for quality control.
  - Wind force values: when a range (e.g., "4-5") is present, the first value is used.
  - Probe replicates (conductivity, pH, DO, and related temperatures) are filtered using Median Absolute Deviation (MAD) criteria. If only 1–2 replicates exist, none are removed. If 3 replicates exist and two are identical, the outlier is removed.
  - pH values are converted to 10^pH, MAD applied, then converted back; means are rounded to 2 decimal places (pH/DO) or 1 decimal place (conductivity, DO%, temperatures).
  - As of 21/12/2022, the Hach probe model changed (HQ30d to HQ4300); inter-calibration maintained; column names updated accordingly, order unchanged.
- Quality assurance:
  - Automated and manual checks on data entries and ranges; unusual values investigated and corrected as needed.

## Data format and schema

- Output format: single CSV file.
- Content: columns cover site conditions, lake chemistry, and crustacean/zooplankton counts; includes units and site references; missing values are NA.
- Column naming and structure:
  - Detailed column descriptions provided (Date, Site, Week_of_Year, site-specific measurements, and numerous determinands with site and unit suffixes).
  - 2023 updates: internal renaming for consistency (e.g., litres abbreviated as L, μ abbreviated as u, degrees as deg) and Ceriodaphnia_sp. added; new taxa appended at dataset end.
- Column reference guidance:
  - Column names encode determinand, site, and units (e.g., Conductivity_uS/cm_Hach_HQ4300_Site_RB; Depth_m_Site_RB; chla_ug/L_Site_RB).
  - Table 3 in the document provides full column descriptions and units.

## 2023 updates and notes

- Column names updated for encoding consistency (L, u, deg); Ceriodaphnia_sp. now recorded.
- Some new taxa added at the end of the dataset (e.g., Ceriodaphnia_sp. and Polyphemus pediculus).
- Order of columns remains the same; only naming and encoding changed.

## Practical GIS considerations

- Data are ideal for map-based visualization of water quality and zooplankton distributions over time.
- Use EPSG:27700 coordinates for precise site mapping; integrate with other GIS layers (e.g., land use, hydrology).
- Two main data themes suitable for GIS:
  - Spatial-temporal water chemistry and physical parameters (per site, per date).
  - Zooplankton densities by taxa (per site, per date).
- Handling of missing data:
  - Missing observations represented as NA; appropriate for time-series analyses and spatial joins where data gaps exist.
- Dataset limitations to consider in GIS workflows:
  - Fortnightly sampling may create gaps; some years may have incomplete records due to weather or access.
  - Replicate measurements and derived values (e.g., pH transformations, QA corrections) should be understood when performing automated GIS-based time-series analyses.

## References and related resources

- Measurement methods and analyses references:
  - Murphy, J. & Riley, J.P. (1962). A modified single solution method for phosphate in natural waters.
  - Wetzel, R.G. & Likens, G.E. (2000). Limnological Analyses.
  - Golterman, H.L., et al. (1978). Methods for Physical and Chemical Analysis of Fresh Waters.
- Additional readings:
  - Water quality monitoring reports and Loch Leven research compilations (e.g., Dudley et al., Spears & May; Loch Leven: 40 years of scientific research).

- The dataset is part of the Loch Leven long-term monitoring program, with data management and processing aligned to the project framework and standard limnological methods.