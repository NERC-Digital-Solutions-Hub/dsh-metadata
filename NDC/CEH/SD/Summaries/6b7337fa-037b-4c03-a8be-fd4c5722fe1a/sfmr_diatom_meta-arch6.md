# Diatom data from the South Fork McKenzie River in Oregon, USA.

- Purpose and scope
  - Monitor diatom response to wildfire in restored vs unrestored sites on the South Fork McKenzie River.
  - Post-fire data collection occurring after the Holiday Farm Fire (Sept 2020).
  - Sampling across 23 sites (10 sites in Feb 2022; 13 sites in Sept 2021) spanning restored and unrestored transects.

- Datasets and structure
  - Two CSV files:
    - SFMR_Diatom_Data: main dataset with site-level and per-sample measurements.
    - A separate file describing key column names for the main data file and a genus-level counts file with site characteristics for each site.
  - SFMR_Diatom_Data includes columns such as:
    - Status (restored or unrestored), date.coll, year, habitat (e.g., pool, riffle, off-channel), Season, transect, site.id
    - AI (autotrophic index), mean.depth (cm), mean.velocity (m/s)
    - rock1.area.cm2, rock2.area.cm2, rock3.area.cm2
    - Genus-level diatom counts: Tabellaria, Epithemia, Fragilaria, Hannaea, Melosira, Nitzschia, Cocconeis, Gomphonema, Diatoma, Navicula, Achnanthes, Reimeria, Cyclotella, Cymbella, Frustulia, Synedra, Rhopalodia, Eunotia, Pinnularia, Rhizosphenia, Amphora, Caloneis, Surirella, Asterionella
    - Additional fields: leftLon/leftLat/rightLon/rightLat coordinates for transects
  - Diatoms identified to genus level; sample unit is the transect (three rocks per transect composited for analysis).

- Sampling and collection details
  - Periphyton sampling from riffles and pools using standardized methods:
    - Scrub periphyton from five cobbles per location with a toothbrush, rinse, and composite into a single sample; split into three subsamples.
    - One subsample preserved in 37% formalin for diatom composition; two subsamples analyzed for chlorophyll a (Chl a) and ash-free dry mass (AFDM).
  - Diatoms counted to at least 500 valves per sample; genus-level identification.
  - Autotrophic index (AI) defined as the ratio of organic mass per cm2 in periphyton to Chl a per cm2 in periphyton.
  - Chl a per unit organic biomass estimated as % Chl a in periphyton AFDM.

- Measurements and site data
  - Variables include AI, mean.depth, mean.velocity, rock1/rock2/rock3.area.cm2
  - Transect metadata and geographic coordinates (left/right river bank) for each transect
  - Habitat type, sampling season, and date of collection

- Data provenance and quality control
  - Collected and counted following standard laboratory procedures (referenced methods).
  - Minimum robustness criterion: at least 500 diatom valves counted per sample.

- Notable methodological references
  - Baird, Eaton & Rice (2017): Standard methods for the examination of water and wastewater (23rd ed.)
  - Kelly et al. (1998): Recommendations for routine sampling of diatoms for water quality assessments

- Potential uses and relevance for data support
  - Compare diatom community composition and AI across restored vs unrestored sites post-fire.
  - Link diatom genus abundances with site characteristics (habitat, depth, velocity, rock area) and temporal context (date, season).
  - Integrate with other site data to create dashboards or reports enabling self-serve exploration of wildfire impact on periphyton communities.