# Loch Leven long-term monitoring dataset

- A long-running data collection from Loch Leven, Scotland, UK, part of the UK-SCAPE WP7 LEVEN programme, maintained since 1968 and ongoing at the time of publication.
- Contains in situ lake measurements, water chemistry analyses, and crustacean zooplankton densities, stored in a single CSV file with detailed column metadata.

## Sampling regime and site information

- Sampling frequency: generally fortnightly.
- Primary sampling sites: Reed Bower (RB) and Sluices / Outflow (L); Harbour (H) is referenced in site codes.
- Access limitations: adverse weather, ice, or resource constraints may prevent sampling; RB requires boat access, L can be sampled from shore.
- Site identifiers and coordinates:
  - Harbour (H): 312251 E, 701670 N
  - Reed Bower (RB / RB5): 313568 E, 701141 N
  - Sluices / Outflow (L / Sl8): 317004 E, 699380 N
- Sampling at each visit includes site-specific conditions and measurements; data are organized with clear site codes in the columns.

## Measurements, determinations, and analyses

- Field measurements (in situ): conductivity, pH, temperature (water temperature for conductivity measurements), and Secchi depth (measured at Reed Bower; depth to Secchi disc visibility).
- Water sampling: duplicate 2 L samples per site; RB uses a vertical integrated sample, L uses a bottle 10 cm below the surface.
- Laboratory analyses on collected samples (vs. field measurements):
  - Soluble reactive phosphorus (SRP) and total soluble phosphorus (TSP)
  - Total phosphorus (TP) and, for TP, a digestion step converts all forms to SRP
  - Silicate (soluble reactive) and total diatom silica
  - Chlorophyll a
- Analytical methods referenced include Murphy & Riley (1962) for SRP and Wetzel & Likens (2000) for TP/TSP; general methods outlined in Golterman et al. (1978).
- Weather data (when possible) includes cloud cover, wind direction, and wind force (Beaufort scale), with wind descriptions aligned to a provided lookup table.

## Crustacean and zooplankton data

- Densities of crustacean zooplankton taxa per litre (ind/L) at RB and L:
  - Includes Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopidae (total), Cyclops abyssorum, Cyclops vicinus, Cyclopodidae, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, and others.
  - Zero values indicate non-recording in the sample; NAs indicate missing values.
- 2022 update: several column name refinements and two new taxa (Ceriodaphnia sp. and Polyphemus pediculus) added; minor methodological notes:
  - RB sampling via 4 m angled net haul (120 µm mesh); L sampling via 30 L surface water filtered (120 µm).
  - Post-collection processing (preservation in formaldehyde) and laboratory counting with standard taxonomic guides.
  - Counts converted to ind/L; samples archived after counting.

## Data processing and quality assurance

- Processing performed with an R import script that:
  - Handles wind force entries like "4-5" by taking the first value.
  - Applies replicate value checks for conductivity, pH, DO, and related temperatures using Median Absolute Deviation (MAD); maintains data when replicates are sparse.
  - For pH, values are converted to 10^pH during MAD calculations, then transformed back to pH; final values are rounded (pH/DO to 2 dp, temperatures and conductivity to 1 dp).
  - Inter-calibration adjustments for the HQ4300 instrument introduction (HQ30d replaced) to maintain measurement consistency.
- Quality Assurance: automated and manual checks identify and correct out-of-range or erroneous values.

## Data format and column descriptions

- Data format: single CSV file with a comprehensive set of columns describing site conditions, lake chemistry, and crustacean/zooplankton counts.
- Missing data represented as NA.
- Core columns (examples):
  - Date, Week_of_Year
  - Water_Level_cm_Site_H
  - Cloud_cover_Eighths_Site_RB
  - Wind_Direction_Site_RB
  - Wind_Force_Beaufort_scale_Site_RB
  - Depth_m_Site_RB
  - Secchi_m_Site_RB
  - Conductivity_µS/cm_Hach_HQ4300_Site_RB
  - Temperature_°C_Hach HQ4300_(cond)_Site_RB
  - DO_mg/L_HachHQ4300_Site_RB
  - DO_%_HachHQ4300_Site_RB
  - pH_HachHQ4300_Site_RB
  - TP_ugP/l_Site_RB1, TP_ugP/l_Site_L1, TP_ugP/l_Site_L2
  - SRP_ugP/l_Site_RB1, SRP_ugP/l_Site_RB2, SRP_ugP/l_Site_L1, SRP_ugP/l_Site_L2
  - TSP_ugP/l_Site_RB1, TSP_ugP/l_Site_RB2, TSP_ugP/l_Site_L1, TSP_ugP/l_Site_L2
  - chla_ug/l_Site_RB1, chla_ug/l_Site_RB2, chla_ug/l_Site_L1, chla_ug/l_Site_L2
  - Zooplankton density columns (e.g., Daphnia_hyalina_ind/L_Site_RB, Eudiaptomus_gracilis_(adults_+_copepodites_I-V)_ind/L_Site_RB, etc.)
- Table 3 provides full detail for each column, including determinand, site, and units.
- Data are designed for easy self-service use, analysis, and potential dashboarding.

## References and further reading

- Methods and context for analyses:
  - Golterman, H.L., Clymo, R.S., Ohnstad, M.A.M. 1978. Methods for Physical and Chemical Analysis of Fresh Waters.
  - Murphy, J. & Riley, J.P. 1962. A modified single solution method for phosphate in natural waters.
  - Wetzel, R.G. & Likens, G.E. 2000. Limnological Analyses.
- Additional information:
  - Dudley et al. 2012; Spears & May (eds.) 2012. Loch Leven: 40 years of scientific research.
- Zooplankton taxonomic references for identification and methodology are cited with standard guides.