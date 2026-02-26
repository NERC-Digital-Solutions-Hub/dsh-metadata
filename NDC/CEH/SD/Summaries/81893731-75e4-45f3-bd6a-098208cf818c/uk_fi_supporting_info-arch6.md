# Collection of water samples:

- The study collected water samples across autumns 2018–2020, in collaboration with the Faroese Geological Survey (Jarðfeingi), including sites in England, Scotland, Wales, Northern Ireland and the Faroe Islands, focusing on water bodies with peat or organic soils and multiple locations within each catchment. Access restrictions limited site location details.

## Sampling scope and site types

- Water samples taken from different water body types with peat or organic soils: pools, headwaters, streams, inlets, reservoirs, lakes, and outlets.
- Within each catchment, several locations were sampled to capture spatial variability.
- Site type metadata covers a range of water body classifications (e.g., lakes, inlets, reservoirs, streams, pools) and proximities to lakes or reservoirs.

## Sampling protocol and field measurements

- In-field measurements: pH, conductivity (EC), dissolved oxygen (DO), water temperature; and ancillary air temperature, pressure, and humidity recorded using a portable setup (Hach MM156).
- Grab water samples: 50 mL collected at each site, filtered on site through a 0.45 µm syringe filter, kept cold (in a cool bag and cool box) and stored at 4 °C in the laboratory prior to analysis.

## Organic matter sampling (subset)

- At roughly one third of sites, larger water samples were collected in DI-rinsed caddies.
- Processing: filtration to remove particulates (0.7 µm, 47 mm), concentration to ~100 mL, then evaporation and drying to collect particulate organic matter (POM) and dissolved organic matter (DOM).

## Laboratory analyses

- DOM and POM elemental composition analyzed with a Elementar Vario MICRO cube to determine total carbon, nitrogen, hydrogen, and oxygen, with inorganic carbon removed by acid treatment.
- DOM and POM analyses provide both elemental content and derived metrics (see datasets).

## Quality assurance (QA)

- Lab QA: 10% of samples analyzed in replicate; calibration at run start and throughout; multiple checks.
- Data QA: replicate measurements compared; averages used if within 95% agreement; otherwise re-analysis.
- Derived metrics from CHNO content restricted by physical properties to ensure consistency.

## Datasets produced

- UK_FI_Water_Chemistry (N = 448)
  - Site and sampling metadata: site code, location within catchment.
  - Environmental conditions at sampling time: air temperature, humidity, air pressure, bank soil temperature, water temperature.
  - In-field water chemistry: pH, electrical conductivity (EC), DO.
  - Lab-based water chemistry: DOC, SUVA254, E4/E6, DON, Prop_DON, DOP, Prop_DOP, and concentrations of Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li (all in mg/L or µg/L as specified).
- UK_FI_DOM_CHNO
  - DOM elemental content (N, C, H, O, and organic C) and site code.
  - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C, and prop C (percent organic carbon).
- UK_FI_POM_CHNO
  - POM elemental content (N, C, H, O, and organic C) and site code.
  - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C, and prop C.
- UK_FI_SITES
  - Site metadata and classification: site code; Type (e.g., L1/L2/L3/L4 variants, R1/R2/R3/R4 variants, STREAM, POOL).
  - Land use: category describing primary land use (e.g., cutting, felled forest, grazing, moorland, plantation, renewable energy, restored, shooting, woodland).
  - Vegetation cover: CEH-derived categories (acid grassland, bog, broadleaf woodland, coniferous woodland, heather, heather grassland, improved grassland).
  - Catchment area: calculated via DEM models in QGIS (km²).
  - Country: ENG, SCO, WAL, NIR, FAROE. Note: site locations anonymized due to access restrictions.

## Data use and applicability for data support

- The datasets provide a cohesive, multi-layered view of water chemistry and organic matter across UK and Faroe Island sites.
- Rich metadata enables cross-dataset linking (site-level, environmental context, and bathymetric/land-use information) to support self-service exploration, dashboard creation, and data storytelling.
- Quality-controlled data with derived CHNO metrics supports interpretation of carbon cycling, organic matter processing, and nutrient dynamics in catchments.
- Data accessibility considerations: some site locations are anonymized, which may influence spatial analyses requiring precise geolocation.