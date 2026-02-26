# The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport

## Overview
- A dataset detailing moths captured at paired lit and unlit sites near Wallingford, Oxfordshire, UK, and pollen collected from their proboscides.
- Sampling occurred at 20 site pairs within 40 km of Wallingford from May to September 2014 using night-time transects, light-trapping, and overhead flight-activity surveys.
- The dataset was originally collected to assess the effects of street lighting on moths and nocturnal pollen transport; associated publication in Global Change Biology (in press).
- The data are organized into four spreadsheets and include both field observations and pollen analysis results.

## Experimental design and sampling regime
- 20 lit sites paired with nearby hedgerows (unlit sites) to control for habitat variables.
- Lit sites required at least one high-pressure sodium street light nearby; unlit sites were >100 m from any street lights.
- Distances: within-pair site distance ~207 m on average (range 120–330 m); nearest-extrapair-neighbour-distance among pairs ~6.0 km on average.
- Distance to nearest habitation recorded to account for floristic variability in gardens.
- Sampling employed three methods (night-time transects, overhead flight activity surveys, light-traps) across three seasonal periods: spring, early summer, late summer.
- Each pair was sampled once per method per season, with lit/unlit transects conducted on the same night where possible; light-traps conducted on a separate night.
- Weather gating: sampling occurred under suitable moth activity conditions (dry, Beaufort 3 or lower wind, minimum 12 °C).
- Weather and site conditions caused partial sampling (six pairs per method in spring), resulting in 46 paired observations per method.

## Data collection methods and instrumentation
- Light-level measurements with a CEM DT-1300 lux meter (lit sites higher light levels than unlit sites).
- Night-time transects: 25 m transects with a red-filtered floodlight to minimize moth response; moths captured with a hand net after 1 minute per section (five 5 m sections per transect), repeated thrice per sampling occasion.
- Overhead flight activity: vertical counting of moths during 1-minute counts using a bright LED torch to assess higher-altitude activity (3–12 m).
- Light-traps: Heath-style traps with 8 W actinic bulbs, operated from dusk until battery depletion (~8 hours); traps placed at the centers of lit and unlit sites and rotated across sessions to avoid interference.
- Species data and morphological notes: standard identification of captured moths; non-moth taxa excluded from overhead counts.

## Pollen transport assessment
- Pollen sampling from moth proboscides: moths euthanized and stored (-20°C) until analysis; proboscises swabbed with 1 mm³ fuchsin jelly to capture pollen.
- Microscopy (400x) used to morphotype and identify pollen against reference keys and local plant knowledge.
- Pollen morphotypes grouped when species-level separation was not possible; pollen from species lacking a functional proboscis (e.g., Hepialidae) was not swabbed.

## Data structure and contents
- Four CSV spreadsheets:
  - F1_sites.csv – site pair details (e.g., Site_Number, Site_Name, Lit_Site_Grid_Ref, Hedge_Height, Lamp_Height, Margin_Width, Crop, Distances to habitation and to other sites, Number of lights, Lit_site_Light_reading in lux).
  - F2_moths.csv – moth observations (Date, Site, Method, Treatment [Lit/Unlit], Reference, BinomialName, EnglishName, Family, Group [Macro/Micro]).
  - F3_overhead.csv – overhead flight-activity counts (Date, Site, Treatment, FirstCount, SecondCount, ThirdCount).
  - F4_pollen.csv – pollen analysis per moth (MothReference; BinomialName; 28 morphotype columns with counts; morphotype metadata including family and probable identifications when known).
- Keys for linking data across files include Site_Number, Date, Method, Treatment, and MothReference.

## Data quality, limitations, and considerations
- Some sampling periods were weather-limited, leading to fewer data for certain methods in spring.
- Overhead counts may include non-moth insects (filtered to Lepidoptera or clearly identified groups where possible).
- Pollen identifications rely on morphotypes and available reference materials; some morphotypes remain unidentified or ambiguously classified.
- Time spent on capturing each individual moth was not included in total search time.

## Provenance and publication link
- Dataset associated with Macgregor et al., The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport (in press, Global Change Biology).

## How Data Leaders can use this dataset
- As a robust, multi-method, matched-pair design for evaluating how street lighting affects nocturnal insect activity and pollen transport.
- To study data interoperability: four linked CSVs illustrate how to integrate field observations with biological sampling (pollen) for ecological impact assessments.
- To inform data governance: explicit site-pair matching criteria and metadata (habitat, hedge, verge characteristics) support comparability and replication across networks.
- To identify data gaps and standardization needs (e.g., metadata completeness, taxonomic resolution, and standardized pollen morphotype definitions) for cross-program data sharing and broader ecosystems research.

## Reference
- Macgregor, C.J., Evans, D.M., Fox, R. and Pocock, M.J.O (in press) The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.