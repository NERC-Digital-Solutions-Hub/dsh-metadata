# Physical_geochemical_properties_narrow_cores.csv

## Overview
- Dataset of physical and geochemical properties of saltmarsh soils from 462 narrow-diameter gouge cores collected across 22 UK saltmarshes between 2018 and 2021.
- Intended to support calculation of organic carbon soil stocks across UK saltmarsh ecosystems.

## What is included
- Core and sub-sample data:
  - 462 cores collected using 30 mm gouge corers; 3434 sub-samples at 10 cm resolution.
  - Core descriptions follow Troels-Smith classification; samples analyzed for organic carbon content.
- Measured variables (per core/sub-sample):
  - Location and positioning: Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_above_OD_m.
  - Spatial and site descriptors: Saltmarsh, Marsh_type, Marsh_zone (Low/High), Nation (Scotland/Wales/England).
  - Sampling details: Collection_year, Sample_depth_cm, Mid_Point_depth_cm.
  - Physical properties: Wet_bulk_density_g_cm3, Dry_bulk_density_g_cm3.
  - Chemical property: OC_perc (Organic carbon content %).
- Data resource file: Physical_geochemical_properties_narrow_cores.csv (CSV format).

## Geographical coverage
- United Kingdom saltmarsh sites, distributed to represent coastal variability across Scotland, England, and Wales.
- Sites documented with precise geospatial coordinates (WGS84) and corresponding easting/northing values.

## Methods and QA
- Sampling: 462 cores from 22 UK saltmarshes using a 30 mm gouge corer; subsamples collected at 10 cm increments.
- In-field descriptions: Core descriptions recorded using Troels-Smith classification; DGPS used for precise locations.
- Sample processing: Samples frozen at -20°C; weighed before/after drying at 60°C for bulk density calculations; milled to a fine powder.
- Carbon quantification: 50 mg subsamples analyzed with Elementar Soli TOC using a temperature gradient method (DIN 19539; Natali et al., 2020; Smeaton et al., 2021).
- Calibration: Soli TOC calibrated with CaCO3 and Silty soil TOC/ROC/TIC standards.
- Quality control: Laboratory equipment calibrated per University of St Andrews practices; data checked for consistency with standard references.

## Data structure and formats
- Primary data file: Physical_geochemical_properties_narrow_cores.csv
- Key columns (example):
  - Core_ID, Saltmarsh, Marsh_type, Marsh_zone, Nation, Collection_year
  - Lat_dec_deg, Long_dec_deg, X_easting, Y_northing
  - Elevation_above_OD__m, Sample_depth_cm, Mid_Point_depth_cm
  - Substrate, Wet_bulk_density_g_cm_3, Dry_bulk_density_g_cm_3, OC_perc

## Data quality and provenance
- Data collection and analysis procedures are documented with references to methodological standards and calibration procedures.
- Where applicable, data fields are provided with clear formats (text or numeric) and units.
- Some fields may be NA where data were not applicable or not collected.

## Potential uses for data support and exploration
- Build self-serve data products (dashboards, pivot tables) to compare organic carbon stocks across marsh zones, marsh types, and nations.
- Integrate with regional hydrology, elevation models, or other soil datasets to model carbon stock distribution in UK saltmarshes.
- Facilitate quality-controlled data cleaning, transformation, and aggregation for policy or research use.
- Support meta-analyses or comparative studies of saltmarsh organic carbon content and sediment properties across sites.