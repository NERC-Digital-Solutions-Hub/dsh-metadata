# Vascular plant and bryophyte survey from a 33-year chronosequence on bare chalk, Dorset, 2019-2020

## Objective and context
- Investigates primary succession on bare chalk using a 33-year chronosequence across 13 excavated plots.
- Focuses on two taxa: vascular plants and bryophytes.
- Conducted at Down Farm, north Dorset, on a unique excavation site with open, unmanaged bare chalk surfaces since alterations begun in 1986.
- Builds on prior archaeological and ecological work to understand colonisation dynamics and succession on disturbed chalk surfaces.

## Site, chronology, and sampling design
- 13 transects set up in July 2019; one transect per excavated block representing years: 1986, 2004–2008, and 2013–2018 (two blocks excavated in 2016).
- Each transect is 16 m long.
- Vascular plants: recorded in 50 cm × 50 cm quadrats every 1 m along each transect (total of 208 quadrats).
  - Species identified to full scientific name (except Taraxacum microspecies).
- Bryophytes: recorded in February 2020 using a 20 cm × 20 cm quadrat (more appropriate for bryophytes).
  - Most bryophyte identifications to species level; a few small/infertile individuals grouped (Didymodon/Bryum).
  - Two bryophyte plots not recorded (excavated 2006 had rubble; 2016 time constraints).
- Site area: approximately 125 m² of disturbed chalk original archaeology; mosaic of bare chalk surfaces with no chemical input or biomass removal since disturbance.

## Data collection, QA, and management
- Data collected by experienced field ecologists; paper forms digitised into Excel and checked for anomalies.
- Quality control includes validation and consistency checks during digitisation.
- Data are organized for reuse and discovery with metadata, enabling cross-study comparisons.

## Data structure and file descriptions
- Vascular data: Vascular_plant_survey_bare_chalk_Dorset.csv
  - Key columns: Plot_number, Year_exc, Quadrat_number, Unique_ID (Plot_Quadrat), Survey_date, species cover columns, sward_height, Bare_chalk, Bare_soil, Bare_chalk&soil, etc.
- Bryophyte data: Bryophyte_survey_bare_chalk_Dorset.csv
  - Key columns: Plot_number, Year_exc, Quadrat_number, Unique_ID, Survey_date, bryophyte species cover columns, Vas_plant_cov, Bare_chalk, Bare_soil, Stones, Flint, Total_bare_grd, etc.
- Data describe per-quadrat percentages of vascular plant and bryophyte cover, plus habitat context (bare chalk/soil, stones, flint) and plot-level metadata.
- Each plot-quadrat combination has a Unique_ID (PlotQuadrat) for traceability.
- Temporal coverage aligns with excavation year for each plot (1986–2018).

## Variables, scale, and potential analyses
- Spatial scale: 13 plots × up to 16 quadrats per plot (0–15 quadrat numbers).
- Temporal scale: surveys linked to excavation year per plot; cross-sectional and longitudinal interpretation across the 33-year chronosequence.
- Potential analyses (analysts’ perspective):
  - Colonisation and succession trends by time since exposure using species richness and total cover for vascular plants and bryophytes.
  - Cross-taxon comparisons (vascular plants vs bryophytes) in colonisation rates and community structure.
  - Relationships between cover of bare chalk/soil and species establishment or turnover.
  - Modeling with environmental covariates (sward_height, bare ground components, substrate characteristics).
  - Integration with functional trait analyses and prior work on chalk grassland restoration and primary succession.
- Limitations and considerations:
  - Bryophyte identifications limited for some taxa to groups; some species not fully resolved.
  - Two bryophyte plots missing data, potentially biasing small-sample comparisons.
  - Some taxa (e.g., Taraxacum microspecies) identified to species level only where possible; microscopy used for confirmation as needed.
  - Data are derived from field sheets with standard QA but may require careful handling for cross-dataset comparability.

## References and provenance
- Green, M. (2000). A Landscape Revealed: 10,000 Years on a Chalkland Farm.
- Preston, C.D., Hill, M.O., Pilkington, S., Pywell, R.J. (2009). The effect of disturbance on the bryophyte flora of Salisbury Plain. Journal of Bryology.
- Ridding et al. (under review). Do functional traits influence primary succession patterns for bryophytes and vascular plants? Evidence from a 33-year chronosequence on bare chalk.
- Hawes et al. (2020). Colonisation of exposed chalk surfaces and the restoration of chalk grassland. Conservation Land Management.