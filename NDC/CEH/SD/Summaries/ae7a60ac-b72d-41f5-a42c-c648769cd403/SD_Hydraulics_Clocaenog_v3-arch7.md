# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Abstract
- Dataset of soil hydraulic measurements from the Climoor field site, Clocaenog forest, North Wales.
- Comprises five data sets: (1) soil bulk density (0–5 cm) and saturated water content; (2) field unsaturated hydraulic conductivity via minidisk at tensions -2 and -6 cm; (3) HYPROP-based unsaturated hydraulic conductivity on field cores; (4) soil water release curves for wet soil from HYPROP; (5) soil water release curves for dry soil from WP4 potentiometer.
- Quality checked; incorrect/missing values removed; data not infilled; NA values added where data are missing.
- Collected 2010–2012; aims to monitor site-specific soil properties at a reference time and to inform on warming and drought effects on ecosystem processes.

## Field site and climate treatments
- Clocaenog climate change field site: upland Atlantic heathland dominated by Calluna vulgaris; long-running drought and warming experiments with three replicate plots per treatment plus controls.
- Drought treatment: automated retractable roofs over plots May–September, reducing rainfall by ~20% (and up to ~80% of rainfall excluded due to detection limits).
- Warming treatment: automated aluminum curtains at night; reflect infrared radiation to reduce heat loss; curtains retract during rain to limit rainfall exclusion (ca. 14% annual rainfall reduction); operation halted in winds >10 m s^-1.
- Plot layout: 3 drought roofs, 3 warming roofs, 3 control plots; samples collected toward plot edges to minimize environmental interference.

## Data collection and processing
- HYPROP: used to obtain water release curves and hydraulic conductivity from 250 cm³ soil cores (0–5 cm depth); data interpolated to a standard suction range with spline fitting in R; HYPROP-FIT software used for analysis.
- Minidisk infiltrometer: field measurements at -2 cm and -6 cm tensions; results converted to hydraulic conductivity using standard minidisk methodology.
- WP4 potentiometer: laboratory measurement of dry soil water release curves; samples from control plots (November 2010).
- Bulk density: oven-dry method (105°C, 16 h); bulk density computed from dry mass and ring volume.
- Data organization: five CSV files with accompanying supporting documentation and manuals; quality assurance included.

## Data files overview
- (1) Bulk_density.csv: dry bulk density, plot, treatment, SatVWC, FofS, EstPD, etc.
- (2) Minidisk_K.csv: field unsaturated hydraulic conductivity; columns include plot, treatment, tension (h0_cm), mean_k_cm_per_s, and mean_k_cm_per_day; 19 rows.
- (3) Hyprop_K.csv: laboratory-measured unsaturated hydraulic conductivity; per plot and treatment across multiple plots; 45 rows, 18 columns.
- (4) Hyprop_SWRC.csv: HYPROP soil water release curves; interpolation numbers and VWC values for multiple plots; 501 rows, 11 columns.
- (5) WP4_SWRC.csv: WP4 soil water release curves; includes temperature, soil moisture, matric potential, and pressure head; 60 rows, 4 columns.

## Provenance and authorship
- Roles: D.A. Robinson (HYPROP measurements and SWRCs), I. Lebron (HYPROP, SWRCs, bulk density), A.R. Smith (WP4), M.R. Marshall (minidisk), B.A. Emmett (PI, Clocaenog site), S. Reinsch (field site science management), D.M. Cooper (statistical interpolation in R), M. Brooks (field site and roof maintenance).
- Context and references: Domínguez et al. (2015); Reinsch et al. (2016a, 2016b); Robinson et al. (2016); Sowerby et al. (2008); supporting documentation with manuals.

## Spatial and GIS relevance
- Location: Clocaenog Forest, North Wales (56°23′N, 10°57′W).
- Data enable GIS-based mapping and analysis of soil hydraulic properties (bulk density, saturated water content, unsaturated hydraulic conductivity, and water release curves) across drought, warming, and control plots.
- Suitable for integrating with climate, meteorological, and vegetation data to visualize spatial patterns and treatment effects on soil hydraulic properties at shallow depths (0–5 cm).

## Usage notes and caveats
- Timeframe: data collected between 2010 and 2012; sampling months specified per data type.
- Data integrity: quality-checked; no data infilling; NA values used where data are unavailable.
- Processing details: HYPROP data interpolated to common suction levels; minidisk and WP4 conversions follow standard manuals included in the package.
- Experimental caveats: rainfall exclusion under drought and warming is subject to sensor limits and wind restrictions; sampling focused on topsoil (0–5 cm) with cores taken from plot edges to minimize bias.