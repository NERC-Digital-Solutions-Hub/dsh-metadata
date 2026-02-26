# Collection of water samples:

- Study scope: Fieldwork conducted in autumn (Sept–Nov) 2018–2020 across the UK; collaboration with the Faroese Geological Survey (Jarðfeingi) to collect from sites with high organic soil content in the Faroe Islands; coverage across England, Scotland, Wales, Northern Ireland, and the Faroe Islands.
- Site types and contexts: Samples taken from various water body types with peat or organic soils; multiple locations within each catchment (pools, headwaters, streams, inlets, reservoirs, lakes, outlets) within access constraints.

## Sampling and site measurements

- In-situ site variables: pH, conductivity, dissolved oxygen, and water temperature; concurrent air temperature, pressure, and humidity recorded.
- Water sampling: Grab 50 mL samples collected at each site; filtration in the field through a 0.45 μm syringe filter (pre-rinsed); filtered water kept cold and dark (cool bag in the field, cool box in transit).

## Sample handling and storage

- Post-collection: Filtered water stored at 4 °C in the laboratory before chemistry analyses.
- Organic matter sampling: At about one-third of sites, a large water sample was filtered to remove solids, concentrated to ~100 mL, and then processed to yield residues representing colloidal and dissolved organic matter (DOM) and particulate organic matter (POM).

## Laboratory analyses and metrics

- DOM and POM analyses: Elemental composition (C, H, N, O) and organic carbon for DOM and POM after treatment (acid digestion to remove inorganic carbonates for CHNO analyses) using an Elementar Vario MICRO cube.
- Additional derived metrics: For DOM and POM, compute Cox (carbon oxidation state), OR (oxidative ratio), DBE/C, C/N, H/C, O/C, and prop C (proportion of total C that is organic).

## Quality assurance and data validation

- Laboratory QA: 10% of all samples replicated; equipment calibrated at run start and with ongoing checks.
- Data QA: Replicates compared; if within 95% agreement, averaged; if not, re-analysis performed.
- Derived metrics constrained by physical properties (e.g., bonding) to ensure data plausibility.

## Datasets and key variables

- UK_FI_Water_Chemistry (N=448)
  - Site identifiers and environment: site code; environmental conditions at sampling (air temp, humidity, air pressure, bank temp, water temp).
  - Field water chemistry: pH, electrical conductivity (EC), dissolved oxygen (DO).
  - Laboratory water chemistry: DOC, SUVA254, E4/E6, DON, Prop_DON, DOP, Prop_DOP, and concentrations of Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li (all in mg L−1 or µS cm−1 as specified).

- UK_FI_DOM_CHNO
  - Site code; elemental contents in dissolved organic matter: N, C, H, O, Org. C (percentages).
  - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C; prop C (percent organic carbon).

- UK_FI_POM_CHNO
  - Site code; elemental contents in particulate organic matter: N, C, H, O, Org. C (percentages).
  - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C; prop C.

- UK_FI_SITES
  - Site metadata and classifications: site code; Type (e.g., Lake, Headwater, Inlet, Reservoir, Outlet, Stream, Pool; with subtypes and descriptions).
  - Land use and vegetation: primary land use (e.g., cutting, felled forest, grazing, moorland, plantation, renewable, restored, shooting, woodland); vegetation cover categories (from CEH Land Cover maps).
  - Catchment information and geography: catchment area (km², via DEM/QGIS); country (ENG, SCO, WAL, NIR, FAROE).

- Data usability and governance: Datasets are structured to enable cross-dataset integration (chemistry with DOM/POM composition and site metadata); robust QA steps support reliability; site anonymization is observed for locations with restricted access.