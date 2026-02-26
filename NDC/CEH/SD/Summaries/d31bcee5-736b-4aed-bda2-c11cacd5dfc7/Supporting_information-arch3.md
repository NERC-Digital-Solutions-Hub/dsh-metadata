Plants, carabid beetles and birds in native reforestation sites in Glen Affric and Glen Moriston, Scottish Highlands

## Overview and aim
- A biodiversity monitoring study assessing the value of native reforestation sites for plants, carabid beetles and birds, relative to grazed/un-grazed unforested areas and mature Caledonian pineforest.
- Context: Scottish Highlands historically forested; reforestation priority to restore priority habitats; overgrazing by deer suppresses regeneration.
- Objective for monitoring frameworks: demonstrate a multi-taxa, policy-relevant appraisal of restoration outcomes and inform future management decisions.

## Study design and setting
- Location: 14 fenced native reforestation sites in Glen Affric and Glen Moriston, established 1990–2012 by Trees for Life, Forestry Commission Scotland and the National Trust for Scotland.
- Landscape context: adjacent mature Caledonian pineforest remnants, conifer plantations, heathland, and regenerating native forest.
- Treatments and sampling design (hierarchical):
  - Treatments represented in all combinations: reforestation, unforested, mature forest; grazing status: grazed, ungrazed. Reforestation × grazed not present due to deer pressure.
  - Plot types:
    - Plants and carabids: 10 × 10 m plots.
    - Birds: 50 m radius plots, subset surveyed (10 of 14 reforestation sites).
  - Matching:
    - Reforestation ungrazed plots paired with nearest unforested grazed and nearest unforested ungrazed plots to assess effects of grazing exclusion and tree establishment.
  - Mature forest: five plots (grazed/ungrazed) at three sites, with two plots per site where possible.
  - Spatial arrangement: plots positioned to reflect best-case reforestation establishment; bird plots centered to maintain separation from plant/carabid plots.
- Temporal scope:
  - Plant and carabid data collected in summer 2018.
  - Bird data collected in summer 2019.

## Data collection methods by taxon
- Plants:
  - Survey window: 22 June – 5 July 2018.
  - Plot method: three randomly placed 1 × 1 m quadrats per plot; species identified to species level (non-vascular plants to genus/morphospecies).
  - Abundance: percent cover using the DOMIN scale; full plot-level species list generated.
- Carabid beetles:
  - Survey window: 7 June – 18 August 2018.
  - Plot method: six pitfall traps per plot, paired with plant quadrats; traps filled with propylene glycol and topped with rain guards.
  - Sampling cadence: emptied at 2-week intervals over two sampling periods; specimens identified to species; voucher specimens deposited in the Oxford University Museum of Natural History.
- Birds:
  - Surveys: two 15-minute surveys per plot; conducted 6:00–11:30 a.m. with 2-minute settling period.
  - Method: identification visually or by song/call; two surveyors per plot covering ~50% each; weather conditions recorded.
  - Limitations: at one site, first period survey data were unavailable due to logistical constraints; otherwise two surveys per plot.

## Data structure and files
- plant_carabid_plot_locations.csv
  - Plot locations for plant and carabid surveys; includes site, plot type, grazing status, year established, grid reference, and pitfall trap dates.
- bird_plot_locations.csv
  - Locations for 50 m radius bird plots; includes site, plot type, forest and grazing status, year, grid reference, and weather notes per survey.
- plants.csv
  - Plant data: site, plot, quadrat, date, species, DOMIN percent cover, seedling frequency.
- carabids.csv
  - Carabid data: site, plot, time of trap sampling, species, frequency.
- birds.csv
  - Bird data: date, site, plot, time, species, how recorded, distance from plot center.
- Appendix: Data descriptions emphasize documented fields, units, and data collection dates to support reuse and meta-compatibility.

## Data quality, provenance and governance
- Data quality and integrity:
  - Standardized field methods across plots and years; species-level identifications where feasible; voucher specimens for carabids deposited (OUMNH).
  - Cross-checking in birds: two surveyors validated final species lists to avoid double counting.
  - Comprehensive metadata for each dataset (locations, treatments, dates, plot geometry, weather notes).
- Data governance and openness:
  - Underlying data are prepared for sharing with clear documentation of structure and field definitions.
  - Data management considerations highlighted: transparency of data sources, openness, and the need for maintaining up-to-date metadata and dataset provenance.
- Data sharing context:
  - The study demonstrates how to document multi-taxa monitoring in restoration contexts, aligning with governance expectations around sharing data used to inform policy and practice.

## Challenges and considerations for monitoring frameworks
- Common issues highlighted by monitoring practitioners:
  - Data gaps and data of insufficient quality or completeness.
  - Access and timeliness of data across organizations.
  - Siloes within/between organizations hindering data integration.
  - Barriers to publicly sharing datasets (data sensitivity, governance).
  - Keeping data up to date and maintaining adequate metadata.
  - Transforming data formats for usability and ensuring consistent data governance.
- Lessons for monitoring frameworks:
  - Emphasize robust metadata, standardized protocols, and transparent data governance.
  - Use hierarchical, matched-pair designs to isolate effects of restoration actions (e.g., grazing exclusion, tree establishment).
  - Provide multi-taxa datasets with explicit data files and detailed field definitions to facilitate reuse in policy evaluation and decision-making.

## Roles of authors (Appendix 1)
- Experimental design: Emily Warner, Andy Hector, Owen Lewis, Nick Brown.
- Background information to reforestation project and fieldwork facilitation: Doug Gilbert, Alan McDonnell.
- Data collection: Emily Warner, Rowan Green, Alys Savory.