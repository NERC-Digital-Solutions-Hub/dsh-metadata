# The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport

## Overview
- A dataset detailing moths captured at paired lit and unlit sites near Wallingford, Oxfordshire, UK (within 40 km), plus pollen sampled from moth proboscides.
- Collected in 2014 (May–September) to study effects of street lighting on moths and nocturnal pollen transport.
- Data underpin a published analysis on how street lighting may disrupt nocturnal pollen transport.

## Study design and spatial context
- 20 lit site pairs, each paired with a nearby hedgerow (unlit site) to control habitat variables.
- Lit sites required at least one adjacent high-pressure sodium street light; unlit sites >100 m from any street lights.
- Within-pair distance average 207 m (range 120–330 m); between-pair nearest neighbour distance average ~6.0 km (range 2.2–14.0 km).
- Distance to nearest human habitation recorded (lit site distance always less than unlit site distance).
- Sites located on arable field margins in south-east England (Oxfordshire and Berkshire).
- Lighting, hedgerow, verge, field marginal characteristics matched across pairs (road orientation, verge width, hedge height, crop type, etc.).

## Data collection and sampling methods
- Sampling methods (per pair per season): night-time transects, overhead flight activity surveys, and light-traps.
- Sampling periods divided into three six-week blocks: spring, early summer, late summer.
- Weather and conditions required for moth activity (dry, wind ≤ Beaufort 3, min temp ≥ 12°C).
- Sites within pairs sampled on the same evening to control environmental conditions (e.g., moon phase).
- Six replicate trials per method per season across pairs; total: 46 paired observations per method (spring period variability noted).

## Field equipment and measurements
- Light level: CEM DT-1300 light meter (lux) used; lit sites median 2.3 lux vs unlit sites 0 lux.
- Night-time transects: 25 m transects with a street light as midpoint; five 5 m sections; red-filtered floodlight to reduce moth attraction.
- Transect sampling: 1 minute per 5 m section, moving forward 10 paces between sections; moths netted and retained for ID.
- Overhead flight-activity surveys: 1-minute counts with a high-intensity LED torch; tallied moth passes (non-moth exclusions noted).
- Light-traps: Heath-style traps (8 W actinic bulbs) operated for ~8 hours; traps placed at lit and unlit centerpoints; collections used for moth IDs and pollen sampling.

## Data structure and contents
- Four spreadsheets:
  - F1_sites.csv: site-pair details (20 lit-unlit pairs) with fields such as Site_Number, Site_Name, Lit_Site_Grid_Ref, Hedge_Height_m, Lamp_Height_m, Margin_Width_m, Crop, Distance_Lit_site_To_Habitation_m, Distance_Lit_site_To_Unlit_site_m, Distance_to_Nearest_Extrapair_Neighbour_Site_km, Number_of_lights_within_100m, Lit_site_Light_Meter_reading_lux.
  - F2_moths.csv: moth capture records (Date, Site, Method, Treatment, Reference, BinomialName, EnglishName, Family, Group).
  - F3_overhead.csv: overhead flight counts (Date, Site, Treatment, FirstCount, SecondCount, ThirdCount).
  - F4_pollen.csv: pollen data per moth (MothReference, BinomialName) plus 28 morphotype columns with pollen grain counts and provisional identifications.
- F4_pollen.csv includes 28 morphotypes with associated taxonomic families and provisional identifications where possible.

## Pollen transport analysis
- All moths retained during sampling were pollen-swabbed from the proboscis only (post-collection storage at -20°C; relaxing chamber prior to swabbing).
- Pollen swabs prepared on microscope slides and examined at 400x; morphotypes identified using established keys and local references.
- Morphotypes represent groups that may contain multiple species; exact species-level resolution not always possible.

## Methods: attributes of matched-pair sites
- Lit site selection criteria emphasize similarity to the unlit paired site across road, verge, hedge, and field characteristics.
- Road characteristics: similar orientation (tolerance ±30°), similar road width, and similar land use on far side.
- Verge/hedge: similar verge width, field margin width, hedge height/width, hedge species composition, and presence/absence of ditch or hedgerow trees within 50 m.
- Field characteristics: similar crop type and crop state at sampling.
- Reference: Macgregor et al. (in press) Global Change Biology.

## GIS-focused considerations and uses
- Spatial data are structured for GIS integration: pairwise lit/unlit sites with grid references, distances, and habitat attributes.
- Potential map-based products:
  - Visualize lit vs unlit sites and hedgerow pairings on a map.
  - Map light intensity distributions (lux) across lit sites.
  - Spatial analysis of distances to habitation, nearest extrapair neighbours, and proximity to other lights.
  - Overlay habitat variables (hedge height, margin width, crop type) for habitat suitability mapping.
  - Link moth records (F2) and pollen transport data (F4) to locations for spatial pattern analysis.
- Data joinability: use Site_Number to connect F1_sites.csv with F2_moths.csv, F3_overhead.csv, and F4_pollen.csv.
- Grid references (Lit_Site_Grid_Ref) enable georeferencing and conversion to coordinates for mapping; note that distances were calculated using Google Earth for several fields (e.g., habitation distance, inter-site distances).
- Data limitations to consider in GIS work:
  - Seasonal sampling variability; not all methods completed in spring due to weather (46 sets per method).
  - Morphotype pollen identifications are morphologically defined and may group multiple species.
  - Some overhead counts may include non-moth taxa; data notes indicate exclusions were applied where possible.

## Reference
- Macgregor, C.J., Evans, D.M., Fox, R. and Pocock, M.J.O (in press) The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.