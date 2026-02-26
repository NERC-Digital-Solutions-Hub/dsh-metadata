# Rationale Contamination of waterbodies with FIOs from diffuse and point sources is of significant concern to human health, as well as waterbody quality and ecology, due to the potential for exposure to a large audience of formal and informal recreational users, and for overlap with a range of other stressors.

## Aim and scope
- Examine spatial distribution of fecal indicator organisms (FIOs) and their drivers in standing waters across UK Hydroscapes with contrasting landcover.
- Hydroscapes: Greater Glasgow (urban), Norfolk (agricultural), Cumbria (upland/pastoral).
- Within each Hydroscape, 18 water bodies were selected to cover gradients of size, productivity, hydrological connectivity, and ecological quality (total across three Hydroscapes: 54 water bodies).

## Study areas and temporal context
- Samples collected in three seasons: spring, summer, and autumn.
- Time frame: data collection occurred in 2016 or 2017.

## FIO sampling and analysis (methods)
- Sampling timing: all samples collected 3 hours after sunrise to standardize UAV exposure timing.
- Spatial sampling design: water samples taken from three locations per water body, separated by ~100 m.
- In-water sampling: shallow water (<0.5 m) sampled by wading; at each location three subsamples collected, separated by ~5 m, yielding nine unique samples per water body per visit.
- Total samples: 1,278 unique samples collected across the study.
- Water sampling for E. coli:
  - Collected ~30 cm below surface using sterile 180 mL bottles.
  - Samples stored at 4°C and processed within 6 hours of collection.
  - Filtration: three volumes (100 mL, 10 mL, 1 mL) filtered through 0.45-µm membranes.
  - Culturing: filters placed on MLGA agar; incubated at 37°C; colonies counted after 24 hours.
  - Units: colony forming units (CFU) per 100 mL.
- Additional measures: total heterotrophs (Hetero) CFU per 100 mL also quantified.

## Appendices and data structure
- Appendix lists field name descriptions for Disease_distribution_data_UK_standing_waters.csv:
  - Hydroscape: landscape category (Greater Glasgow, Cumbria, Norfolk)
  - season: spring, summer, autumn
  - site: focal water body name
  - sample: code of spatially discrete sample per water body (1–3)
  - rep: sub-sample designation (a–c)
  - Ecoli: E. coli concentration (CFU per 100 mL)
  - Hetero: heterotrophs concentration (CFU per 100 mL)

## Data governance and stewardship considerations for Data Stewards
- Data quality and standards:
  - Standardized sampling timing relative to sunrise and UAV exposure.
  - Consistent spatial and subsampling scheme (9 samples per water body per visit).
  - Clear laboratory workflow (filtration volumes, culture conditions, incubation, and reporting units).
- Metadata and documentation:
  - Well-defined field descriptors (Hydroscape, season, site, sample, rep) ensure traceability and reuse.
  - Appendix provides explicit definitions to support interoperability and discovery.
- Data storage, sharing, and updates:
  - Dataset comprises CFU counts per 100 mL for E. coli and heterotrophs; should be stored with associated metadata and accessible via relevant portals/catalogues.
  - Temporal scope (2016/2017) and geographic scope (three Hydroscapes) should be clearly noted to inform reuse and potential updates.
- User needs and usability:
  - Data capture enables analysis of spatial distribution and drivers of FIOs, supporting health risk assessment and ecological quality evaluations.
  - Documentation supports reproducibility and potential integration with other datasets (e.g., UAV-derived metrics or landcover data).
- Potential challenges and considerations:
  - Multi-year and multi-season design may require harmonization if integrating with datasets of different timeframes.
  - Ensuring consistent data format and units (CFU per 100 mL) across all samples and future updates.

## Summary takeaway for data users
- The dataset provides a robust, standardized set of E. coli (and heterotrophs) counts across 54 UK water bodies, collected in three seasons, with a clear sampling framework and metadata descriptors to support spatial analysis of FIO distribution and drivers, suitable for informing public health and ecological assessments.