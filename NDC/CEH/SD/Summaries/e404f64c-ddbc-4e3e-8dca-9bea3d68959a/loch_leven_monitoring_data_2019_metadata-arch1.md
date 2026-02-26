# Loch Leven long-term monitoring dataset

## Overview
- Datasets collected as part of a long-term monitoring programme of Loch Leven, a lowland lake in Scotland, UK, spanning from 1968 to the present.
- Describes data collection, sampling and analysis methods, data processing techniques, and output file format.
- Data collection and processing conducted under project UK-SCAPE WP7 LEVEN; most recently by NERC / UK Centre for Ecology & Hydrology.
- Aimed at providing a structured, metadata-rich dataset suitable for analysis of lake chemistry and crustacean zooplankton dynamics.

## Sampling regime and sites
- General cadence: fortnightly sampling.
- Sites visited per occasion: two main sites – Reed Bower (RB) and Sluices (L/Sl8; outflow). Measurements sometimes limited by resource constraints, weather, or ice cover.
- Site coding: Harbour (H), Reed Bower (RB5), Sluices / Outflow (L/Sl8); coordinates provided in UK National Grid (epsg:27700).
- Special note: when data recorded as Outlet, values are treated as Sluices in the dataset for ease of use.

## Measurements and analyses
- In situ measurements at each site: conductivity, pH, temperature; Secchi depth measured at Reed Bower.
- Water samples collected at each site for laboratory analyses:
  - Nutrients and related measures: soluble reactive phosphorus (SRP), total soluble phosphorus (TSP; filtered and frozen), total phosphorus (TP; unfiltered and frozen), soluble reactive silicate, total diatom silica.
  - Chlorophyll a: filtered from 400 mL samples and stored frozen until analysis.
- Sampling details:
  - Reed Bower: integrated sample collected with a weighted PVC tube to capture the full water column.
  - Sluices: 10 cm below surface using a bottle.
  - Duplicate 2 L samples per site; samples processed within hours to days.
- Analytical methods:
  - SRP: Murphy & Riley (1962) colorimetric method with phospho-molybdenum blue complex; absorbance at 882 nm.
  - TP: digestion with sulfuric acid and potassium persulphate; SRP-like measurement post-digestion (following Wetzel & Likens 2000 with added acidification).
  - TSP: similar to TP but using filtered samples.
- Weather data: cloud cover, wind direction, wind force recorded at Reed Bower when possible; wind force table provided (Beaufort scale with descriptive lookup).
- Additional references for methods included in the dataset documentation (Golterman et al., Murphy & Riley, Wetzel & Likens).

## Crustacean & zooplankton
- Densities of crustacean zooplankton recorded at Reed Bower and Sluices, expressed as individuals per liter (ind/L) for multiple taxa (e.g., Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus).
- Sampling methods:
  - Reed Bower: 4 m angled net haul (mesh 120 µm).
  - Sluices: filtration of ~30 L surface water through a 120 µm net.
- Preservation and lab processing:
  - Preserved in 4% formaldehyde.
  - Counting performed under a light microscope; four sub-samples counted per sample.
  - Species-level identification where possible; counts converted to ind/L using appropriate multipliers.
- Post-processing: samples reconstituted and archived after counting.

## Data processing, quality assurance, and data format
- Data processing: an import R script used to process data before database entry; specific rules include:
  - Wind force: when a range is given (e.g., 4-5), the first value is used.
  - Probe replicates (conductivity, pH, DO and corresponding temperatures): replicate values retained if within Median ± MAD; handling accommodates small replicate counts; pH values are converted to 10^pH for calculation and back-transformed for final averaging; values are rounded (pH/DO to 2 dp; conductivity and temperatures to 1 dp).
- Quality assurance: automated and manual checks performed on all data; unusual values investigated and corrected as appropriate.
- Data storage format: a single comma-separated values (CSV) file; missing values labeled NA.
- Column structure: columns describe determinand, site conditions, lake chemistry, and crustacean/zooplankton counts with units; detailed mapping provided in the dataset’s Table 3.
- Column descriptions (highlights):
  - Date, Week_of_Year
  - Weather: Cloud_cover_Eighths, Wind_Direction, Wind_Force_Beaufort_scale, etc.
  - Site-specific conditions: Depth_m (RB/L), Secchi_m (RB), Water_Level_cm (Harbour), etc.
  - Chemical determinants: Conductivity (µS/cm), Temperature (°C) for conductivity and DO, DO (mg/L, %), pH, TP (µg P/L), SRP (µg P/L), TSP (µg P/L), chla (µg/L).
  - Zooplankton: densities for each taxon (ind/L) at each site (RB/L).
- Documentation: Table 3 provides full, detailed descriptions of each column’s determinand, site, and units; Table 1 lists sampling sites; Figure 1 shows site locations.

## References and supporting materials
- Methods for chemical analyses and nutrient determinations (Golterman et al., Murphy & Riley, Wetzel & Likens).
- Additional reading: Hydrobiologia special issue on Loch Leven; Scottish Natural Heritage reports (e.g., 2008–2010 water quality monitoring).