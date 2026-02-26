# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Abstract and Data Content
- Five data sets of soil hydraulic properties collected at the Climoor field site, Clocaenog Forest, North Wales (56°23'N, 10°57'W).
- Datasets include:
  - 1) Soil bulk density (0–5 cm) and saturated water content.
  - 2) Unsaturated hydraulic conductivity in the field at tensions of -2 and -6 cm using a minidisk infiltrometer.
  - 3) Unsaturated hydraulic conductivity measured in the laboratory on HYPROP soil cores.
  - 4) Soil water release curves for wet soil from HYPROP measurements (laboratory).
  - 5) Soil water release curves for dry soil measured with a WP4 potentiometer (laboratory).
- Quality checked; incorrect/missing values removed, no data infilling; NA values added where data are absent.
- Data collected between late 2010 and early 2012.
- Purpose: monitor site-specific soil properties at a reference time to study the effects of warming and drought on ecosystem processes.

## Site, Treatments, and Sampling Design
- Site: Clocaenog climate change field site, upland Atlantic heathland dominated by Calluna vulgaris.
- Long-term drought and warming experiment initiated in 1999 with replicated plots (three per treatment) and fully automated rain exclusion roofs.
- Drought treatment: ~20% reduction in rainfall May–September; some small events may be excluded due to sensor limits.
- Warming treatment: retractable aluminum curtains at night that reflect infrared radiation, reducing heat loss; rainfall is sometimes excluded due to rain-triggered retraction, yielding an average ~14% rainfall reduction.
- Wind limits: curtains do not operate in winds >10 m/s.
- Experimental design: 3 drought roofs, 3 warming roofs, and 3 control plots (scaffold-mirrored shading on controls).
- Sampling location and method: Hyprop cores (250 cm³, 5 cm deep) collected from the eastern edge of plots away from prevailing wind/rain; samples collected in 2011 under heather; near rain gauge area.
- Plot and sample identifiers include specific treatments (control, drought, warming) and plot-level design details.

## Data Processing and Quality Assurance
- HYPROP data processed with HYPROP-FIT software; water release curves interpolated onto a common suction scale using spline fitting in R.
- Minidisk infiltrometer measurements converted to hydraulic conductivity using standard methods from manufacturer manuals.
- WP4 measurements were conducted in the lab on dried/dried-equilibrated samples following the WP4 potentiometer methodology.
- Bulk density calculated from oven-dried mass (105°C, ~16 hours) divided by sample ring volume; samples described as fully organic with no stones.

## Data Files and Structure
- (1) Bulk_density.csv
  - Content: Dry bulk density (g/cm³), SatVWC (saturated volumetric water content), FofS (fraction of solid material), EstPD (particle density), with per-plot and per-treatment metadata.
  - Structure: 6 columns, 10 rows; includes Plot, Treatment, and measurement values.
- (2) Minidisk_K.csv
  - Content: Unsaturated hydraulic conductivity measured in the field with minidisk (at -2 cm and -6 cm tensions); includes mean_k in cm/s and cm/day, plot-level, treatment-level.
  - Structure: 5 columns, 19 rows; includes Plot, Treatment, h0 (tension), mean_k values; notes indicate pairing with tension.
- (3) Hyprop_K.csv
  - Content: Unsaturated hydraulic conductivity measured in HYPROP laboratory experiments; multiple plots with suction values and corresponding conductivity in cm/day.
  - Structure: 18 columns, 45 rows; includes Suction (kPa) for each plot and corresponding Unsaturated_hydraulic_conductivity (cm/day) per plot.
- (4) Hyprop_SWRC.csv
  - Content: HYPROP-derived soil water release curve data; interpolation point numbers and corresponding VWC at various suction values for each plot (Plot1_Warming, Plot2_Warming, Plot3_Control, Plot4_Drought, Plot5_Drought, Plot6_Control, Plot7_Warming, Plot8_Drought, Plot9_Control).
  - Structure: 11 columns, 501 rows; includes Interpolation_number and VWC per plot.
- (5) WP4_SWRC.csv
  - Content: WP4 potentiometer-derived soil water release curves; includes Temperature, Soil moisture (m³/m³), Matric potential (MPa), and Pressure head (cm of water).
  - Structure: 4 columns, 60 rows.

## Metadata, Provenance, and Roles
- Data collected by experienced soil scientists; key contributors include:
  - D.A. Robinson – HYPROP measurements and soil water release curves
  - I. Lebron – HYPROP measurements, soil water release curves, bulk density
  - A.R. Smith – WP4 measurements
  - M.R. Marshall – minidisk measurements
  - B.A. Emmett – Principal Investigator, Clocaenog site
  - S. Reinsch – field site science manager
  - D.M. Cooper – statistical interpolation in R
  - M. Brooks – field site and roof maintenance
- Supporting documentation and manuals referenced for methods (HYPROP, HYPROP-FIT, WP4, minidisk) are included with the dataset.

## Geographic and GIS-Relevant Context
- Site location coordinates enable integration with spatial datasets (e.g., climate, meteorology, topography) for GIS analyses.
- Data are plot-based, enabling map-based visualization of soil hydraulic properties across drought, warming, and control treatments.
- Coherent time frame (2010–2012) supports temporal comparison with other climate experiments at Clocaenog and elsewhere.

## References
- Domínguez et al. 2015; Reinsch et al. 2016a, 2016b; Robinson et al. 2016; Sowerby et al. 2008; Dominguez et al. 2015; Pertassek et al. 2015; Peters & Durner 2015; UMS HYPROP manuals (2015).
- Data interpretation and analyses linked to HYPROP-FIT and related software manuals.

## Potential GIS and Data-Product Implications
- Enables creation of map-based visuals of soil hydraulic properties (bulk density, saturated water content, unsaturated conductivity, soil water release curves) across plots and treatments.
- Facilitates spatial analysis of treatment effects (drought vs. warming vs. control) on soil properties, and integration with meteorological data from Clocaenog.
- Supports temporal comparisons with other climate manipulation studies and contributes to spatially explicit models of soil moisture dynamics under warming and drought scenarios.