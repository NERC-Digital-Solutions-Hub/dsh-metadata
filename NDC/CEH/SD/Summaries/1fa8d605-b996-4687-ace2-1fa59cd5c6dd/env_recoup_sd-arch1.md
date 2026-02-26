# RECOUP-Moor Environmental data: Methodology

- Field site and context
  - Stalybridge estate, Saddleworth Moor (UK), a blanket bog near Manchester.
  - 2018 wildfire on June 24 affected 18 km2 and caused large-scale removal of surface vegetation.

- Experimental design
  - 10 plots established in October 2018, each 10 m x 10 m.
  - Burn severity: 5 shallow burn plots (S1–S5), 5 deep burn plots (D1–D5).
  - 5 plots unburned/reference (R1–R5).
  - Post-fire condition: surface vegetation removed, exposing bare peat.

- Field measurements
  - Geographical properties recorded for each plot: location, elevation, slope.
  - Soil temperature measured at multiple time points over 24 months.
  - Specific temperature timestamps:
    - Temp_Oct18 (22/10/2018)
    - Temp_May19 (14/05/2019)
    - Temp_Jul19 (23/07/2019)

- Peat sampling and preparation
  - Peat samples collected on 23 July 2019 from the surface of each plot.
  - Sample size: 5 cm x 5 cm x 2 cm; homogenized and stored at ~5°C until analysis.
  - Preparation: dried at 70°C for 72 hours and crushed to a fine powder.

- Laboratory analyses
  - Carbon and nitrogen content
    - For each plot, three subsamples of the fine powder analyzed.
    - Combustion at 1800°C using a Vario Micro Cube (Elementar).
    - Carbon and nitrogen percentages quantified; consistency checked across subsamples.
    - Final CN_ratio and C_cont, N_cont values calculated as the average of the three subsamples per plot.
  - Elemental composition
    - ICP-MS analysis on two subsamples per plot.
    - Relative composition quantified for 22 elements.
    - Final elemental values calculated as the average of the two subsamples per plot.

- Data variables and structure
  - Plot identifiers and geometry
    - Plot_number
    - Plot_ID (S1–S5 = shallow burn, D1–D5 = deep burn, R1–R5 = unburned/reference)
    - N_Coor (latitude) and W_Coor (longitude)
  - Temporal measurements
    - Temp_Oct18, Temp_May19, Temp_Jul19 (soil temperature in °C)
    - CN_ratio (carbon to nitrogen ratio)
  - Chemistry and soil properties
    - C_cont (%), N_cont (%)
    - Slope (degrees), Elevation (m)
  - Elemental composition (mg/g)
    - Al, As, B, Ca, Cd, Co, Cr, Cu, Fe, Hg (noted as Silver content in text), K, Mg, Mn, Mo, Ni, P, Pb, S, Si, Sr, Zn

- Data quality and handling
  - Use of replication (3 CN subsamples; 2 ICP-MS subsamples) with averaging to ensure representativeness and homogeneity.
  - Clear documentation of sampling dates, plot burn status, and measurement methodologies.
  - Explicit units and equipment used (Vario Micro Cube for CN; ICP-MS for 22 elements).

- Potential analyses and applications for analysts
  - Assess correlations between burn severity and soil carbon/nitrogen content.
  - Explore relationships between burn severity and elemental composition in post-fire peat.
  - Model spatial and temporal variation in soil temperature and chemical properties over the 24-month period.
  - Compare plots across elevation and slope gradients to understand topographic influences on post-fire recovery.

- Metadata and provenance
  - Detailed description of field site conditions, plot designation, and analytical procedures to enable reproducibility and integration with other datasets.