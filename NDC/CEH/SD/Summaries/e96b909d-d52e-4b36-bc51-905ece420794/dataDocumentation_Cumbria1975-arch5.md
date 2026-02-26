# Terrestrial habitat, vegetation and soil data from Cumbria, 1975 Ecological Survey of Cumbria 1975. Dataset Summary

## Overview
- A countywide ecological survey of Cumbria (England) conducted in 1975 to inform nature conservation and land-use planning.
- Covers terrestrial habitats, soils and vegetation from across Cumbria; centre of gravity in the Lake District region.
- Time period: 1975; geographic coverage: Cumbria, England.
- Data categories: Vegetation data (vascular plants, bryophytes, macro-lichens), Soil data (horizon depths, pH), Habitat data (habitat types, slope, aspect).
- Sampling: stratified design with 768 plots selected, 642 surveyed; each plot is 200 m² (0.04 ha).
- Field methods and quality control followed Bunce & Shaw (1973) standardized procedures; data collected by well-trained surveyors and supervised for quality.
- Privacy note: specific site locations are not provided to protect landowner privacy (many sites private).

## Data content and structure
- Data files (CSV) and their focus:
  - CUMBRIA_1975_VEG.csv: Vascular plants, bryophytes and macro-lichens recorded by plot; includes species codes, scientific and common names, growth forms, and cover percentages; nest-level data aggregated to whole-plot level as needed.
  - CUMBRIA_1975_SOIL.csv: Soil horizon descriptions; horizon codes and descriptive categories; field-listed groupings per horizon.
  - CUMBRIA_1975_PLOTS.csv: Plot-level physical data; includes slope, aspect, soil pH, depth/layer measurements (litter, organic/mineral layers, leached and weathered layers), and habitat-related measurements within plot and at 50 m edge.
  - CUMBRIA_1975_HABS.csv: Habitat descriptions; codes and classification for within-plot and 50 m edge habitats; supplementary subgroups.
  - CUMBRIA_1975_PHYS.csv: Physiographical features recorded within 50 m of plot edge; broad categorical descriptors of site surroundings.
- Data schema highlights:
  - VEG: STRATUM, SQUARE, PLOT, NEST, COVER, CODE, BRC_NUMBER, SCIENTIFIC_NAME, COMMON_NAME, GROWTH_FORM, FIELD_SHEET.
  - SOIL: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, FIELD_SHEET.
  - PLOTS: STRATUM, SQUARE, PLOT, DATE, SLOPE, ASPECT, PH, LITTER_FROM/TO, ORG_FROM/TO, MIXED_FROM/TO, LEACH_FROM/TO, WEATHER_FROM/TO, UNDER_DEPTH, etc.
  - HABS: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, SUBGROUP, FIELD_SHEET.
  - PHYS: STRATUM, SQUARE, PLOT, CODE, DESCRIPTION, GROUP, FIELD_SHEET.
- Species data:
  - Full list of species recorded (Appendix 1) with scientific and common names, growth forms and codes.
  - Data include presence and, where recorded, percent cover by species across plots.

## Collection, provenance and documentation
- Origin and purpose:
  - Commissioned by Cumbria County Council to fill information gaps for land-use policy and nature conservation; to map habitat extent given the large number of designated sites (SSSIs and nature reserves).
- Sampling design:
  - Stratified land classification with 16 strata derived from 1 km² data; 3 plots randomly chosen per stratum per initial squares; 642 plots surveyed (768 selected) to capture variation.
  - Plot design: nested quadrats (4 m², 25 m², 50 m², 100 m², then 200 m²) for vegetation; soil pits in plot centre; horizon pits and augers for deeper horizons; pH measurement from top 10 cm.
- Methods and standards:
  - Vegetation: nested quadrats; percent cover bands (5%, 1%, few); full vascular plants, bryophytes and macro-lichens recorded.
  - Soil: horizon depth, composition and descriptive categories; standard categories defined in field handbook.
  - Habitat: within-plot and 50 m edge habitat types; slope and aspect measured with clinometer and compass.
- Quality control:
  - Data collected by fully trained surveyors; supervisor checks; standardized methods across plots.
- Related materials:
  - Related datasets: Land Classification of Cumbria 1975 (Bunce, Smith, Hill, 2015) and works by Bunce & Shaw (1973); 1978 survey publication; field methods handbooks.

## Privacy, governance and data quality considerations
- Privacy controls:
  - Specific site locations are withheld to protect landowner privacy; most sites were in private ownership.
- Data quality and governance for Data Stewards:
  - Documentation aligns with established field methods (Bunce & Shaw 1973) and standardized QA processes.
  - Metadata includes dataset purpose, surveying team, sampling design, measurement methods, and data schemas.
  - Clear data provenance: original field sheets, field sheets cross-referenced via FIELD_SHEET, and linkage to field methods and publications.
- Licensing and sharing considerations:
  - Privacy considerations limit disclosure of precise coordinates; data can be shared with appropriate access controls and in aggregated form where needed.

## Data discovery, interoperability and maintenance
- Data organization facilitates cross-linking:
  - Data are split into coherent themes (VEG, SOIL, PLOTS, HABS, PHYS) with consistent STRATUM/SQUARE/PLOT indexing for mapping and integration.
- Interoperability:
  - Uses standardized nomenclature and field codes; species nomenclature follows authoritative references; crosswalks to field handbook enable reproducibility.
- Maintenance and updates:
  - Dataset is versioned (Dataset Summary version 1.1 in 2017); potential updates should preserve original structure while documenting changes.
- Potential uses for stewards:
  - Integrate with broader Cumbria land-classification history; support re-analyses of habitat extent, species distributions, and soil-habitat correlations.
  - Enable metadata-driven data discovery, reuse, and citation, including linking to original publications and the Full List of Species Recorded.

## Practical notes for Data Stewards
- Ensure preservation of dataset schema and field definitions when sharing or migrating data.
- Maintain privacy constraints by generalizing or omitting precise coordinates where required.
- Provide clear user guidance to interpret habitat categories and vegetation cover data, including nested quadrat methodology.
- Facilitate data citations tying VEG/SOIL/PLOTS/HABS/PHYS data to the original field handbook and Bunce & Shaw (1973) procedures.