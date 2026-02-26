# Vascular plant and bryophyte survey from a 33-year chronosequence on bare chalk, Dorset, 2019-2020

## Aim
- Investigate primary succession on bare chalk across a 33-year chronosequence for vascular plants and bryophytes at Down Farm, north Dorset.
- Leverage a unique excavation site to understand colonisation dynamics over time.

## Study site and context
- Location: Down Farm, Dorset (chalk grassland area with bare chalk surfaces).
- Background: Archaeological excavations began in 1986, creating a mosaic of bare chalk patches that have remained open with no chemical input or biomass removal.
- Scope: Part of broader work on succession and restoration, with related publications and ongoing research (Ridding et al., Hawes et al.; Green 2000).

## Survey design and methods
- Transects: 13 transects (one in each excavated block) set up in July 2019; blocks dated 1986, 2004–2008, and 2013–2018 (two blocks in 2016).
- Sampling intensity: Each transect 16 m long; 50 cm x 50 cm quadrats recorded every 1 m along the transect (total of 208 quadrats for vascular plants).
- Temporal aspect: Year of excavation (Year_exc) captured for each plot (1986–2018).
- Vascular plants: Identified to species level (except Taraxacum microspecies); sward height recorded in cm.
- Bryophytes: February 2020 sampling using 20 cm x 20 cm quadrats; species-level identification with microscopy as needed; two bryophyte plots excluded due to rubble (1986 block) or time constraints (2016 block).

## Data collected and structure
- Datasets:
  - Vascular_plant_survey_bare_chalk_Dorset.csv
  - Bryophyte_survey_bare_chalk_Dorset.csv
- Key variables for vascular plants:
  - Plot_number, Year_exc, Quadrat_number, Unique_ID (Plot_Quadrat), Survey_date
  - Sward_height (cm)
  - Species columns with percentage cover
  - Bare_chalk, Bare_soil, Bare_chalk&soil, and total bare ground metrics
- Key variables for bryophytes:
  - Plot_number, Year_exc, Quadrat_number, Unique_ID
  - Survey_date
  - Species columns with percentage cover
  - Vas_plant_cov (vascular plant cover), Bare_chalk, Bare_soil, Stones, Flint, Total_bare_grd
- Data capture: Collected by experienced field ecologists; paper forms digitised into Excel and checked for anomalies.
- Scope of detail: Species-level data where possible; some groups recorded to higher taxonomic level when necessary.

## Quality control and data processing
- Data quality: Field data collected by experienced ecologists; paper data sheets digitised and checked for anomalies.
- Verification steps: Cross-checking entries to ensure consistency; microscopy used to confirm bryophyte identifications where required.

## Data management, sharing, and accessibility
- Data handling: Structured, tabulated datasets with clear metadata (plot, year, quadrat, survey date, and species covers).
- Sharing and cataloguing: Datasets uploaded to relevant portals and integrated into data holdings; work noted for potential documentation and reuse.
- Documentation: References provided for methodological context and related studies; data structure described to facilitate reuse and interoperability.

## Limitations and challenges
- Bryophyte data gaps: Two bryophyte plots omitted (one due to rubble, another due to time constraints).
- Identification limits: Some bryophyte identifications limited to groups for small or infertile specimens.
- General data challenges anticipated in chronicling 33-year succession across multiple plots and formats.

## References
- Green, M. (2000). A Landscape Revealed: 10,000 Years on a Chalkland Farm.
- Preston, C.D., Hill, M.O., Pilkington, S., Pywell, R.J. (2009). The effect of disturbance on the bryophyte flora of Salisbury Plain. Journal of Bryology.
- Hawes, P. et al. (2020). Colonisation of exposed chalk surfaces and the restoration of chalk grassland. Conservation Land Management.
- Ridding, L.E. et al. (under review). Do functional traits influence primary succession patterns for bryophytes and vascular plants? Evidence from a 33-year chronosequence on bare chalk. Journal of Ecology.