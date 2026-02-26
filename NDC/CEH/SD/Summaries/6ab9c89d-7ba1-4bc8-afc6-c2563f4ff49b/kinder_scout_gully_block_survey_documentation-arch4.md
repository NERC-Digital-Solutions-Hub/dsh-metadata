# Kinder Scout gully block survey 2021

- Project and data context: Protect-NFM; NERC grant NE/R004560/1; author Adam Johnston. Dataset on 492 gully blocks on Kinder Scout, an upland UK peatland, to assess long-term evolution 7–8 years after peatland restoration (2013–2014) involving stone and timber dams.
- Purpose: understand long-term hydrological and ecological changes in gully-blocked peatland features and support data-informed restoration/management decisions.

## Data collected and structure

- Location data
  - Dam centre points surveyed with differential GPS (Leica VIVA GS10); post-processed with Leica Infinity using OS RINEX reference (Buxton) for corrections.
  - 3D positional accuracy: ±0.03 m; fixed control points repeat-surveyed daily.
- Dam measurements
  - In-field measurements of dam dimensions: width, height, sediment depth behind dam, and related metrics.
  - Some records missing (marked as nd) due to data loss or inability to relocate dams during the second survey.
  - Dam type recorded as Stone or Timber.
- Geospatial attributes (derived)
  - Terrain attributes: aspect, gully_wall_slope, channel_slope, gully_width, gully_depth from a 0.25 m Digital Surface Model (DSM) derived from aerial photogrammetry (Bluesky International).
  - Upslope bare peat area and bare peat percentage prior to dam installation derived from 0.05 m RGB imagery (2011, GetMapping).
- Vegetation data (ancillary)
  - Collected at three positions around each dam: gully floor (Flr), gully walls (Wall), and dam top (Dam_top).
  - For each position: overall vegetation cover percent; presence/absence (binary) of key indicator species; separate “other” notes field for non-listed species.
  - Ancillary vegetation dataset provided separately but linked by dam_id and survey date.
- Storage and hydrology
  - Storage-related variables: dam top to sediment height, sediment depth, vertical storage capacity, percentage of storage space filled, presence of a pool behind the dam, pool depth, and whether channel flow enters the pool.
  - Calculated values include static_storage_volume (m3) and percent_storage_volume_full.
- Data availability and access
  - Two CSV files: main dam dataset (position, dimensions, and hydrological attributes) and ancillary vegetation dataset; both link by dam_id and field_survey_date.
  - Columns include: GNSS_dateTime_GMT, easting, northing, elevation, aspect, gully_wall_slope, channel_slope, gully_width, gully_depth, upslope_area, percent_bare_peat_upslope, field_survey_date, dam_type, dam_width, dam_height, dam_top_to_sediment, sediment_depth, storage_height_availability, storage_height_sediment_infilled, pool_behind_dam, pool_depth, channel_flow_into_dam_pool, static_storage_volume, percent_storage_volume_full, notes, plus vegetation-related columns per position.

## Experimental design and timeline

- Population and sampling: >3000 gullies installed in 2013–2014; 500 randomly selected for survey across the plateau.
- Relocation constraints: eight dams could not be relocated for the second survey.
- Survey window: dGPS data collection 22/09/2021–06/10/2021; field measurements 13/09/2021–13/10/2021.
- Marker placement used to aid relocation for follow-up measurements.

## Methods and quality control

- Location accuracy: 3D ± 0.03 m verified via daily repeat surveys of fixed control points.
- Field measurements: conducted with tape measure, 1 m ruler, and level for dam dimensions; some data gaps noted as nd.
- Derived attributes: terrain and bare peat metrics derived from high-resolution DSMs and historical imagery; documentation provided in column descriptions.
- Data structure: two linked CSV files (main data and ancillary vegetation) with dam_id as the key; dataset described by explicit column metadata.

## Data quality, gaps, and limitations

- Missing data: some dam attributes recorded as nd due to data loss or unsuccessful relocation.
- Relocation gaps: eight dams could not be relocated during the second survey, potentially affecting completeness.
- Temporal alignment: dGPS positions collected separately from other measurements, though daily control points mitigated positional uncertainty.

## Implications for data strategy and use

- Rich, multi-dimensional dataset suitable for longitudinal analyses of engineered peatland features, hydrology, and vegetation responses.
- Clear metadata and linking mechanism (dam_id) enable integration with ancillary vegetation data and potential cross-site comparisons.
- Suitable for informing data-informed NFM planning, peatland restoration evaluation, and governance discussions on data quality, provenance, and discoverability.

## Provenance and stewardship notes

- Project provenance: Protect-NFM; fieldwork and data collection conducted in 2021; data intended to support downstream community protection and peatland restoration evaluation.
- Access: provided as two CSV files with comprehensive column metadata; appropriate for reuse in policy, planning, and cross-team data collaborations.