# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

## Overview
- Dataset of soil hydraulic measurement data from the Climoor field site in Clocaenog Forest, North Wales, collected 2010–2012.
- Aims to support understanding of how warming and drought affect ecosystem processes.
- Five data sets capturing key soil hydraulic properties across experimental plots with drought, warming, and control treatments.
- Quality-assured data with no infilling; missing values marked as NA; raw data interpolated where needed for analysis.
- Data processing and interpretation involved HYPROP software, spline interpolation in R, and standard manuals for instruments.

## Data Sets and Content
- Data set 1: Bulk density (0–5 cm) and saturated water content (SatVWC)  
  - File: Bulk_density.csv  
  - Contents: Dry bulk density (g/cm3) and related soil properties; 6 columns, 10 rows (Plot, Treatment, BD, SatVWC, FofS, EstPD, etc.).
- Data set 2: Unsaturated hydraulic conductivity (minidisk infiltrometer) in the field  
  - File: Minidisk_K.csv  
  - Contents: Measurements at tensions of -2 cm and -6 cm; fields include Plot, Treatment, h0 (cm), mean_k (cm/s and cm/day); 5 columns, 19 rows.
- Data set 3: Unsaturated hydraulic conductivity (HYPROP) in the laboratory  
  - File: Hyprop_K.csv  
  - Contents: HYPROP-derived unsaturated hydraulic conductivity across multiple plots; 18 columns, 45 rows; paired suction and conductivity data per plot.
- Data set 4: Soil water release curves (SWRC) from HYPROP measurements  
  - File: Hyprop_SWRC.csv  
  - Contents: Interpolated SWRC data (kPa, VWC) across plots; 11 columns, 501 rows; interpolation numbers included.
- Data set 5: Soil water release curves (WP4 potentiometer method) for dry soil  
  - File: WP4_SWRC.csv  
  - Contents: SWRC data using WP4; 4 columns, 60 rows; includes temperature, soil moisture, matric potential, and pressure head.

## Data Structure and Metadata
- Detailed structure provided for each file, including:
  - (1) Bulk_density.csv: Plot, Treatment, BD (g/cm3), SatVWC, FofS, EstPD, etc. 6 columns, 10 rows.
  - (2) Minidisk_K.csv: Plot, Treatment, h0 (cm), mean_k (cm/s), mean_k (cm/day). 5 columns, 19 rows.
  - (3) Hyprop_K.csv: Suction (kPa) and Unsaturated_hydraulic_conductivity (cm/day) for Plot1–Plot9 across treatment types. 18 columns, 45 rows.
  - (4) Hyprop_SWRC.csv: Interpolation_number, Suction (kPa), VWC (m3/m3) for plots; 11 columns, 501 rows.
  - (5) WP4_SWRC.csv: Temperature (°C), Soil moisture (m3/m3), Matric potential (MPa), Pressure head (cm of water). 4 columns, 60 rows.
- Data processing notes:
  - HYPROP data analyzed with HYPROP-FIT software.
  - Water release curves interpolated onto a regular suction grid using spline fitting in R.
  - Minidisk data converted to hydraulic conductivity using standard procedures.
  - Bulk density derived from oven-dried mass (105°C) and sample volume; samples were moss-free and taken from 0–5 cm depth.

## Field Site and Experimental Design
- Location: Clocaenog Forest, North Wales; upland Atlantic heathland dominated by Calluna vulgaris.
- Experimental setup: Drought and warming treatments, each with three replicated plots (4 m × 5 m) plus three control plots with scaffolding to mirror shading effects.
- Treatments:
  - Drought: Retractable roofs exclude rainfall May–September, reducing annual rainfall by ~20%.
  - Warming: Retractable aluminum mesh curtains reduce nocturnal heat loss (infrared reflection 96–97%), with a slight rainfall exclusion effect (~14% annual rainfall reduction); curtains do not operate in winds >10 m/s.
- Measurements focus on soil hydraulic properties (bulk density, SWRC, and hydraulic conductivity) across plots, collected from topsoil (0–5 cm) and cores under heather, with HYPROP cores sampled from plot edges away from wind/rain effects.

## Data Quality, Access, and Documentation
- QA/QC: Data visually inspected; incorrect or missing values removed; no data infilling performed; NA values used where data are absent.
- Documentation and methods:
  - Instrument manuals and supporting documents included (HYPROP, minidisk, WP4).
  - Data interpretation and interpolation procedures referenced to HYPROP-FIT and R-based methods.
  - Key publications and data centre references cited (e.g., Domínguez et al. 2015; Robinson et al. 2016; Reinsch et al. 2016a,b).
- Roles:
  - D.A. Robinson, I. Lebron, A.R. Smith, M.R. Marshall, B.A. Emmett, S. Reinsch, D.M. Cooper, M. Brooks contributed to measurements, processing, statistics, field site management, and data interpretation.

## Potential Uses and Relevance for Data Leaders
- Provides a complete, quality-controlled set of soil hydraulic properties across climate treatment plots for understanding drought and warming impacts on soil processes.
- Useful for:
  - System-wide data planning and integration in soil and ecosystem models.
  - Assessing data gaps, standards, and metadata needs for cross-site harmonization.
  - Coordinating ancillary datasets (meteorology, soil properties) to support broader data ecosystems and communities of practice.
- Clear metadata, instrument provenance, and processing steps support data discoverability, reproducibility, and reuse within inter-organizational networks.