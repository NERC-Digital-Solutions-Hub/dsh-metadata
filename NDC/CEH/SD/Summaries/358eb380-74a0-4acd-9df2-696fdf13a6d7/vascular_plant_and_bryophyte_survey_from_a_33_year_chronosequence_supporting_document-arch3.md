# Vascular plant and bryophyte survey from a 33-year chronosequence on bare chalk, Dorset, 2019-2020

- Purpose and scope
  - Investigates primary succession on bare chalk using a 33-year chronosequence across two taxa: vascular plants and bryophytes.
  - Enabled by an excavation site at Down Farm, Dorset, with a history of archaeological diggings and subsequent open, unmanaged bare chalk surfaces.

- Study site and chronology
  - Location: Down Farm, north Dorset.
  - Excavation timeline: 1986; 2004–2008; 2013–2018 (with two blocks excavated in 2016), creating a mosaic of bare chalk surfaces.
  - Conditions: No chemical inputs or biomass removal; surfaces remained open for study.

- Survey design and field methods
  - 13 transects across excavated blocks, each 16 m long; one transect per age category (1986, 2004–2008, 2013–2018; two blocks in 2016).
  - Vascular plants: 50 cm x 50 cm quadrats, surveyed every 1 m along each transect (208 quadrats total); species identified to fine taxonomic resolution (Taraxacum microspecies exceptions).
  - Bryophytes: February 2020 survey using 20 cm x 20 cm quadrats; two plots not recorded (excavated 2006 had rubble; 2016 time constraints).
  - Data collection quality: Conducted by experienced field ecologists; paper forms digitised into Excel; data checked for anomalies.

- Data management and structure
  - Data files:
    - Vascular plants: Vascular_plant_survey_bare_chalk_Dorset.csv
    - Bryophytes: Bryophyte_survey_bare_chalk_Dorset.csv
  - Structure and key fields (examples):
    - Plot_number (1–13), Year_exc (1986–2018), Quadrat_number (0–15), Unique_ID (Plot_Quadrat), Survey_date (dd.mm.yy)
    - Sward_height (vascular plants), Agrostis_stolonifera - Viola_hirta (species percentage cover), Bare_chalk, Bare_soil, Bare_chalk&soil (vascular dataset)
    - Bryophyte species columns (e.g., Amblystegium_serpens, Weissia_sterilis), Quadrat-level bryophyte cover
    - Additional metrics: Stones, Flint, Total_bare_grd (combined bare ground components)
  - Metadata and data governance considerations noted (openness, data sharing potential, and the need for clear provenance).

- Quality control and data limitations
  - Strengths: Data collected by skilled ecologists; systematic sampling across a long time span; explicit quadrat-level structure enabling trend analysis.
  - Limitations: Two bryophyte plots not recorded; some bryophyte identifications limited to groups for small or infertile specimens; potential challenges in fully harmonizing long-term metadata across excavation ages.

- Relevance for monitoring frameworks
  - Demonstrates a robust, long-term, multi-taxa monitoring approach suitable for tracking primary succession and habitat change.
  - Uses a standardized, repeatable sampling design (transects, quadrats, species-level data) aligned with environmental health monitoring needs.
  - Provides transparent data structure and documentation (CSV formats with explicit column descriptions), supporting data verification, reuse, and governance.
  - Highlights practical challenges common in monitoring (data gaps, metadata quality, access to datasets, and open-data considerations), illustrating how to address them in framework development.

- References
  - Green, M. (2000). A Landscape Revealed: 10,000 Years on a Chalkland Farm. Tempus Publishing Ltd.
  - Preston, C.D., Hill, M.O., Pilkington, S., Pywell, R.J. (2009). The effect of disturbance on the bryophyte flora of Salisbury Plain. Journal of Bryology, 31, 255-266.
  - Ridding, L.E., Hawes, P., Walls, R., Pilkington, S.L., Bailey, J., Pywell, R.F., Pescott, O.L. (under review). Do functional traits influence primary succession patterns for bryophytes and vascular plants? Evidence from a 33-year chronosequence on bare chalk. Journal of Ecology.