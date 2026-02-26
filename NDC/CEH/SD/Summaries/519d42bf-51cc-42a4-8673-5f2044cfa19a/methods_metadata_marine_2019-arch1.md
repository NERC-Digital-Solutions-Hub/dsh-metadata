# Methods, metadata and summary for marine monitoring at Akrotiri and Dhekelia between April 2017 and September 2018

- Project context
  - Part of the Defra Darwin Initiative Plus Project DPLUS056: Assessment and monitoring of current and future IAS in Cyprus to establish baseline data on native and non-native marine species in the Sovereign Base Area of Akrotiri and Dhekelia.
  - Collaboration between the University of Cyprus and volunteer divers from the Western Sovereign Base Area Sub Aqua Club.

- Study area and timing
  - Location: Akrotiri and Dhekelia (Sovereign Base Areas), with a baseline survey in Dhekelia and seasonal sampling in front of the Sub-aqua club, RAF Akrotiri.
  - Timeframe: April 2017 to September 2018.

- Methods and sampling design
  - Underwater Visual Census (UVC) used to record marine species, focusing on invasive species.
  - Habitat coverage: seagrass beds and rocky habitats where possible.
  - Fish assessments:
    - Strip transects: 25 m long, 2.5 m observation on each side (total 25x5 m2) along three replicate transects within an 85 m transect layout.
    - Divers record fish species and estimated abundances along each 25 m transect.
  - Benthic (algae and invertebrates) sampling:
    - Point intercept photo transects along all three 25 m transects.
    - Along each transect, a 20x20 cm quadrat placed every 1 m; quadrats photographed with GoPro and light.
    - Species and abundances derived from photos.
  - Baseline component: additional sampling conducted in Dhekelia.

- Data and metadata products
  - Two CSV data files:
    - akrotiri_marine_2017_2019: sampling site location and fish species abundance.
    - akrotiri_marine_quadrats_2017_2018: sampling site location and benthic species abundance (percent cover).
  - Data structure (akrotiri_marine_2017_2019):
    - Date, Site_code, Site_full_name, Lat, Lon, Species, Species_common, Taxonomic_group, Abundance (ACFOR scale), Abundance_num, Method.
  - Data structure (akrotiri_marine_quadrats_2017_2018):
    - Date, Site_code, Site_full_name, Lat, Lon, Species, Taxonomic_group, Species_Cov_% (percent cover), Method.
  - Metadata notes:
    - Data describe sampling sites, coordinates, taxonomic details, abundance measures, and recording method (diving or snorkeling).
    - Abundance recorded on ACFOR scale for fish and detailed presence/abundance for benthic components.
  
- Data quality and governance
  - Quality control/assurance performed by UCY staff: equipment and protocols developed by experienced UCY personnel.
  - Incoming data reviewed and digitised by UCY staff; data quality checks ensured before inclusion in outputs.
  - Documentation links data collection methods to the volunteer team and ensures traceability of sampling events and observer method.

- Practical implications for analysts
  - Provides baseline, spatially explicit data on native and non-native marine species in Akrotiri and Dhekelia to inform IAS assessments and future monitoring.
  - Enables cross-dataset analyses between fish assemblages and benthic community structure using standardized transects and sampling schedules.
  - Metadata and data quality practices support reproducibility, data sharing, and potential integration with other datasets or portals.