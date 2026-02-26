# Collection of water samples:

## Overview
- Fieldwork conducted autumns (September–November) 2018–2020 across the UK; collaboration with the Faroese Geological Survey (Jarðfeingi).
- Study sites span England, Scotland, Wales, Northern Ireland, and the Faroe Islands.
- Sampling targeted water bodies with peat or organic soils; multiple locations within each catchment (pools, headwaters, streams, inlets, reservoirs, lakes, outlets).

## Sampling design and in situ measurements
- Within each catchment, multiple sampling locations were used.
- Measured site variables on site: pH, conductivity, dissolved oxygen, water temperature; also air temperature, pressure, and humidity (using a Hach MM156 multi-parameter meter).

## Sample collection and processing
- Grab water samples (50 mL) collected at each site and filtered in the field through a 0.45 µm syringe filter; samples kept cold (in a cool bag, then 4 °C in transit) and later analyzed in the lab.
- In-field and laboratory analyses included dissolved organic/inorganic carbon, absorbance at eight wavelengths, and dissolved nutrients, cations, metals, and anions.

## Organic matter (DOM and POM) processing
- At about one third of sites, a large water sample was collected for particulate and dissolved organic matter.
- Filtration (0.7 µm) to extract particulate organic matter (POM); water concentrated to ~100 mL, then evaporated to dryness and collected as residue (DOM/POM processing).
- DOM and POM residues analyzed to determine elemental composition.

## Analytical methods
- DOM/POM elemental composition measured with an Elementar Vario MICRO cube (total carbon, nitrogen, hydrogen, oxygen; organic carbon after acid treatment to remove inorganic carbonates).

## QA and data quality
- Laboratory QA: 10% of samples analyzed in replicate; equipment calibrated at start and with ongoing checks.
- Data QA: replicate data compared; if within 95%, average value used; if not, samples re-analyzed.
- Derived metrics constrained by physical property restrictions after CHNO calculations.

## Datasets

- UK_FI_Water_Chemistry
  - N = 448 samples.
  - Site metadata: site code; environmental conditions at sampling (air temperature, humidity, air pressure, bank temperature at 10 cm soil probe, water temperature).
  - Water chemistry measured at the site: pH, electrical conductivity (µS cm⁻¹), dissolved oxygen (%).
  - Lab-measured chemistry: dissolved organic carbon (DOC, mg C L⁻¹), SUVA254, E4/E6 ratio, DON, Prop_DON, DOP, Prop_DOP; concentrations of Ca, K, Mg, Na, Al, Mn, Fe, Pb, Cd, Co, Cu, Ni, Zn, Li (mg L⁻¹).

- UK_FI_DOM_CHNO
  - Elemental content of dissolved organic matter (DOM) in UK and Faroe Islands samples: N, C, H, O, Org. C (percentages).
  - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C; prop C (proportion of total C that is organic).

- UK_FI_POM_CHNO
  - Elemental content of particulate organic matter (POM) in UK and Faroe Islands samples: N, C, H, O, Org. C (percentages).
  - Derived metrics: Cox, OR, DBE/C, C/N, H/C, O/C; prop C.

- UK_FI_SITES
  - Site metadata (locations anonymized; site coordinates not provided due to access constraints).
  - Type classifications for surface water sampling (L1/L2/L3/L4; INLET, SURFACE, OUTLET, etc., with detailed subtypes).
  - Land use at sampling site (e.g., Cutting, Felled Forest, Grazing, Moorland, Plantation, Renewable, Restored, Shooting, Woodland).
  - Vegetation cover categories (from UK CEH Land Cover maps; e.g., acid grassland, bog, broadleaf woodland, coniferous woodland, heather, etc.).
  - Catchment area (calculated via DEM models and QGIS; in km²).
  - Country: ENG, SCO, WAL, NIR, FAROE.

## GIS considerations and how to use the data
- Rich geospatial context: site-level attributes linked to water chemistry and organic matter metrics enable spatial analysis and mapping of chemical signatures across catchments.
- Data can be joined by site code to visualize relationships between chemistry (DOC, DOP, DOM/POM metrics) and land use, vegetation cover, and catchment characteristics.
- Catchment-area calculations via DEM/QGIS facilitate watershed-scale analyses and comparisons.
- Limitations: precise site locations are restricted due to anonymity, which may affect high-precision mapping at exact coordinates; catchment-scale and site-aggregate analyses are more feasible.

## Practical applications for GIS specialists
- Create map-based visualizations of water chemistry patterns across regions and watershed boundaries.
- Overlay DOM/POM metrics with land-use and vegetation-cover layers to explore environmental drivers.
- Integrate site metadata with chemical measurements to support policy briefs, client reports, or public-facing dashboards.
- Use catchment-area data to conduct spatial analyses of influence zones and connectivity among sampling sites.

## Notes on accessibility
- Site locations are not publicly disclosed in the dataset due to access constraints and anonymity requirements, limiting precise geolocation mapping but allowing broader catchment- and site-level analyses.