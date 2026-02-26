# Peaknaze Moor field site Supporting documentation for data

- The Peaknaze Moor project is a manipulation experiment to evaluate how upland moorland ecosystems recover from reduced nitrogen deposition and interact with climate change.
- Location: Peak District, England; 53.47 N, 1.91 W; elevation 433 m; 208.45 hectares; typical Eriophorum vaginatum blanket mire with Calluna vulgaris-Cladonia sub-community; dominated by Deschampsia flexuosa, Eriophorum vaginatum, Eriophorum angustifolium, Vaccinium myrtillus, and Calluna vulgaris.
- Timeline: Site established in 2006; automated retractable roof system powered by solar/wind; data collection through multiple years (2006–2012 for major datasets, with later extreme-event observations).

- Data structure and layout
  - Area/site history: 75% of moor burnt in April 2003; grazing removed in 2004; fenced off and allowed to recover.
  - Plot design: 15 plots established in 2006; each plot 5 m × 4 m with a 3 m × 3 m experimental area; 0.5 m × 0.5 m quadrats designated for measurements.
  - Plot organization: 3 blocks, each containing four treatments and an untreated Control; 12 treatments total across blocks; Drought and Warming started in 2010; Pristine and Optimum Moisture started in 2012.
  - Measurements and data layers mentioned: meteorological data, soils characteristics, plant biodiversity, soil respiration, net ecosystem exchange, lysimeters, leaf litter, and other ecosystem process measurements.

- Climate change and pollution treatments
  - Drought: retractable roofs exclude rainfall to simulate drought; rain removal without rainfall replacement.
  - Warming: night-time reflective covers reduce infrared heat loss.
  - Pristine: rainfall is modified to simulate polluted rain using collected rainfall data to determine the amount of polluted rain applied.
  - Optimum Moisture: constant soil moisture achieved via feedback-controlled irrigation from on-site storage.

- Biodiversity treatments and data collection
  - Plant surveys (2005 pre-treatment) used non-destructive pin-point methods across three quadrats per plot (3 × 300 pins per plot) to quantify species hits and vegetation structure.
  - Species tracked include Nardus stricta, Deschampsia flexuosa, Eriophorum angistifolium, Eriophorum vaginatum, Vaccinium myrtillus, Calluna vulgaris, Empetrum nigrum, and Juncus (data codes provided and cross-checked for accuracy).
  - Data quality: transcription double-checked; missing pins adjusted to maintain a total of 300 pins per plot.

  - Nested biodiversity treatments (from December 2011)
    - Moss Removal: all moss removed from designated subplots; moss biomass separated from debris and weighed; samples processed to determine moss proportion.
    - Cover Removal: vegetation clipped to bare soil within randomly placed squares; clipped biomass dried for analysis.
    - Biomass measurements documented to establish initial establishment weights for moss and cover removals (noted as total moss biomass and total cover biomass per plot across establishment year).

- Extreme events and data
  - Vapourer (Orgyia antiqua) outbreak and fungal infections monitored in February 2010, with defoliation percentages recorded by quadrat and treatment.
  - Outbreak primarily affected Vaccinium myrtillus; defoliation levels varied by year and treatment, with some quadrats showing very high defoliation (up to 100% in several cases) and others showing little to no signs of attack.
  - Fungal infections also recorded alongside caterpillar damage; signs noted across Control, Moss Removal, and Cover Removal subplots.

- Data availability and quality notes
  - Some meteorological data are not determined for certain years (e.g., 2006–2009 growing season MAT and related metrics).
  - Soil data show many placeholders and partial measurements (e.g., texture, organic horizon data, pH values, carbon/nitrogen content, and exchangeable cations with variable completeness).
  - Overall, the documentation emphasizes data verification, cross-checking, and standardized collection methods, but several data fields are incomplete or missing for certain years.

- Metadata and provenance
  - Author: Sabine Reinsch
  - Version: 1
  - Date: 11/10/2016

- GIS-relevant implications
  - Ready-to-use spatial layers include plot footprints, block structures, and treatment assignments suitable for map-based visualization of experimental design.
  - Potential layers: plot polygons, treatment type, year of treatment initiation, vegetation surveys by species, moss and biomass removal subplots, meteorological data by year, soil properties where available, and extreme-event defoliation metrics by quadrat.
  - Temporal data potential: multi-year climate manipulation (2010 onward) linked with biodiversity and soil process measurements for trend analysis.
  - Data gaps to address in GIS workflows: fill missing meteorological/soil attributes, standardize species nomenclature, and align measurement codes for cross-dataset integration.