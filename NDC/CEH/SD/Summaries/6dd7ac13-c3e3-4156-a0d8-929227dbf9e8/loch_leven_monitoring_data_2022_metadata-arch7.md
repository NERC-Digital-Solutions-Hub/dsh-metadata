# Loch Leven long-term monitoring programme dataset

## Overview
- Dataset from Loch Leven long-term monitoring (started 1968; ongoing at time of writing) for lake water quality and biota.
- Collected under UK-SCAPE WP7 LEVEN; analyses performed by Natural Environment Research Council and UK Centre for Ecology & Hydrology.
- Output delivered as a single CSV file with comprehensive metadata on sites, measurements, and taxa.
- GIS-relevant details include precise site coordinates (UK National Grid, epsg:27700) and a map showing sampling locations.
- Data types cover lake chemistry (conductivity, pH, temperature, Secchi depth, nutrients), weather context, and crustacean zooplankton densities.

## Sampling regime
- Fortnightly sampling cadence.
- Two main sites visited per sampling: Reed Bower (RB) and Sluices/Outflow (L).
- Reed Bower is boat-accessible; Sluices can be sampled by boat or shore/outlet.
- Occasionally sampling is skipped due to resource limits, bad weather, or ice.
- In-field measurements or laboratory analyses follow field collection.

## Sampling sites and locations
- Harbour (H), Reed Bower (RB5), Sluices / Outflow (L / Sl8).
- Coordinates (UK National Grid, epsg:27700):
  - Harbour: Easting 312251, Northing 701670
  - Reed Bower: Easting 313568, Northing 701141
  - Sluices / Outflow: Easting 317004, Northing 699380
- Sites are referenced by codes used across Loch Leven’s long-term monitoring.

## Measurements and analysis methods
- In situ measurements: conductivity, pH, temperature (using hand-held probes) at each sampled site; Secchi depth measured at Reed Bower.
- Water sampling: two duplicate 2 L samples per site.
  - Reed Bower: integrated sample using a weighted PVC tube to sample the entire water column.
  - Sluices: bottle sampling 10 cm below surface.
- Laboratory analyses (filtered and unfiltered subsets as appropriate) for:
  - Soluble reactive phosphorus (SRP) and total soluble phosphorus (TSP)
  - Total phosphorus (TP)
  - Soluble reactive silicate and total diatom silica
  - Chlorophyll a
- Analytical methods and references (Murphy & Riley 1962; Wetzel & Likens 2000; standard filtration with Whatman GF/C).
- Weather observations (cloud cover, wind direction, wind force) at Reed Bower when possible; wind described using Beaufort scale with a lookup table.

## Crustacean & Zooplankton data
- Densities (ind/L) for multiple crustacean zooplankton taxa from Reed Bower and Sluices:
  - Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopidae, Cyclops abyssorum, Cyclops vicinus, Cyclopodidae, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, and others added in 2022.
- Methodology:
  - Reed Bower: 4 m net haul, 120 µm mesh; Sluices: 30 L of surface water through 120 µm net.
  - Preservation in 4% formaldehyde; laboratory subsampling (four subsamples per sample) and microscopic identification/counting.
  - Counts converted to individuals per litre; preserved samples archived.
- Data notes:
  - Zeros indicate non-detection at sampling resolution; NAs indicate missing values.
  - Taxa names updated in 2022; two new taxa added (Ceriodaphnia sp. and Polyphemus pediculus).

## Data processing
- Data processed with an R import script prior to database entry.
- Handling rules:
  - Wind force: for ranges like 4-5, the first value used.
  - Probe replicates (conductivity, pH, DO, and related temperatures): values outside Median ± MAD are discarded; if only 1–2 replicates exist, none are discarded; median-based filtering applied with calibration for pH (log transformations as needed).
  - HQ30d replaced by HQ4300 (inter-calibration performed; column names updated accordingly; column order unchanged).
- Quality checks:
  - Automated and manual QA to flag entry errors or out-of-range values; unusual values investigated and corrected where appropriate.

## Format of stored data
- Single CSV file containing all measurements and counts.
- Columns describe determinands, sites, conditions, lake chemistry, and crustacean/zooplankton counts; units are specified where relevant.
- Missing data are marked as NA.

## Column descriptions and structure
- Column naming scheme includes: Date, Site, Week_of_Year, water-level, cloud cover, wind direction, wind force, depth, Secchi depth, conductivity, temperature, dissolved oxygen (DO), pH, phosphorus forms (TP, SRP, TSP), chlorophyll a, zooplankton taxa densities, and related metadata.
- Example groupings:
  - Temporal: Date, Week_of_Year
  - Site and conditions: Water_Level_cm_Site_H, Cloud_cover_Eighths_Site_RB, Wind_Direction_Site_RB, Wind_Force_Beaufort_scale_Site_RB
  - Lake chemistry: Depth_m_Site_RB, Secchi_m_Site_RB, Conductivity_µS/cm_HQ4300_Site_RB, Temperature_°C_HQ4300_(cond)_Site_RB, DO_mg/L_HQ4300_Site_RB, DO_%_HQ4300_Site_RB, pH_HQ4300_Site_RB, etc.
  - Nutrients and productivity: TP_ugP/l_Site_RB1, SRP_ugP/l_Site_RB1, TSP_ugP/l_Site_RB1, chla_ug/l_Site_RB1
  - Zooplankton: taxa-specific ind/L entries (e.g., Daphnia_hyalina_ind/L_Site_RB, Cyclops_vicinus_ind/L_Site_RB)
- A detailed mapping of each column, its determinand, site, and unit is provided in Table 3 of the original document.

## References and further reading
- Methods and foundational references:
  - Golterman, H.L., Clymo, R.S., Ohnstad, M.A.M. (1978). Methods for Physical and Chemical Analysis of Fresh Waters.
  - Murphy, J. & Riley, J.P. (1962). A modified single solution method for phosphate determination.
  - Wetzel, R.G. & Likens, G.E. (2000). Inorganic nutrients: nitrogen, phosphorus and other nutrients. Limnological Analyses.
- Additional information:
  - Dudley et al. (2012). Water quality monitoring at Loch Leven 2008-2010.
  - Spears & May (eds.) (2012). Loch Leven: 40 years of scientific research. Developments in Hydrobiology.
- Zooplankton taxonomy references:
  - Dussart & Defaye (1995); Einsle (1996); Flößner & Kraus (1986); Harding & Smith (1974); Scourfield & Harding (1966).