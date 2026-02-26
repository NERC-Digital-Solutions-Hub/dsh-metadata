# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- Dataset of soil hydraulic measurements from the Climoor field site, Clocaenog Forest, North Wales (2010–2012).
- Comprises five data sets:
  - (1) Bulk density (0–5 cm) and saturated water content.
  - (2) Field unsaturated hydraulic conductivity using a mini disk infiltrometer at tensions of -2 and -6 cm.
  - (3) Laboratory unsaturated hydraulic conductivity using HYPROP on field-core samples.
  - (4) Soil water release curves for wet soil from HYPROP measurements (laboratory).
  - (5) Soil water release curves for dry soil measured with a WP4 potentiometer.
- Quality assurance: data have been quality checked; incorrect/missing values removed; data not infilled; NA values added where data are missing.
- Data collection window: end of 2010 to early 2012; datasets 1, 3, 4 collected Apr and Sept 2011; dataset 2 in May 2012; dataset 5 in Nov 2010.
- Purpose: investigate effects of warming and drought on ecosystem processes; data reflect site-specific soil properties at defined reference times.

## Data content and structuring
- Five CSV data files:
  - (1) Bulk_density.csv — dry bulk density, bulk density across plots and treatments.
  - (2) Minidisk_K.csv — field-measured unsaturated hydraulic conductivity at -2 cm and -6 cm tension; includes units and plot/treatment information; provides mean_k values (cm/s and cm/day) and notes on tension and treatment.
  - (3) Hyprop_K.csv — lab-measured unsaturated hydraulic conductivity via HYPROP; includes suction values and corresponding conductivity for each plot (warming, control, drought) across multiple plots.
  - (4) Hyprop_SWRC.csv — HYPROP-derived soil water release curves (SWRC) with interpolation numbers (1–500) and VWC at various plotted suctions.
  - (5) WP4_SWRC.csv — WP4-potentiometer SWRC data for dry soil; includes temperature, volumetric moisture content, matric potential, and pressure head.
- Each file includes clear column headers and unit definitions; data are aligned to plots and treatment types (control, drought, warming).
- Data processing notes:
  - HYPROP data analyzed with HYPROP-FIT software; SWRC data interpolated to a common suction scale using spline fitting in R.
  - Minidisk measurements converted to hydraulic conductivity following standard manuals.
  - Bulk density derived from oven-dried mass (105°C, 16 h) divided by sample volume; no stones in samples.

## Methods and processing
- Field methods:
  - HYPROP: soil cores (250 cm³) from 0–5 cm depth; laboratory evaporation method used to determine SWRC and unsaturated conductivity.
  - Minidisk infiltrometer: field measurements at -2 and -6 cm tensions.
  - WP4 potentiometer: dry soil SWRC measurements in the laboratory.
- Sample handling:
  - Samples collected from plots across drought, warming, and control treatments; cores collected away from wind and rain influence (eastern edge) to minimize bias.
  - Moss-free samples collected under heather; sampling locations noted (e.g., squares G7, G8 near rain gauge funnel).
- Site-scale information:
  - Clocaenog climate change site features fully automated drought and warming treatments using roof and curtain systems; rainfall reduction ~20% for drought periods; warming reduces night-time heat loss via reflective curtains; operations paused in high winds.

## Field site and treatments
- Location: Clocaenog Forest, North East Wales; upland Atlantic heathland dominated by Calluna vulgaris.
- Treatments:
  - Drought: three replicated plots, May–Sept annually, roof excludes rainfall, reducing annual rainfall by ~20% during active period.
  - Warming: three replicated plots, night-time curtains reduce infrared heat loss; rain sensor triggers retraction to minimize rainfall loss; annual rainfall reduction ~14% on average.
  - Controls: three plots with scaffolding to mirror shading effects of experimental structures.
- Plot layout: 3 drought, 3 warming, 3 control plots (4 m × 5 m each).

## Provenance, quality, and governance
- Personnel and roles:
  - D.A. Robinson, I. Lebron, A.R. Smith, M.R. Marshall, B.A. Emmett, S. Reinsch, D.M. Cooper, M. Brooks – responsible for data collection, processing, statistical interpolation, and field site management.
  - Specific responsibilities include HYPROP measurements, SWRC generation, bulk density, minidisk measurements, WP4 measurements, and site operations.
- Documentation and references:
  - Supporting documentation and manuals referenced (HYPROP, Minidisk, WP4; HYPROP-FIT) accompany the dataset.
  - Related publications and data center records cited (Domínguez et al. 2015; Reinsch et al. 2016a–b; Robinson et al. 2016).
- Data integrity:
  - Data visually inspected as part of QA/QC; no data infilling beyond NA imputation where data are missing.
  - Data are intended as site-specific measurements at defined reference times; interpolation and processing documented to enable reproducibility.

## Access, documentation, and references
- Data are complemented by extensive supporting materials and manuals included with the dataset.
- Related datasets and publications provide context and use cases:
  - Domínguez et al. 2015; Reinsch et al. 2016 (daily meteorological and AWS data); Robinson et al. 2016; Sowerby et al. 2008.
- Keywords: soil water release, hydraulic conductivity, Clocaenog, HYPROP, bulk density, infiltrometer.

## Practical notes for data stewards
- Scope and context:
  - The dataset is a snapshot focusing on specific time points (2010–2012) and measured properties; consider longitudinal integration with ongoing or future measurements for trend analysis.
- Metadata and discoverability:
  - Ensure cross-linking with supporting documentation (manuals, site documentation) and associated publications.
  - Maintain clear mapping of plots, treatments, and sampling times to enable reproducibility and meta-analyses.
- Data quality and caveats:
  - Acknowledge potential biases due to sampling location (e.g., eastern edge sampling) and treatment dynamics (roof operation lag, wind constraints).
  - Note that some rainfall exclusion and measurement timing nuances may affect comparability across plots and treatments.
- Licensing and reuse:
  - Cite primary sources and data creators; reference associated DOIs and publications when reusing.
- Long-term stewardship:
  - Preserve CSV data files alongside full methodological documentation, processing scripts (HYPROP-FIT, R spline interpolation), and manuals to support reuse and validation.