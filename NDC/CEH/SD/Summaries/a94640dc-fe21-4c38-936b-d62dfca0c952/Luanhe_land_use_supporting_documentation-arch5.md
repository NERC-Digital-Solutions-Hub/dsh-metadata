# Basin - Supporting Information

- The document describes the study area, generation methods, nature and units of recorded values, quality control, and data structure for land use products under four scenarios in 2030 in the Luanhe River Basin (LRB).

## Study Area
- Luanhe River Basin (LRB) area: ~45,000 km2 in semi-arid North China (coordinates roughly 39°10′–42°30′ N, 115°30′–119°15′ E).
- Climate: temperate continental monsoonal with a semi-arid regime; 1982–2015 average temperature 7.0 ± 2.6°C and precipitation 488.4 ± 80.7 mm.
- Summer dominates rainfall (200–550 mm, 66–76% of annual precipitation); distinct land covers: upper reaches grassland, middle-lower reaches temperate forests, eastern plains cropland and urban areas.
- Population: ~5.4 million; density ~122 people/km2.

## CLUMondo framework
- Land system maps created for 2000 and 2015 by integrating multiple human-environment datasets.
- The CLUMondo model was parameterized and calibrated using the 2015 land system map.
- Future changes from 2015 to 2030 simulated under four scenarios representing different commodity/service demands and management pathways.
- The workflow is illustrated in a dedicated figure (Fig. 2).

## Land system classification
- Classification based on three main factors: (1) land use/cover, (2) livestock density, (3) agricultural intensity.
- Data source: China National Land Use and Cover Change (CNLUCC) dataset (RESDC, CAS) with six land use/cover categories: farmland, forestland, grassland, water, urban land, unused land.
- Accuracy: validated with field verification; ~10% of counties validated; accuracy of selected polygons > 94.3%.
- Data used for delineation includes land system delineation (class index 0–1) and explanatory factors from climate, soil, topography, and socioeconomic variables (e.g., temperature, precipitation, altitude, slope, soil properties, accessibility, population, GDP).
- Explanatory factors sources include RESDC, NASA SRTM, HWSD v1.2, and literature-derived socioeconomic data.

## Scenarios formulation
- Four scenarios: Trend, Expansion, Sustainability, and Conservation.
- Designed to explore land system evolution and challenges based on different socio-economic development, environmental targets, local plans, policies, and stakeholder input.
- Table 2 provides average annual changes 2015–2030 for: crop production, livestock numbers, built-up land, and forest (where specified). Some scenarios specify changes for certain categories while others are allocated by the model.

## Nature and units of recorded values
- Raster data representing land use maps with nine land use classes.

## Quality control
- Model validation used the 2000–2015 simulation against the actual 2015 land system map.
- Metrics: Kappa simulation (overall and per class), Kappa transition, and Kappa transition location.
- CLUMondo showed high accuracy: overall Kappa simulation = 0.86; Kappa transition near 1; Kappa transition location up to ~0.99 for several classes, indicating strong agreement in quantity and spatial allocation of changes.
- Detailed per-class Kappa scores (e.g., forest, grassland, water, cropland) demonstrate robust performance.

## Data structure
- Outputs: four land use maps for 2030 under the four scenarios: Trend_2030.tif, Expansion_2030.tif, Sustainability_2030.tif, Conservation_2030.tif.
- Extent: LRB; format: raster GeoTIFF; coordinate systems: GCS_Krasovsky_1940 and Krasovsky_1940_Albers projection.
- Resolution: 1 km; nine land use classes encoded as: 0 extensive cropland, 1 medium intensive cropland, 2 intensive cropland, 3 forest, 4 grassland with low livestock, 5 grassland with high livestock, 6 water, 7 built-up, 8 unused land.
- Class mapping corresponds to Table 3 values.

## References
- Wu et al. 2020; Xu et al. 2018; Zhang et al. 2019, providing context for climate, land use data, and hydrological implications.