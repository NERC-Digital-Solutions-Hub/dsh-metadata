# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Aim and Scope
- Presents soil hydraulic measurement data from the Climoor field site, Clocaenog Forest, North Wales.
- Contains five data sets that capture different hydraulic properties and soil characteristics.
- Data collected to investigate effects of warming and drought on ecosystem processes; data intended to monitor site-specific soil properties at a reference time.
- Data quality-checked; incorrect/missing values removed; no infilling; NA values added where data are absent.

## Data Sets Overview
- 1) Soil bulk density (0-5 cm) and saturated water content.
- 2) Field-measured unsaturated hydraulic conductivity at tensions of -2 and -6 cm using a mini disk infiltrometer.
- 3) HYPROP-derived unsaturated hydraulic conductivity from soil cores measured in the laboratory.
- 4) Soil water release curves for wet soil corresponding to HYPROP measurements (laboratory).
- 5) Soil water release curves for dry soil measured with a WP4 potentiometer (laboratory).

## Data Quality and Processing
- Data have been quality assured; errors removed; data not infilled.
- Raw data interpolated to common suction values (HYPROP data) using spline fitting in R.
- Hydraulic conductivity conversions for mini-disk measurements follow standard manuals.
- HYPROP data analyzed with HYPROP-FIT software.
- WP4 data processed per standard WP4 procedures.
- Supporting documentation includes method manuals and interpolation procedures.

## Field Site and Treatments
- Clocaenog climate change field site: upland Atlantic heathland dominated by Calluna vulgaris.
- Experimental drought and warming treatments with three replicate plots per treatment and three controls.
- Drought treatment uses automated retractable roofs May–September to reduce rainfall by ~20%.
- Warming treatment uses retractable aluminum mesh curtains at night to reduce heat loss; rainfall reduction under warming ~14%.
- Roofs do not operate in winds above 10 m/s.
- HYPROP cores collected from the eastern edge of plots; samples taken under heather, moss-free.

## Sampling and Methods (Data Collection)
- HYPROP: 250 cm3 soil cores, 0-5 cm depth; water release curves determined by laboratory evaporation method; suction values aligned via spline interpolation; data processed with HYPROP-FIT.
- Minidisk infiltrometer: field measurements at -2 cm and -6 cm tensions; two measurements per plot.
- WP4: lab measurements of soil water potential (dewpoint method) on dry soil samples; rapid measurements (<5 minutes) with internal fan to aid equilibration.
- Bulk density: oven-dried mass (105°C, 16 hours) divided by sample ring volume.

## Data Structure Details
- (1) Bulk_density.csv: Dry bulk density, saturated water content, per plot and treatment.
- (2) Minidisk_K.csv: Unsaturated hydraulic conductivity from field minidisk measurements; columns for plot, treatment, suction, and mean k (cm/s or cm/day).
- (3) Hyprop_K.csv: Unsaturated hydraulic conductivity from HYPROP (lab) across plots; multiple suction points per plot.
- (4) Hyprop_SWRC.csv: HYPROP-derived soil water release curves; interpolated VWC values across suction (kPa) for each plot/condition.
- (5) WP4_SWRC.csv: WP4 soil water release curves for dry soil; variables include temperature, soil moisture, matric potential, and pressure head.
- Interpolation and data processing notes and accompanying manuals are included in the dataset’s support materials.

## Temporal Coverage and Sampling
- Data collection occurred across multiple years and seasons:
  - 2010 November: WP4 measurements (dry soil curves).
  - 2011 April and September: HYPROP measurements (wet soil curves and K).
  - 2011 September: HYPROP sampling under warming plots; control plots also sampled.
  - 2012 May: Minidisk infiltrometer measurements.
- Site description and climate treatment details provided for context and repeatability.

## Publications and References
- Data linked to key publications and data centre records:
  - Domínguez et al. 2015; Reinsch et al. 2016 (daily plot-level meteorological and AWS data); Robinson et al. 2016; Sowerby et al. 2008.
- Supporting documentation and data series described in the Clocoenog project outputs.

## Roles and Responsibilities
- D.A. Robinson: HYPROP measurements and soil water release curves.
- I. Lebron: HYPROP measurements, SWRCs, and bulk density.
- A.R. Smith: WP4 measurements.
- M.R. Marshall: Minidisk measurements.
- B.A. Emmett: Principal investigator, Climaor field site.
- S. Reinsch: Field site science manager.
- D.M. Cooper: Statistical interpolation in R.
- M. Brooks: Field site and roof maintenance.

## Relevance for Environmental Monitoring
- Provides standardized, high-quality soil hydraulic data suitable for time-series analysis and cross-site comparisons.
- Enables integration with climate and ecosystem datasets to assess drought and warming impacts on soil properties.
- Supports data transparency by documenting methods, QA processes, and data processing workflows; includes access to manuals and supporting materials (facilitating data reuse).