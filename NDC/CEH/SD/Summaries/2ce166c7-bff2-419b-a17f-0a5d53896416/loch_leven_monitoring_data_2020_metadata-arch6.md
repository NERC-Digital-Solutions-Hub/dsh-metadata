# Loch Leven long-term monitoring dataset

- A dataset collected as part of the Loch Leven long-term monitoring programme in Scotland, UK, beginning in 1968 and continuing at the time of documentation. It covers nature, sampling/analysis methods, data processing, and output format under project UK-SCAPE WP7 LEVEN. The data include both lake chemistry and crustacean/zooplankton observations.

## Sampling regime and sites
- Fortnightly sampling schedule with two primary sites: Reed Bower (RB) and Sluices/Outflow (L/Sl8); Reed Bower is boat-access only, Sluices can be sampled by boat or from shore.
- Sampling may be interrupted by resource limits, bad weather, or ice; when boats are unsafe, only Sluices is sampled, or neither site is sampled.
- Site codes: Harbour (H), Reed Bower (RB/RB5), Sluices Outflow (L/Sl8) with corresponding UK National Grid coordinates provided.
- Data are labeled with site-specific codes for consistency across the monitoring program.

## Measurements and analyses
- In situ measurements: conductivity, pH, temperature, and Secchi depth (Secchi depth measured at Reed Bower; others may be collected in the field or later in the lab).
- Water samples collected in duplicates (2 L per site) with site-specific collection methods:
  - Reed Bower: integrated sample collected with a weighted PVC tube to sample the full water column.
  - Sluices: bottle collected 10 cm below the surface.
- Laboratory analyses on returned samples include:
  - Soluble reactive phosphorus (SRP) and total soluble phosphorus (TSP; filtered and frozen).
  - Total phosphorus (TP; unfiltered and frozen).
  - Soluble reactive silicate and total diatom silica (storage conditions noted).
  - Chlorophyll a (via filtration and freezing).
- Weather data (cloud cover, wind direction, wind force) recorded at Reed Bower when possible, with wind force described using a detailed Beaufort-based scale.

## Data processing and quality assurance
- An R-based import script processes data before database entry, including:
  - Wind force values: when a range is given (e.g., 4-5), the first value is used.
  - Probe replicates (conductivity, pH, DO, and associated temperatures): values within Median Absolute Deviation (MAD) are kept; outliers are discarded according to MAD criteria. pH values are converted to 10^pH for MAD calculations and back to pH after averaging; outputs are rounded to 2 decimal places (pH/DO) or 1 decimal place (conductivity/temperatures).
- Quality assurance includes automated and manual checks for data entry errors or out-of-range values, with follow-up corrections as needed.

## Data format and storage
- Data stored in a single comma-separated values (CSV) file.
- Columns describe determinands, site conditions, lake chemistry, and crustacean/zooplankton counts, with units and site indicators clearly included.
- Missing data are marked as NA.
- Column naming convention encodes determinand, site, and units (e.g., Date, Week_of_Year, Cloud_cover_Eighths_Site_RB, Conductivity_µS/cm_Hach_HQ30d_Site_RB, TP_ugP/l_Site_RB1, SRP_ugP/l_Site_RB2, chla_ug/l_Site_RB1, Daphnia_hyalina_ind/L_Site_RB, etc.).

## Crustacean & Zooplankton dataset
- Contains densities (ind/L) of multiple crustacean zooplankton taxa at Reed Bower and Sluices:
  - Daphnia hyalina, Eudiaptomus gracilis (adults + copepodites I-V), Eudiaptomus nauplii, Cyclopodidae (total), Cyclops abyssorum, Cyclops vicinus, Cyclopod nauplii, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus (Reed Bower only).
- Sampling methods differ by site:
  - Reed Bower: 4 m angled net haul (120 µm mesh).
  - Sluices: 30 L of surface water passed through a 120 µm net.
- Preservation and laboratory processing:
  - Samples preserved in 4% formaldehyde; counts are converted to ind/L using subsampling and multiplication factors; identifications are performed to the extent possible given specimen condition.
- Zero values indicate non-detection within the sampling and analytical resolution; NAs indicate missing values.

## References and methods
- Core measurement methods and analysis references:
  - Murphy & Riley (1962) for SRP determination.
  - Wetzel & Likens (2000) for TP/TSP digestion and measurement.
  - Golterman et al. (1978) for general freshwater analysis methods.
- Additional reading and project reports related to Loch Leven monitoring and data interpretation are cited for broader context.