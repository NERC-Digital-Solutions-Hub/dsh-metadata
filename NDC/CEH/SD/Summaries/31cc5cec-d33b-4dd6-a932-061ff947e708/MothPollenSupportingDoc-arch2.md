# The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport

## Aim
- Document details of moths captured at paired lit and unlit sites and pollen sampled from their proboscides.
- Assess the effects of street lighting on moths and nocturnal pollen transport.
- Provide a complete dataset from a study conducted in 2014; data underpin a published analysis.

## Study area and design
- 20 lit–unlit site pairs within 40 km of Wallingford, Oxfordshire, UK; arable field margins.
- Lit site selected near at least one high-pressure sodium street light; unlit site (>100 m away) paired to control for habitat variables.
- Within-pair distance: mean 207 m (range 120–330 m); between-pair distance ~6 km.
- Distance to nearest habitation recorded due to potential garden biodiversity effects.
- Sampling: May–September 2014, divided into three six-week periods (spring, early summer, late summer).
- Weather conditions required: dry, Beaufort wind ≤ 3, minimum temperature ≥ 12°C; same-night sampling for paired sites to control conditions.
- Each pair sampled once per method per season: night-time transects and overhead flight activity on same night; light-trapping on a separate night.
- Weather/season constraints led to 46 sets of paired observations per method (six pairs in spring for each method).

## Data collection methods
- Light levels: measured with a CEM DT-1300 light meter; lit sites median 2.3 lux vs unlit sites <0.1 lux.
- Night-time transects: 25 m transects with a lit midpoint; three replicates per occasion, alternating lit/unlit order; moths captured with a net after 1 minute per 5 m segment; red-filtered floodlight to reduce moth attraction and maintain focus.
- Overhead flight activity: counts of moths passing through a vertical beam for 1 minute, repeated three times; excludes non-moth taxa where possible.
- Light-traps: Heath-type traps operated for ~8 hours from dusk; traps placed at lit and unlit centers; mean moths per trap ≈ 11.8.
- Equipment: lux meter, red-filter floodlight, strong LED torch, Heath traps, standard microscopes for pollen analysis.

## Pollen transport analysis
- Moths retained from sampling were euthanized and stored (-20°C) until pollen analysis.
- Proboscides swabbed with 1 mm3 fuchsin jelly to collect pollen; slides prepared and examined at 400x.
- Pollen morphotypes identified using standard keys and local reference collections; morphotypes represent groups that may include multiple species.
- Pollen analysis timeframe: November 2014–March 2015; Hepialidae (no proboscis) excluded from swabbing.

## Data structure and contents
- Four CSV files:
  - F1_sites.csv – site pair details (Site_Number, Site_Name, Lit_Site_Grid_Ref, Hedge_Height, Lamp_Height, Margin_Width, Crop, Distances, Number_of_lights_within_100m, Light_Meter_reading).
  - F2_moths.csv – moth-level records (Date, Site, Method, Treatment, Reference, BinomialName, EnglishName, Family, Group).
  - F3_overhead.csv – overhead flight counts (Date, Site, Treatment, FirstCount, SecondCount, ThirdCount).
  - F4_pollen.csv – pollen on proboscises (MothReference, BinomialName, followed by 28 morphotype pollen counts with morphotype metadata).
- F1–F4 collectively enable linking site context, moth captures, high-altitude activity, and pollen transport data.

## Analysis scope and published outputs
- Original dataset collection and analysis aimed to quantify street lighting impacts on moths and nocturnal pollen transport.
- Associated analysis published (in press) as: The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.

## Relevance for environmental monitoring analysts
- Standardised, paired design with explicit habitat controls enables robust comparisons across lit vs unlit conditions.
- Comprehensive metadata (hauteur, distance relationships, habitat features, light intensity) supports reproducibility and cross-site analyses.
- Multi-method data (transects, overhead counts, traps) provides a broad view of moth activity and abundance across vertical strata.
- Pollen transport data links insect behavior to plant-pollinator interactions, useful for integrated ecological assessments.
- Clear data structure (four CSV files) facilitates data sharing, re-use, and integration with other environmental datasets.
- Highlights practical challenges and considerations for data valorisation and data accessibility in monitoring programs (e.g., leveraging underlying data for broader analyses).

## Reference
- Macgregor, C.J., Evans, D.M., Fox, R. and Pocock, M.J.O (in press) The dark side of street lighting: impacts on moths and evidence for the disruption of nocturnal pollen transport. Global Change Biology.