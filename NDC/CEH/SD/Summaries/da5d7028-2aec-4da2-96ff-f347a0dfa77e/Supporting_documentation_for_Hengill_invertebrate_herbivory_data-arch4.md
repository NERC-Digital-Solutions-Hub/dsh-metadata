# Invertebrate herbivory data across a natural soil temperature gradient in Iceland from May-July 2017

## Overview
- Dataset from 14 experimental plots in the Hengill geothermal valley, Iceland, collected May–July 2017.
- Plots span a natural soil-temperature gradient (average 5–35 °C) within 1 km2; plots share similar soil moisture, pH, nitrate, ammonium, and phosphate.
- Focus on environmental data, vegetation cover, and invertebrate herbivory at community- and species-level for three plant species: Cardamine pratensis, Cerastium fontanum, and Viola palustris.
- Data link to broader warming-context research (soil temperature effects on plant and invertebrate communities; related publications cited).

## Sampling regime and collection methods
- Plot design: fourteen plots (66–210 m2) established to cover the full soil-temperature gradient; within-plot temperature variation aimed where possible.
- Species-level sampling: 30 individuals per focal species per ten plots, selected by stratified random sampling to cover the temperature range.
- Community-level sampling: five 50 × 50 cm quadrats per plot in eight plots chosen to capture the gradient.
- Measurements:
  - Soil temperature: recorded at 12 cm depth at five points per community quadrat and near each marked individual.
  - Soil moisture: percentage moisture in each community quadrat (ML3 ThetaProbe).
  - Soil chemistry: five cores per quadrat for pH and nutrients; nitrate and ammonium extracted with 2M KCl; phosphate extracted with ammonium lactate–acetic acid buffer; nutrient concentrations measured colorimetrically with specified detection limits.
  - Vegetation phenology: weekly assessment of marked individuals using a 10-stage scale.
  - Vegetation cover: visually estimated by functional groups (bryophytes, forbs, graminoids, lichens, litter, bare ground) within quadrats.
  - Herbivory (leaf damage): standing damage assessed per time-point; species-level surveys every two weeks from 30 May to 2 July (three time-points per species), community-level herbivory assessed on 19 June.
- Damage coding:
  - Species-level: damaged vs. not damaged; additional metrics include length, stems, leaves, leaves damaged, percent leaves damaged, overall percentage of photosynthetic tissue damaged, flowering status, and number of flowers.
  - Community-level: proportion of damaged plants within a 100-individual sample per quadrat; only healthy, fully expanded leaves used for damage assessment; leaf loss counted as damage only if petiole remained with bite marks.
- Timeframe and repetition: multiple time-points across May–July 2017 with emphasis on capturing seasonal phenology and herbivory dynamics; data structure explicitly records time, date, and plot for each observation.

## Data structure and content
- Data delivered as five CSV files. Each row corresponds to a single sampling time-point for an individual plant or a community quadrat.
- Common header: first three columns in all files are time, date, and plot (plot codes explained in Warner et al. 2021).
- File-specific columns:
  - cardamine.csv and cerastium.csv:
    - ID (unique plant), temp (soil temperature in °C, 12 cm depth), phenology (10-stage scale), damage (1/0), length (cm), stems, leaves, leaves_damaged, pc_leaves_damaged, overall_damage (percentage), flowering (Y/N/B/S/W), num_flowers.
  - viola.csv:
    - same as above with pc_leaves_damaged and flowering occupying columns 9–10.
  - cover.csv:
    - ID (unique plant), species (Latin name), temp, cover of moss, lichens, graminoids, forbs, litter, bare ground (percent cover per quadrat), flowering (Y/N/B/S/W).
  - herbivory.csv:
    - herbivory (proportion of plants in quadrat with herbivory), moss/lichens/graminoids/forbs/litter/bare ground cover, temp (mean of five points within quadrat), pH, moisture, nitrate, ammonium, phosphate (mg kg-1).
- Notes:
  - Units and measurement methods align with established protocols cited in the references.
  - Plot codes and additional methodological details are described in Warner et al. (2021) and related sources.

## Data quality, metadata, and accessibility
- Methods follow standardized protocols for soil and plant measurements; explicit limits and procedures are cited (e.g., extraction methods, colorimetric analyses, and phenology staging).
- Data include explicit metadata within the file descriptions (column meanings, units, and sampling context).
- Timepoints and sampling intensity allow longitudinal analyses of warming-gradient effects on herbivory, phenology, and vegetation structure.
- Comprehensive references provide provenance, measurement standards, and methodological context (e.g., Blakemore et al. 1987; Egnér et al. 1960; Turcotte et al. 2014; Warner et al. 2021).

## Implications for data leadership and stewardship
- Rich, multi-dimensional dataset that integrates abiotic (temperature, moisture, nutrients) and biotic (plant phenology, vegetation cover, herbivory) layers along a natural gradient.
- High usefulness for cross-study synthesis, replication, and meta-analyses targeting climate warming effects on plant–herbivore interactions.
- Well-structured with clear data products and explicit documentation, supporting discoverability, reusability, and potential integration with broader data networks or partner datasets.

## Potential uses and applications
- Modelling how soil temperature and related abiotic factors influence herbivory intensity at species and community levels.
- Assessing phenological mismatches and their relation to herbivory across the temperature gradient.
- Cross-site comparisons and synthesis with other warming experiments; informing data strategy for ecological data assets with multi-scale measurements.

## References
- Blakemore, L., Searle, P. & Daly, B. (1987). Methods for chemical analysis of soils. New Zealand Soil Bureau Scientific, Report 80.
- Egnér, H., Riem, H. & Domingo, W.R. (1960). Investigation of soil test analysis for nutrient assessment.
- O'Gorman, E.J. et al. (2012). Impacts of warming on aquatic communities.
- Peet, R.K. et al. (1998). Vegetation composition and structure recording method.
- Robinson, S.I. et al. (2018). Soil temperature effects on plant and invertebrate communities.
- Turcotte, M.M. et al. (2014). Percentage leaf herbivory across vascular plant species.
- Valdés, A. et al. (2019). Phenotypic/genotypic responses of plant phenology to geothermal warming.
- Warner, E. et al. (2021). Impacts of soil temperature, phenology, and plant community composition on invertebrate herbivory.