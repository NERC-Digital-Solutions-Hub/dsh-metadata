# Overview

- This dataset documents moths captured at paired lit and unlit sites and the pollen sampled from their proboscides, collected near Wallingford, Oxfordshire, UK, from May to September 2014. The study was designed to assess the effects of street lighting on moths and nocturnal pollen transport, with analysis published in Global Change Biology.
- The dataset includes four spreadsheets: F1_sites.csv, F2_moths.csv, F3_overhead.csv, and F4_pollen.csv.

## Study design and site pairing

- 20 lit sites, each paired with a nearby hedgerow segment (unlit site) to control for habitat variables.
- Lit sites required at least one nearby high-pressure sodium street light; unlit sites were more than 100 m away from any street lights.
- Within-pair distances were small (mean about 207 m; range 120–330 m) and closer to each other than to other pairs (nearest neighbour distance mean ~6 km).
- Recorded road/hedge/field characteristics to ensure comparable conditions between paired sites (e.g., hedge height, width, crop type, verge width, hedgerow trees presence, ditch presence).

## Sampling regime and timing

- Three sampling methods conducted at each site pair: night-time transects, overhead flight activity surveys, and light-trapping.
- Sampling windows divided into three 6-week periods: spring (May–mid June), early summer (mid June–July), late summer (August–mid September).
- Sampling conditions required for moth activity: dry weather, wind ≤ Beaufort 3, minimum temperature ≥ 12 °C.
- Within each season, each pair was sampled once per method (transect and overhead on the same night; light-trapping on a separate night). Some weather constraints led to six pairs per method in spring, resulting in 46 paired observations per method.

## Data collection methods and instruments

- Night-time transects: 25 m transects with a lit midpoint; each transect replicated three times per session, alternating lit and unlit conditions. Red-filtered floodlight used to reduce moth visibility and observation bias; moths captured with a net to avoid recapture.
- Overhead flight activity: counts of moth passes through a vertical beam (1 minute per replicate; three replicates per session) to quantify higher-altitude activity (3–12 m above ground).
- Light-traps: Heath-style traps (8 W actinic bulbs) powered by a 12 V battery, operated for ~8 hours per night; traps placed at the center of both lit and unlit sites and collected the following morning.
- Light intensity measurements: 0 lux at unlit sites; median 2.3 lux at lit sites (range 0.2–12.1 lux).

## Pollen transport methodology

- Pollen was sampled from the proboscides of moths after euthanasia and storage at −20°C.
- Probes were relaxed for 24 h, then swabbed with fuchsin jelly to collect pollen from the proboscis (to avoid cross-contamination).
- Slides were prepared and pollen morphotypes identified via morphological keys and reference collections; morphotypes represent groupings that may include multiple species.
- Pollen analysis conducted between November 2014 and March 2015; non-moth taxa identified but excluded from the pollen dataset when not clearly moth-associated.

## Data structure and contents

- F1_sites.csv: site-level information for each pair (Site_Number, Site_Name, Lit_Site_Grid_Ref, Hedge_Height_m, Lamp_Height_m, Margin_Width_m, Crop, Distance_Lit_site_To_Habitation_m, Distance_Lit_to_Unlit_m, Distance_to_Nearest_Extrapair_Neighbour_Site_km, Number_of_lights_within_100m, Lit_site_Light_Meter_reading_lux).
- F2_moths.csv: moth-level data (Date, Site, Method: Transect or Trap, Treatment: Lit or Unlit, Reference, BinomialName, EnglishName, Family, Group: Macro or Micro).
- F3_overhead.csv: overhead flight-activity counts (Date, Site, Treatment, FirstCount, SecondCount, ThirdCount).
- F4_pollen.csv: pollen data per moth (MothReference; BinomialName; and 28 morphotype columns with counts; each morphotype includes taxonomic details and exemplar identifications where known).

## Methods: Attributes of matched-pair sites

- Lit sites selected to have street lighting characteristics matched with nearby hedgerows.
- Criteria covered road orientation, road width, land use on far side, verge width, field margin width, hedge dimensions, hedge species composition, presence/absence of ditches and hedgerow trees within 50 m, crop type, and crop state at sampling.

## Publication and provenance

- The dataset supports the study: Macgregor, C.J.; Evans, D.M.; Fox, R.; Pocock, M.J.O. (in press) The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.
- Data completeness: described as complete; pollen morphotypes and identifications derived from established keys and local plant taxa knowledge.