# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- A collection of soil hydraulic measurements from the Climoor field site in Clocaenog Forest, North Wales, collected 2010–2012.
- Five data sets cover bulk density, unsaturated hydraulic conductivity, and soil water release curves (both wet and dry soil).
- Data were quality checked; incorrect or missing values were removed, no infilling performed, and NAs added where data were absent.
- The Clocoenog site is a climate-change experiment (drought and warming) with automated roof and curtain treatments to reduce rainfall and modify nighttime radiation.

## Data sets and content
- (1) Bulk_density.csv
  - Dry bulk density for 0–5 cm depth; includes saturated water content (SatVWC), fraction of solids (FofS), and particle density estimates (EstPD).
  - Context columns: Plot, Treatment, and sample metadata.
  - Structure: 6 columns, 10 rows.
- (2) Minidisk_K.csv
  - Field-measured unsaturated hydraulic conductivity at tensions of -2 cm and -6 cm using a mini-disk infiltrometer.
  - Also includes associated data such as plot, treatment, tension, and mean hydraulic conductivity values.
  - Structure: 5 columns, 19 rows.
- (3) Hyprop_K.csv
  - Laboratory-measured unsaturated hydraulic conductivity using HYPROP on soil cores (plots 1–9 represented across warming/control treatments).
  - Includes suction values and corresponding unsaturated conductivity (cm/day) for each plot.
  - Structure: 18 columns, 45 rows.
- (4) Hyprop_SWRC.csv
  - Soil water release curves from HYPROP measurements (wet soil), interpolated to regular suction values.
  - Includes interpolation point numbers and VWC (volumetric water content) for multiple plots under different treatments.
  - Structure: 11 columns, 501 rows.
- (5) WP4_SWRC.csv
  - Soil water release curves for dry soil measured with a WP4 potentiometer.
  - Includes temperature, soil moisture (m3/m3), matric potential (MPa), and pressure head (cm of water).
  - Structure: 4 columns, 60 rows.

## Site, treatments, and sampling context
- Location: Clocaenog Forest, upland Atlantic heathland with Calluna vulgaris; automated drought and warming experiments.
- Treatments: Drought, Warming, and Control, each with three replicate plots (4 m x 5 m).
- Rain exclusion: Drought treatment uses retractable roofs May–September to reduce rainfall by ~20%; some small events may still be missed.
- Warming treatment: Night-time retraction of aluminum mesh curtains driven by light sensor; reduces heat loss at night and slightly reduces rainfall (approx. 14% annual reduction) due to rain-detector timing.
- Sampling details:
  - HyPROP samples collected from top 250 cm³ soil cores (0–5 cm depth) near the eastern plot edge.
  - Minidisk samples collected in the field (two measurements per plot) in 2011–2012.
  - WP4 samples collected on control plots and processed in the lab in 2010.
  - Core processing and storage followed standardized procedures; all hydrological measurements were performed by experienced soil scientists.

## Data processing and quality assurance
- HYPROP data processed with HYPROP-FIT software; water release curves interpolated onto a common suction grid using spline fitting in R.
- Minidisk data converted to hydraulic conductivity using standard manuals.
- WP4 data processed according to the WP4 Operator Manual.
- Bulk density calculated from oven-dried mass (105°C, 16 h) divided by core volume.
- Visual QA performed with basic plotting; no data infilling performed.
- Supporting materials and manuals are included with the dataset.

## Provenance and roles
- D.A. Robinson: HYPROP measurements and soil water release curves.
- I. Lebron: HYPROP measurements, soil water release curves, and bulk density.
- A.R. Smith: WP4 measurements.
- M.R. Marshall: Minidisk measurements.
- B.A. Emmett: Principal investigator.
- S. Reinsch: Field site science management.
- D.M. Cooper: Statistical interpolation in R.
- M. Brooks: Field site and roof maintenance.

## Usage notes and references
- The data support evaluation of how warming and drought affect soil hydraulic properties and moisture dynamics.
- Reported in scientific contexts: Domínguez et al. (2015); Reinsch et al. (2016a, 2016b); Robinson et al. (2016); and related Clocaenog publications.
- Keywords: soil water release, hydraulic conductivity, Clocaenog, HYPROP, bulk density, infiltrometer.