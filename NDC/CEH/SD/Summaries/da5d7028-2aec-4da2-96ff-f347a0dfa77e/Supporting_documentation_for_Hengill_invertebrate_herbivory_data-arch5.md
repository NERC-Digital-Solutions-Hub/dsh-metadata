# Invertebrate herbivory data across a natural soil temperature gradient in Iceland from May-July 2017

## Overview and context
- Dataset of environmental data, vegetation cover, and community- and species-level invertebrate herbivory.
- Collected at 14 experimental plots along a natural soil temperature gradient (average 5–35 °C) in the Hengill geothermal valley, Iceland.
- Sampling period: May to July 2017; vegetation representative of a low Arctic community dominated by herbaceous perennials and bryophytes.
- Plant phenology, vegetation composition, and herbivory are analyzed in relation to soil temperature and plant community context.

## Study site, design, and sampling regime
- 14 plots ranging 66–210 m² within a 1 km² area; plots distributed across the temperature gradient while allowing within-plot temperature variation.
- Focal species for species-level herbivory: Cardamine pratensis, Cerastium fontanum, Viola palustris.
- Community-level herbivory assessed in eight plots using five 50 × 50 cm quadrats per plot.
- Sampling schedule:
  - Individual plants: 30 individuals per focal species per plot, with measurements every two weeks from 30 May to 2 July (three time-points per species).
  - Community-level: five quadrats per plot, with assessments on 19 June.
- Field measurements include soil temperature (12 cm depth, five points per quadrat or near individuals), soil moisture (ML3 ThetaProbe), and soil nutrient content (nitrate, ammonium, phosphate) using standard extraction methods.

## Data collected and measurements
- Phenology: weekly assessment of floral development stages (1–10, from vegetative to full flowering and wilting) for marked individuals.
- Vegetation surveys: ground-level canopy cover (bryophytes, forbs, graminoids, lichens, litter, bare ground) using predefined cover classes.
- Herbivory assessments:
  - Leaf herbivory (standing damage) at plant-level and time-points; damage recorded as present/absent on fully expanded leaves, focusing on herbivory signs (no mining/galling); damage proportion per plant and per quadrat documented.
  - Community-level herbivory: proportion of damaged plants within each quadrat.
  - Leaves damaged, percentage leaves damaged, and overall photosynthetic tissue damage recorded for species-level data.
- Additional plant metrics:
  - Plant size metrics (length of longest vegetative structure, number of stems, leaves).
  - Flowering status and number of flowers.
- Soil and nutrient measurements:
  - pH, soil moisture (%), and nutrient concentrations (nitrate, ammonium, phosphate) with specified detection limits.
  - Soil samples dried and reconstituted for pH and nutrient analyses.
- Temporal resolution:
  - Species-level data: three time-points across May–July 2017.
  - Community-level data: single assessment on 19 June 2017.

## Data structure and file descriptions
- Five comma-separated value (CSV) files:
  - cardamine.csv (Cardamine pratensis) – plant-level data including ID, temperature, phenology, damage, length, stems, leaves, leaves damaged, percentage leaves damaged, overall damage, flowering, number of flowers.
  - cerastium.csv (Cerastium fontanum) – same set of plant-level variables as cardamine.csv.
  - viola.csv (Viola palustris) – similar plant-level variables; includes leaves damaged percentage and flowering status as columns 9–10.
  - cover.csv – quadrat- and plot-level vegetation cover data, with ID, species, temperature, and percentage cover for moss, lichens, graminoids, forbs, litter, bare ground, plus flowering status.
  - herbivory.csv – community-level herbivory and associated quadrat metadata, including herbivory proportion and environmental context (moss/lichens/graminoids/forbs/litter/bare ground cover, average temperature, pH, moisture, nitrate, ammonium, phosphate).
- Common core columns across files:
  - time, date, plot.
- File-specific additional columns:
  - cardamine/cerastium: ID, temp, phenology, damage, length, stems, leaves, leaves_damaged, pc_leaves_damaged, overall_damage, flowering, num_flowers.
  - viola: same as cardamine/cerastium with adjusted column positions for leaves_damaged and flowering.
  - cover: ID, species, temp, cover metrics, flowering.
  - herbivory: herbivory, cover metrics, temp, pH, moisture, nitrate, ammonium, phosphate.

## Variable details and measurement standards
- Temperature: soil temperature measured at approximately 12 cm depth, near individuals or within quadrats.
- Phenology: 10-stage scale describing developmental progress from vegetative to flowering to wilting.
- Herbivory assessments: standing leaf damage as a binary or proportional indicator; careful exclusion of wilted leaves to avoid misattribution; damage categorized only when petiole remains with bite marks.
- Vegetation cover: visual estimation within standardized cover classes to capture community composition and functional groups.
- Nutrients and soil chemistry: standardized extraction and colorimetric methods with documented detection limits for nitrates, ammonium, and phosphate; pH and moisture measured per quadrat.

## Temporal and spatial coverage
- Temporal: May–July 2017 (with specific timepoints for species-level and community-level data as described).
- Spatial: 14 plots within Hengill geothermal valley, Iceland, covering a natural soil temperature gradient.

## Data governance, provenance, and quality considerations
- Data generated using established protocols and cited references (e.g., Blakemore et al. 1987; Egnér et al. 1960; Turcotte et al. 2014; Warner et al. 2021).
- Documentation includes explicit column definitions and the meaning of plot codes (refer to Warner et al. 2021 for plot coding).
- Data are structured to support cross-variable integration (environmental context, plant phenology, and herbivory).
- Potential quality considerations for data stewards:
  - Ensuring consistent interpretation of phenology stages across timepoints and species.
  - Verifying alignment of timepoints across species and community assessments.
  - Maintaining linkage between species- and community-level data through shared plot and time identifiers.

## Access, reuse, and sharing notes
- Data are provided as CSV files with explicit column descriptions; suitable for integration into data portals and shared repositories.
- Users should cite the study and associated references (including Warner et al. 2021 and prior methodological sources) when reusing the data.
- As a data steward, ensure ongoing availability, metadata completeness, and clarity on any data usage restrictions or embargoes (not specified in the document; confirm if applicable in repository metadata).

## References
- Blakemore, L., Searle, P. & Daly, B. (1987). Methods for chemical analysis of soils.
- Egnér, H., Riem, H. & Domingo, W.R. (1960). Investigation of soil test analysis for phosphate extraction.
- O'Gorman et al. (2012). Impacts of warming on aquatic communities (contextual methods).
- Peet, R.K., Wentworth, T.R. & White, P.S. (1998). Vegetation recording method.
- Robinson et al. (2018). Soil temperature effects on plant and invertebrate communities.
- Turcotte et al. (2014). Percentage leaf herbivory across plant species.
- Valdés, Marteinsdóttir & Ehrlén (2019). Phenotypic/genotypic responses to warming.
- Warner et al. (2021). Impacts of soil temperature, phenology, and plant community on invertebrate herbivory (Oikos).