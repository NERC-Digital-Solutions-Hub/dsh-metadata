# Basin - Supporting Information

- This document outlines the study area, data generation methods, nature and units of recorded values, quality control, and data structure for the land use products under four 2030 scenarios in the Luanhe River Basin (LRB).
- Acknowledges UKRI/NERC TaSE support (Grant NE/S012427/1).

## Study Area
- Luanhe River Basin (LRB): ~45,000 km2 in semi-arid North China (39°10′–42°30′ N, 115°30′–119°15′ E).
- Climate: temperate continental monsoonal with semi-arid characteristics; 1982–2015 mean temperature 7.0 ± 2.6 °C and precipitation 488.4 ± 80.7 mm.
- Seasonal precipitation: concentrated in summer (200–550 mm; 66–76% of annual rainfall).
- Land cover gradient: upper reaches grassland; middle-lower reaches temperate forest; eastern plains cropland and urban areas.
- Population: ~5.4 million; population density ~122 people per km2.
- Visual reference: Figure 1 shows the LRB location.

## CLUMondo Framework (2.1)
- Three-step map development:
  1) Map land systems for 2000 and 2015 by integrating human–environment datasets.
  2) Calculate relationships between land systems and explanatory factors for 2000; parameterise and calibrate CLUMondo model using 2015 map.
  3) Simulate 2015–2030 land system changes under four scenarios representing different commodity/service demands and management pathways.
- Overall workflow illustrated in Figure 2.

## Land System Classification (2.2)
- Classification based on: (1) land use/cover, (2) livestock, (3) agricultural intensity.
- Data source: China National Land Use and Cover Change (CNLUCC) dataset (Liu et al., 2014; Xu et al., 2018).
- CNLUCC categories: farmland, forestland, grassland, water, urban land, unused land.
- Classification thresholds set by natural breaks in variable distributions.
- Data used for delineating land systems and explanatory variables (detailed in Table 1) include:
  - Delineate Land Systems inputs: class indices (0–1) for potential cropland production and livestock density; sources from RESDC and Global Livestock Distribution data.
  - Explanatory factors: climatic (temperature, precipitation, moisture index), altitude, slope, soil characteristics (clay content, organic content, pH, drainage, soil type), and socioeconomic factors (accessibility, population density, GDP).
  - Primary data sources: RESDC, NASA SRTM, HWSD v1.2, Verburg et al. (2011), etc.
- Outputs: a land system delineation framework and related explanatory datasets used for modelling.

## Scenarios Formulation (2.3)
- Four scenarios to explore LRB land system evolution and challenges: Trend, Expansion, Sustainability, Conservation.
- Scenarios reflect different socio-economic development, environmental targets, local plans, policies, and stakeholder inputs.
- Table 2 shows average annual changes from 2015 to 2030 for:
  - Crop production (ton)
  - Livestock numbers (head)
  - Built-up land (km2)
  - Forest extent (km2)
- Notes: Some categories are not specified and are allocated by the CLUMondo model (n/a).

## Nature and Units of Recorded Values
- Raster data representing land use maps with nine land use classes for each scenario in 2030.

## Quality Control
- Validation approach: compare simulated 2000–2015 land systems against actual 2015 map.
- Metrics:
  - Kappa simulation: overall agreement of simulated transitions (range -1 to 1).
  - Kappa transition: agreement in the amount of transitions (0 to 1).
  - Kappa transition location: spatial allocation agreement (-1 to 1).
- Results for 2015 validation indicate strong model performance:
  - Overall Kappa simulation: 0.86 (with per-class values ranging up to 0.94–0.99 for several categories).
  - Kappa transition: overall ~0.99; per-class values similarly high (e.g., Forest 0.92, Water 0.97, Built-up 0.99).
  - Kappa transition location: overall ~0.87; per-class values up to 0.99 for several categories.
- Overall, high accuracy indicates good applicability of CLUMondo for predicting future land-use changes in the LRB.

## Data Structure (5)
- Four land use maps for 2030 under the four scenarios:
  - Trend_2030.tif
  - Expansion_2030.tif
  - Sustainability_2030.tif
  - Conservation_2030.tif
- Coverage: entire LRB; format: raster GeoTIFF.
- Coordinate systems:
  - Geographic: Krasovsky 1940 (GCS_Krasovsky_1940)
  - Projected: Krasovsky 1940 Albers (Krasovsky_1940_Albers)
- Grid: 1 km resolution.
- Nine land use classes (grid values 0–8):
  0 = Extensive cropland
  1 = Medium intensive cropland
  2 = Intensive cropland
  3 = Forest
  4 = Grassland with low livestock
  5 = Grassland with high livestock
  6 = Water
  7 = Built-up area
  8 = Unused land
- Table 3 provides the raster class values; the product covers the LRB extent.

## References (selected)
- Foundational datasets and methodological sources include: CNLUCC (Liu et al., Xu et al., 2018), RESDC data, NASA SRTM, HWSD v1.2, CLUMondo framework (Van Asselen and Verburg, 2013), and associated validation studies (Jin et al., 2019; Liu et al., 2017).

- Data products and results are designed to enable end-user exploration and analysis of future land-use trajectories under different policy and development pathways.