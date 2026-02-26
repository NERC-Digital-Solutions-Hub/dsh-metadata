# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- Dataset of soil hydraulic measurements from the Climoor field site in Clocaenog Forest, North Wales, collected 2010–2012.
- Comprises five data sets:
  - 1) Bulk density (0–5 cm) and saturated water content
  - 2) Unsaturated hydraulic conductivity measured in the field with a mini disk infiltrometer at tensions of -2 and -6 cm
  - 3) Unsaturated hydraulic conductivity measured in the laboratory using HYPROP on soil cores
  - 4) Soil water release curves (SWRC) for wet soil from HYPROP measurements
  - 5) SWRC data for dry soil measured with a WP4 potentiometer
- Data are quality checked, with incorrect or missing values removed; data are not infilled, and NA values are used where data are lacking.
- Data collection ran from late 2010 to early 2012, supporting questions on warming and drought effects on ecosystem processes.

## Field site and experimental design
- Location: Clocaenog Forest, North Wales; upland Atlantic heathland dominated by Calluna vulgaris.
- Climate manipulation:
  - Drought: retractable roofs over plots May–September to reduce rainfall by ~20%.
  - Warming: retractable night curtains (aluminium mesh) that reduce heat loss by ~64% and indirectly reduce rainfall input; roof operation paused in high winds.
  - Three replicated plots per treatment and three control plots (4 × 5 m each).
- Soil and environment:
  - Podzolic organo-mineral soils with a shallow organic horizon.
  - Site features automated monitoring equipment including meteorological sensors.
- Sampling and plots:
  - HYPROP cores collected from the eastern edge of plots; samples taken under heather away from prevailing wind/rain.
  - Treatments: drought, warming, control; sampling times include 2011 April and September, 2011 (HYPROP), 2012 May (Minidisk), 2010 November (WP4 SWRC).

## Data collection methods and processing
- Datasets and measurement approaches:
  - 1) Bulk density: oven-dried mass (105°C, 16 h) divided by core volume; 0–5 cm depth.
  - 2) Minidisk infiltrometer: field measurements at -2 cm and -6 cm tension; data converted to hydraulic conductivity using standard minidisk procedures.
  - 3) HYPROP: laboratory measurements on 250 cm³ soil cores to determine unsaturated conductivity; data interpreted with HYPROP-FIT software.
  - 4) HYPROP SWRC: soil water release curves from HYPROP; raw data interpolated to regular suction values using spline fitting in R.
  - 5) WP4 SWRC: SWRC data for dry soil using WP4 potentiometer; measurements described by WP4 manual.
- Processing and QA:
  - HYPROP data processed with HYPROP-FIT; spline interpolation in R to align suction points.
  - Visual QA performed; no infilling of data; incomplete or missing values represented as NA when appropriate.
- Field and lab workflow:
  - Sample collection, core preparation, and laboratory analysis conducted by experienced soil scientists.
  - Supporting manuals and documentation included for all instruments and methods.

## Data structure and content
- Data files (CSV) and their contents:
  - (1) Bulk_density.csv: Bulk density (g/cm³) and related metadata; 6 columns, 10 rows described (plot, treatment, etc.).
  - (2) Minidisk_K.csv: Unsaturated hydraulic conductivity measured in the field; columns include plot, treatment, suction (cm), mean_k (cm/s or cm/day) and comments; 5 columns, 19 rows.
  - (3) Hyprop_K.csv: Unsaturated hydraulic conductivity measured via HYPROP in the laboratory; 18 columns, 45 rows; multiple plots with warming, control, drought designations.
  - (4) Hyprop_SWRC.csv: Soil water release curve data from HYPROP; 11 columns, 501 rows; includes interpolation number and suction (kPa) with corresponding VWC values for each plot.
  - (5) WP4_SWRC.csv: SWRC data from WP4 potentiometer method; 4 columns, 60 rows; includes temperature, soil moisture, matric potential, and related measurements.
- Key metadata elements:
  - Plot-level identifiers, treatment type (control, drought, warming), and measurement-specific variables (e.g., h0, suction, k, VWC, SWRC values).
  - Interpolation data points and units clearly indicated for SWRC datasets.
- Roles and responsibilities:
  - D.A. Robinson: HYPROP measurements and SWRC data
  - I. Lebron: HYPROP measurements, SWRC, and bulk density
  - A.R. Smith: WP4 measurements
  - M.R. Marshall: Minidisk measurements
  - B.A. Emmett: Principal investigator, Clocaenog field site
  - S. Reinsch: Field site science manager
  - D.M. Cooper: Statistical interpolation in R
  - M. Brooks: Field site and roof maintenance
- References to related work:
  - Domínguez et al. 2015; Robinson et al. 2016; Sowerby et al. 2008; Domínguez et al. 2015; and other site-related publications.

## Data quality, provenance and governance
- Quality assurance:
  - Data visually inspected as part of QA/QC procedures.
  - Interpolations and software tools (HYPROP-FIT, R spline fitting) documented in supporting materials.
- Data provenance:
  - Detailed description of collection methods, instrument usage, and sample handling to ensure traceability.
  - Publications and data centre references provided for broader data reuse and verification.
- Accessibility and sharing:
  - Supporting documentation and datasets are referenced, with links to journal articles and data centre records for reproducibility.
  - Data designed to support monitoring and policy-relevant analyses of drought and warming effects on soil hydraulic properties.

## Implications for monitoring frameworks
- The dataset exemplifies integration of climate manipulation with comprehensive soil hydraulic monitoring, enabling assessment of policy-relevant environmental health measures like soil moisture dynamics under drought and warming.
- Provides a multi-method approach (field and laboratory measurements) with standardized processing (HYPROP-FIT, spline interpolation) to support comparability and reproducibility across monitoring programs.
- Highlights data governance considerations relevant to monitoring teams:
  - Need for clear metadata, documentation, and interoperability between instruments.
  - Transparency about QA/QC procedures and handling of missing data.
  - Role clarity and data provenance to ensure traceable data lineage and responsible sharing.