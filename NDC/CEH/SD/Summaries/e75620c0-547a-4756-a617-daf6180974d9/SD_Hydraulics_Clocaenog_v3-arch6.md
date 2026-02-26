# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- Soil hydraulic properties dataset from the Climoor field site in Clocaenog Forest, North Wales.
- Collected 2010–2012 across five data sets to study effects of warming and drought on ecosystem processes.
- Data are quality checked, with incorrect/missing values removed; no infilling; NA values used where data are absent.

## Data Sets and Contents
- 1) Bulk density (0–5 cm) and saturated water content.
- 2) In-field unsaturated hydraulic conductivity via minidisk infiltrometer at tensions -2 cm and -6 cm.
- 3) HYPROP-based unsaturated hydraulic conductivity (lab) on soil cores.
- 4) HYPROP-derived soil water release curves (wet soil) from lab measurements on cores.
- 5) WP4 potentiometer soil water release curves (dry soil).
- Data were collected at specific dates: 2010 end–2012; instrumentation includes HYPROP cores, minidisk infiltrometer, and WP4 potentiometer.

## Site Context and Climate Treatments
- Clocaenog climate change field site: upland Atlantic heathland with Calluna vulgaris; drought and warming treatments in three replicated plots each, plus three control plots.
- Drought: automated retractable roofs exclude rainfall May–September, reducing rainfall by ~20%.
- Warming: retractable aluminum mesh curtains over the plots at night, reflecting infrared radiation and reducing heat loss; average rainfall reduction ~14% due to monitoring lag.
- Wind restrictions prevent operation in winds >10 m/s.
- Sampling focused on topsoil (0–5 cm) cores; site features podzolic organo-mineral soils with distinct organic-rich horizons.

## Sampling and Measurement Details
- HyPROP cores (250 cm³, 0–5 cm) collected from the eastern plot edge in 2011 (control, warming, drought).
- Minidisk infiltrometer measurements in the field (May 2012): two tensions per plot (-2 cm, -6 cm).
- WP4 SWRC measurements in the lab (November 2010) on dry soil from control plots.
- Measurements processed with HYPROP-FIT software; HYPROP data interpolated to a common suction grid with spline fitting in R.
- Minidisk data converted to hydraulic conductivity using standard procedures; WP4 data documented in the WP4 manual.

## Data Structure and File Details
- (1) Bulk_density.csv: Bulk density (g/cm³), SatVWC, FofS, EstPD; fields include Plot, Treatment, and quality indicators. 6 columns, 10 rows.
- (2) Minidisk_K.csv: Field-measured unsaturated hydraulic conductivity; includes Plot, Treatment, h0 (tension, cm), mean_k (cm/s and cm/day); 5 columns, 19 rows.
- (3) Hyprop_K.csv: Lab-measured unsaturated hydraulic conductivity via HYPROP; 18 columns, 45 rows; includes suction and conductivity per plot (Plot1–Plot9 with corresponding treatments).
- (4) Hyprop_SWRC.csv: HYPROP soil water release curves; 11 columns, 501 rows; includes Interpolation_number and VWC (per plot) across suction points.
- (5) WP4_SWRC.csv: WP4 soil water release curves; 4 columns, 60 rows; includes Temperature, Soil moisture (m3/m3), Matric potential (MPa), and Pressure head (cm of water).
- Interpolation to a common suction grid facilitated by spline fitting; data interpreted with HYPROP-FIT and related manuals.

## Processing, QA, and Documentation
- Raw data visually inspected as part of QA/QC.
- Data not infilled beyond NA placeholders; interpolations performed to enable cross-dataset comparisons.
- Supporting documentation and manuals included (HYPROP, HYPROP-FIT, minidisk, WP4) for methods and data processing steps.

## Usage and Applications
- Enables analysis of how drought and warming influence soil hydraulic properties and soil moisture dynamics.
- Supports cross-dataset integration for dashboards, self-service exploration, or reports, with consistent plot-level and treatment metadata.
- Related publications available: Domínguez et al. (2015); Reinsch et al. (2016a,b); Robinson et al. (2016).

## Roles and Responsibilities
- D.A. Robinson: HYPROP measurements and SWRCs.
- I. Lebron: HYPROP measurements, SWRCs, and bulk density.
- A.R. Smith: WP4 measurements.
- M.R. Marshall: Minidisk measurements.
- B.A. Emmett: Principal investigator.
- S. Reinsch: Field site science management.
- D.M. Cooper: Statistical interpolation in R.
- M. Brooks: Field site and roof maintenance.