# RECOUP-Moor Environmental data: Methodology

- Field site: Stalybridge estate on Saddleworth Moor (blanket bog near Manchester, UK). Fire event: wildfire on June 24, 2018, lasting six weeks, affecting 18 km2 and causing large-scale removal of surface vegetation.

- Study design and sampling:
  - 10 plots established in October 2018, each 10 m × 10 m.
  - 5 plots suffered a shallower (shallow burn) and 5 plots a deeper (deep burn) burn; surface vegetation removed, exposing bare peat.
  - For each plot, recorded geographical properties: location, elevation, and slope.
  - Soil temperature measured at multiple time points over 24 months.

- Sample collection and preparation:
  - July 23, 2019: peat samples collected (each 5 cm × 5 cm × 2 cm) from the surface of each plot.
  - Samples were homogenized, kept at ~5 °C until analysis.
  - Preparation: dried at 70 °C for 72 hours, then crushed to a fine powder.

- Chemical analyses:
  - Carbon and nitrogen: three subsamples per plot, combusted at 1800 °C using a Vario Micro Cube to quantify carbon and nitrogen. Values averaged across subsamples after verifying homogeneity.
  - Elemental composition: two subsamples per plot analyzed by ICP-MS to determine 22 elements. Values averaged across subsamples.

- Data quality and processing details:
  - Homogeneity checks: sub-sample values compared to ensure consistency before averaging.
  - Sample handling included cold storage prior to analysis to preserve integrity.

- Variable Key (dataset definitions):
  - Plot_number: Plot Number.
  - Plot_ID: ID distinguishing plot feature and replicate (S1-5 = shallow burn, D1-5 = deep burn, R1-5 = unburned/reference).
  - N_Coor, W_Coor: Latitude and Longitude coordinates.
  - Temp_Oct18, Temp_May19, Temp_Jul19: Soil temperatures at specified dates.
  - CN_ratio: Carbon to Nitrogen ratio.
  - C_cont, N_cont: Carbon content (%) and Nitrogen content (%).
  - Slope, Elevation: Terrain characteristics.
  - Al, As, B, Ca, Cd, Co, Cr, Cu, Fe, Hg, K, Mg, Mn, Mo, Ni, P, Pb, S, Si, Sr, Zn: concentrations (mg/g) of 22 elements.