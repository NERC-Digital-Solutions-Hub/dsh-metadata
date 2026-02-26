# Physical and geochemical properties of saltmarsh soils produced from 462 narrow diameter gouge cores spanning 22 UK saltmarshes collected between 2018-2021

## Overview
- Dataset describing physical and geochemical properties of saltmarsh soils.
- Derived from 462 narrow-diameter gouge cores across 22 UK saltmarshes, collected 2018–2021.
- Used to calculate organic carbon soil stocks across UK saltmarsh ecosystems.

## Data scope
- Data resource: Physical_geochemical_properties_narrow_cores.csv.
- Key variables:
  - Core_ID, Saltmarsh, Marsh_type, Marsh_zone (Low/LH), Nation (Scotland, Wales, England), Collection_year.
  - Spatial identifiers: Lat_dec_deg, Long_dec_deg (WGS84), X_easting, Y_northing.
  - Elevation_above_OD_m, Sample_depth_cm, Mid_Point_depth_cm.
  - Substrate (Troels-Smith classification), Wet_bulk_density_g_cm3, Dry_bulk_density_g_cm3, OC_perc (organic carbon content %).
- Sub-sampling: 3434 sub-samples at 10 cm resolution within cores.

## Spatial data
- Coordinates provided in both geographic (lat/long, WGS84) and projected (X_easting, Y_northing) formats.
- DGPS used to record sample-site locations.
- Elevation given as meters above ordnance datum (OD).

## Variables and measurements
- Substrate: Troels-Smith classification.
- Densities: Wet and Dry bulk density (g/cm3).
- Organic carbon content: OC_perc (% by weight).
- Sampling framework: 462 cores from 22 saltmarshes; 10 cm sub-sample resolution.

## Methods and quality control
- Field sampling: 30 mm gouge cores; samples collected from 22 UK saltmarshes.
- Laboratory processing: Samples dried at 60°C for 72 hours; milled to fine powder.
- Carbon quantification: 50 mg subsamples analyzed with Elementar Soli TOC using temperature gradient method; calibrated with CaCO3 and standard references.
- QA/QC: Equipment calibrated per University of St Andrews practices; lab procedures aligned with referenced standards and prior work.

## Data format and access
- File format: CSV.
- Data resource description includes explicit field types (text vs numeric) and unit conventions.
- Location and depth data structured to support GIS mapping and calculation of soil organic carbon stocks.

## Provenance and references
- Funding: NERC (NE/R010846/1).
- Research team includes multiple universities (St Andrews, Glasgow, York, Leeds, Bangor, CEH).
- Relevant methodological references: Troels-Smith (1955), Dadey et al. (1992), DIN 19539 (2015), Natali et al. (2020), Smeaton et al. (2021).