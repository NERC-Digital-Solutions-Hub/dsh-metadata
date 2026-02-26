# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- Dataset of soil hydraulic measurements from the Climoor field site, Clocaenog Forest, North Wales.
- Contains five data sets focusing on bulk density, saturated water content, unsaturated hydraulic conductivity (field mini-disk and HYPROP laboratory methods), and soil water release curves for both wet and dry soil.
- Data collected 2010–2012 to study effects of warming and drought on ecosystem processes; data prepared for site-specific soil property monitoring at a reference time.
- Quality controlled: incorrect/missing values removed; no infilling; NAs added where data are unavailable.

## Data Sets and Measurements
- Data set 1: Soil bulk density (0–5 cm) and saturated water content.
- Data set 2: Unsaturated hydraulic conductivity measured in the field with a mini-disk infiltrometer at tensions of -2 and -6 cm.
- Data set 3: HYPROP laboratory measurements of unsaturated hydraulic conductivity on soil cores.
- Data set 4: Soil water release curves for wet soil from HYPROP measurements (laboratory).
- Data set 5: Soil water release curves for dry soil measured with a WP4 potentiometer (laboratory).

## Site Description and Experimental Treatments
- Location: Clocaenog Forest, upland Atlantic heathland ecosystem.
- Treatments: drought, warming, and control (three replicate plots per treatment).
- Drought: retractable roof excludes rain May–September; ~20% reduction in rainfall on average, with some rain events missed by sensor limits.
- Warming: retractable aluminum mesh curtains over plots at night; reflects infrared radiation to reduce heat loss; approximately 14% reduction in annual rainfall due to rain interception.
- Wind restrictions: curtains do not operate in winds > 10 m s-1.
- Plot layout: 3 drought roofs, 3 warming roofs, 3 control plots (4 × 5 m each).

## Data Collection and Timeline
- HYPROP measurements (250 cm³ cores, 0–5 cm depth) collected in 2011 (April and September) for wet soil; cores taken from eastern plot edges away from prevailing winds.
- HYPROP data processing: spline interpolation in R to align data onto common suction values; HYPROP-FIT software used for analysis.
- Minidisk infiltrometer measurements: field measurements at two tensions (-2 cm and -6 cm) in May 2012.
- WP4WP4 potentiometer measurements: dry soil water release curve data collected November 2010.
- Processing notes: bulk density calculated from oven-dried mass (105°C, 16 h) and sample volume; no stones present (fully organic soils).

## Data Structure and Contents
- (1) Bulk_density.csv: dry bulk density and related metadata (plot, treatment, soil properties).
- (2) Minidisk_K.csv: field-measured unsaturated hydraulic conductivity at -2 and -6 cm; includes plot, treatment, tension, and mean k values (cm/s and cm/day).
- (3) Hyprop_K.csv: HYPROP-derived unsaturated hydraulic conductivity data by plot and treatment; multiple suction points per plot.
- (4) Hyprop_SWRC.csv: HYPROP soil water release curves (wet soil) with interpolation points across suction values; includes VWC measurements per plot.
- (5) WP4_SWRC.csv: WP4 soil water release curves (dry soil) with matric potential and moisture data; includes temperature and related fields.

## Processing, Quality Assurance, and Documentation
- QA/QC performed by experienced soil scientists; data visually checked with basic graphs.
- HYPROP data processed with HYPROP-FIT; spline interpolation in R to standard suction values.
- Minidisk data converted to hydraulic conductivity using standard procedures.
- WP4 measurements documented with operator manuals; supporting documentation and manuals included.
- Data interpretation supported by published references (Domínguez et al. 2015; Robinson et al. 2016; Dominguez et al. 2015; Sowerby et al. 2008; Reinsch et al. 2016).

## Data Provenance and Roles
- D.A. Robinson: HYPROP measurements and soil water release curves.
- I. Lebron: HYPROP measurements, HYPROP SWRCs, and bulk density.
- A.R. Smith: WP4 measurements.
- M.R. Marshall: Minidisk measurements.
- B.A. Emmett: Principal investigator; site framework.
- S. Reinsch: Field site science management.
- D.M. Cooper: Statistical interpolation in R.
- M. Brooks: Field site and roof maintenance.

## Potential Uses and Considerations for Analysis
- Correlate soil hydraulic properties (bulk density, saturated water content) with unsaturated conductivity and water release curves across drought/warming/control treatments.
- Investigate treatment effects on soil moisture retention and hydraulic conductivity at different suctions (wet vs. dry soil).
- Integrate with site meteorological data to model soil-water dynamics under climate-change scenarios.
- Consider local-scale data accessibility and standardization challenges typical of multi-method soil datasets; note the dataset emphasizes carefully documented methods and provenance to facilitate reproducibility.