# Canopy height measured by LiDAR during the 2015-16 El Niño Southern Oscillation (ENSO) event in Malaysian Borneo

- Purpose and scale
  - Uses repeat LiDAR to measure canopy height change (TCH) in human-modified tropical forests within oil palm landscapes.
  - Provides TCH change data for 36,655 30 × 30 m pixels over ~3,301 ha after filtering, enabling analysis of canopy growth, mortality, and structural dynamics.

- Study area and context
  - Sabah, Malaysian Borneo, within the Stability of Altered Forest Ecosystems (SAFE) Project.
  - Landscape comprises a mosaic of logged forests and oil palm plantations; site chosen to reflect real-world habitat conversion and fragmentation effects on biodiversity and ecosystem function.

- Data collection (LiDAR)
  - 2014 flight: NERC's Airborne Research Facility, Leica ALS50-II
    - 120 kHz, 12° field of view, ~40 cm footprint
    - ~13.2 points m^-2
  - 2016 flight: ASU Global Airborne Observatory (GAO)
    - 200 kHz, 34° field of view, ~1.8 m footprint
    - ~4.1 points m^-2
  - Objective: obtain consistent canopy height metrics across time despite differing sensor specifications.

- Data processing and harmonisation
  - Created a common Digital Terrain Model (DTM) at 1 m resolution using ground returns from both surveys.
  - Generated per-survey canopy height model (CHM) and derived top-of-canopy height above ground (TCH); computed TCH_change = TCH_2016 − TCH_2014.
  - Resampled the TCH_change to 30 m resolution to reduce artefacts from repeat LiDAR data (wind, within-canopy variation).
  - Area selection and cleaning
    - Excluded 9,587 ha of oil palm plantations and 2,500 ha of salvage-logged forest (clear-cut) between surveys.
    - Excluded areas within 200 m of clear-cuts and roads (30 m buffers) to avoid land-use artefacts.
    - Removed pixels with low LiDAR point density (<10 points m^-2 in the NERC data) due to height bias.
    - Trimmed lower and upper 1% of TCH_change values to remove outliers.
  - Final analysis area: 3,301 ha, 36,655 pixels; TCH_2014 ranged from 0 to 64 m.

- Topography and distance metrics
  - Topographic Position Index (TPI) computed from the DTM to capture landscape position (range roughly -24 to 35.1).
  - Distance to oil palm edge (Dist_OP) calculated from Pléiades imagery (June 2016) and 2 m resampling; Dist_OP ranges 0 to 4,200 m (mean ~1,825 m).
  - Pixel-level coordinates (coords.x, coords.y) provided for geolocation.

- Data product and structure
  - RepeatLiDAR_SAFE_Project.csv contains 7 columns:
    - TCH_2014: Top-of-canopy height in 2014 (m)
    - TCH_2016: Top-of-canopy height in 2016 (m)
    - TCH_Change: Change in TCH = TCH_2016 − TCH_2014 (m)
    - coords.x: Longitude of the pixel center (UTM)
    - coords.y: Latitude of the pixel center (UTM)
    - TPI: Topographic position index
    - dist_OP: Distance to nearest oil palm plantation edge (m)

- Relevance for analysis and modeling
  - Enables analysis of how canopy structure responds to ENSO-related drought, logging history, and spatial context (edge proximity, topography).
  - Facilitates correlations between canopy growth/change and microclimate proxies, terrain, and distance to oil palm edges.
  - Supports predictive modeling of canopy turnover and structural change in fragmented, human-modified tropical landscapes.

- Limitations and considerations for analysts
  - Differences in LiDAR sensor density and resolution between 2014 and 2016 necessitated careful harmonisation (DTM alignment, CHM extraction, and resampling).
  - Filtering steps remove large swaths of oil palm and salvage-logged areas, focusing analysis on regenerating forest pixels within a mosaic.
  - Point-density bias identified in the NERC dataset led to exclusion of ~62% of pixels with density <10 points m^-2; GAO data did not show this bias.
  - Residual artefacts and outliers may remain despite trimming; 30 m resolution mitigates some within-canopy variability.

- References and context
  - Supporting methodology and context include multiple studies on LiDAR data fusion, canopy height modelling, and tropical forest fragmentation, particularly in Borneo (Asner et al., Jucker et al., Ewers et al., Gaveau et al., and others).