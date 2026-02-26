# RECOUP-Moor Environmental data: Methodology

## Field Site
- Stalybridge estate near Manchester, UK; blanket bog (Saddleworth Moor) dominated by Calluna vulgaris and Eriophorum vaginatum.
- June 24, 2018: wildfire on Saddleworth Moor; lasted six weeks; affected 18 km² and removed surface vegetation.

## Methods
- Field design: 10 plots established in Oct 2018 on a post-fire site; each plot 10 m × 10 m.
- Burn categories: 5 plots shallow (less severe burn), 5 plots deep (more severe burn); all plots exposed bare peat post-fire.
- Spatial data: recorded geographical properties for each plot (location, elevation, slope).
- Temporal data: soil temperature measured at multiple time points over 24 months.
- Sampling: July 23, 2019, peat samples collected from each plot (5 cm × 5 cm × 2 cm) and stored at ~5 °C.
- Sample preparation: dried at 70 °C for 72 h, milled to fine powder.
- Carbon and nitrogen analysis: three sub-samples per plot combusted at 1800 °C; %C and %N measured with Vario Micro Cube; sub-sample results averaged to one per-plot value.
- Elemental analysis: two sub-samples per plot analyzed by ICP-MS for 22 elements; sub-samples averaged to one per-plot value.

## Variable Key
- Plot identifiers: Plot_number; Plot_ID (S1-5 = shallow burn, D1-5 = deep burn, R1-5 = unburned/reference).
- Spatial coordinates: N_Coor (latitude), W_Coor (longitude); Elevation (m), Slope (degrees).
- Temporal soil temperatures: Temp_Oct18 (22/10/18), Temp_May19 (14/05/19), Temp_Jul19 (23/07/19).
- Soil chemistry: CN_ratio (C:N ratio), C_cont (carbon content %), N_cont (nitrogen content %).
- Terrain: Elevation, Slope.
- Elements (mg/g): Al, As, B, Ca, Cd, Co, Cr, Cu, Fe, Hg (mercury; note text refers to “Silver content”), K, Mg, Mn, Mo, Ni, P, Pb, S, Si, Sr, Zn.

## GIS Relevance
- Provides geolocated, plot-level data with temporal soil temperature series and comprehensive soil chemistry.
- Enables mapping of post-fire changes in soil properties, correlation with terrain (elevation, slope), and burn severity (shallow vs deep).
- Data can be packaged as point features with rich attribute tables for visualization in GIS.