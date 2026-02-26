# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- A multi-dataset collection of soil hydraulic measurements from the Climoor field site, Clocaenog Forest, North Wales.
- Five data sets cover: 1) dry bulk density and saturated water content (0-5 cm), 2) field unsaturated hydraulic conductivity from minidisk infiltrometer at tensions -2 and -6 cm, 3) HYPROP-based laboratory unsaturated hydraulic conductivity on 250 cm3 cores, 4) HYPROP-derived soil water release curves (wet soil) from laboratory measurements, 5) WP4 potentiometer soil water release curves (dry soil).
- Data quality controlled: incorrect/missing values removed; no infill; NA used where data absent.
- Collection period: end of 2010 to early 2012.
- Purpose: monitor site-specific soil properties to address questions about warming and drought effects on ecosystem processes; data represent a reference time for the site.

## Site and Treatments
- Location: Clocaenog climate change field site, upland Atlantic heathland dominated by Calluna vulgaris.
- Experimental design: drought and warming treatments with three replicates each, plus three control plots.
- Drought treatment: retractable roof excluding rainfall May–September, reducing annual rainfall by ~20% (some small events may be missed due to sensor limits).
- Warming treatment: retractable aluminum mesh curtains at night to reduce heat loss; automatically retracted during rain to partially preserve rainfall; average annual rainfall reduction ~14%.
- Operational limits: roofs do not operate in winds above 10 m/s.
- Sampling: HYPROP cores collected from the eastern plot edges; samples taken under heather, moss-free, within 2011 sampling windows (April and September 2011 for HYPROP; May 2012 for minidisk; November 2010 for WP4).

## Data Sets (1–5)
- (1) Bulk_density.csv
  - Dry bulk density measurements; 6 columns, 10 rows.
  - Includes plot, treatment, BD in g/cm3, saturated volumetric water content (SatVWC), fraction of solid material (FofS), estimated particle density (EstPD), and related metadata.
- (2) Minidisk_K.csv
  - Field-measured unsaturated hydraulic conductivity using minidisk infiltrometer at tensions of -2 and -6 cm; 5 columns, 19 rows.
  - Columns include plot, treatment, tension (h0 in cm), and mean hydraulic conductivity (cm/s and cm/day) with a note that values reflect Zhang (1997) calibrations.
- (3) Hyprop_K.csv
  - HYPROP laboratory-measured unsaturated hydraulic conductivity; 18 columns, 45 rows.
  - Data separated by plot and treatment; includes suction in kPa and corresponding unsaturated hydraulic conductivity (cm/day) for each plot.
- (4) Hyprop_SWRC.csv
  - HYPROP-derived soil water release curve data for the wet soil; 11 columns, 501 rows.
  - Interpolated SWRC data: interpolation index, suction (kPa), and volumetric water content (VWC) for each plotted condition (Plot1–Plot9 with warming/control/drought labels).
- (5) WP4_SWRC.csv
  - WP4-potentiometer soil water release curves for the dry soil; 4 columns, 60 rows.
  - Includes temperature, soil moisture (m3/m3 × 100), matric potential (MPa), and pressure head (cm of water).

## Data Processing and Quality Assurance
- HYPROP data processed with HYPROP-FIT software; raw data interpolated onto common suction values using spline fitting in R.
- Minidisk measurements converted to hydraulic conductivity via standard minidisk procedures; documentation and manuals included in supporting materials.
- WP4 SWRC implemented according to discontinued WP4-Operators-Manual; detailed methods provided in supporting materials.
- Bulk density calculated from oven-dried mass (105°C, 16 h) and core volume; samples described as moss-free and taken under heather.
- Data inspected with basic graphing as part of QA/QC; no data imputation performed; missing data labeled as NA.
- All data and methods are anchored with detailed references and manuals, including HYPROP and HYPROP-FIT documentation and related publications.

## Data Structure and Provenance
- Data were collected by experienced soil scientists; roles include HYPROP measurements (Robinson, Lebron), HYPROP SWRC and bulk density (Lebron, Smith), WP4 measurements (Smith), minidisk measurements (Marshall), site management and oversight (Emmett, Reinsch, Brooks), and statistical interpolation in R (Cooper).
- Data lineage includes explicit instrumentation (HYPROP system, minidisk infiltrometer, WP4 potentiometer), sampling depth (0–5 cm), and site treatment assignments (Control, Drought, Warming).
- Referenced publications and data-center entries document site context and data usage, including Domínguez et al. (2015), Reinsch et al. (2016), and Robinson et al. (2016).

## Applications for Analysis
- Enables examination of how drought and warming influence soil hydraulic properties at shallow depths.
- Facilitates cross-method comparisons (field minidisk vs. laboratory HYPROP) and linkage of soil water release characteristics to hydraulic conductivity.
- Supports modeling and prediction of soil moisture dynamics under climate change scenarios, with datasets suitable for correlational analyses and predictive modeling.

## References and Supporting Materials
- Published results and related datasets: Domínguez et al. (2015); Robinson et al. (2016); Reinsch et al. (2016).
- HYPROP, HYPROP-FIT, and WP4 manuals referenced for methodological details.
- Supporting documentation includes additional field site description, data series, and measurement procedures.