# Nitrous oxide fluxes from an intensively managed grazed grassland in Scotland

## Overview
- Investigates fluxes of N2O from two adjacent grassland fields in Easter Bush, Scotland, before and after a tillage event on 1 May 2012.
- Study site details: temperate maritime climate, ~921 mm annual rainfall, ~9°C average temperature; two ~5.4 ha fields with long-term intensive livestock production.
- Focus on comparing tilled (South) vs. un-tilled (North) management and associated N2O emissions using high-resolution flux measurements.

## Study site and management
- Location: Easter Bush, Scotland (55° 51' 55.30"N, 3° 12' 22.17"W).
- Field characteristics: clay loam soils (top 30 cm 52/20/28 vs 57/19/24 texture); pH ~5.1; imperfectly drained Macmerry soil; drainage system present but functioning poorly, causing surface water in wet periods.
- Field setup: two fields (~5.4 ha each), historically grazed by sheep; similar stocking densities (~0.7 LSU ha⁻¹) and N fertiliser inputs (~200 kg N ha⁻¹ y⁻¹).
- Management contrast:
  - North (un-tilled): grazed continuously by about 30 sheep ha⁻¹; fertilisation with two 70 kg N ha⁻¹ applications (28 May and 9 Aug 2012).
  - South (tilled): tilled on 1 May 2012 (ploughed to 30 cm), harrowed, seeded with ryegrass; glycophosphate pre-tilage; fertilisation with a single 70 kg N ha⁻¹ application on 9 Aug 2012.

## Experimental design and data collection
- Tillage event and timeline:
  - 16 Feb 2012: tilled vs. un-tilled fields prepared.
  - 27 Apr 2012: glyphosate applied to tilled field.
  - 1 May 2012: tillage (South) performed; un-tilled field grazed as usual.
  - 3 May 2012: tilled field harrowed, seeded, rolled.
  - 28 May 2012: 70 kg N ha⁻¹ applied to un-tilled field; tilled field received no May N application.
  - 9 Aug 2012: 70 kg N ha⁻¹ applied to both fields (tilled and un-tilled).
  - 19 Sep 2012: grazing continued on both fields.
- Measurement systems:
  - Eddy covariance setup installed 27 Mar 2012 at field boundary.
  - 3-axis ultrasonic anemometer (WindMaster Pro) at 2.4 m; 10 Hz wind measurements.
  - N2O, H2O, CO2 measured with a quantum cascade laser analyser (QCL) via a 13 m inlet line; sampling ~13 L/min.
  - Flux computation: half-hourly, using covariance between N2O concentration fluctuations and vertical wind speed.
  - Data processing: double coordinate rotation, spike removal, block averaging, time lag removal by covariance maximisation; frequency response and density corrections (Moncrieff et al. 1997; Burba et al. 2012); quality control (Foken et al. 2005).
  - Field attribution: winds between 180–270° assigned to tilled field; winds between 330–100° assigned to un-tilled field; data outside these ranges discarded due to cabin/fence obstruction.
- Chamber measurements:
  - Static chambers: PVC cylinders, 38 cm I.D., 22 cm height; inserted 5 cm into soil; 40 min closures; three samples (0, 20, 40 min); gas analysed by GC-ECD; ten chambers per field; occasional relocation to minimize microclimate bias.
  - Dynamic chambers: 39 cm I.D., 22 cm height; closed system connected to QCL via tubing; ~15 m chamber-to-instrument distance; ~6–7 L/min flow; ~22 s lag; fluxes derived from 1 Hz data over 3 minutes using linear and non-linear (asymptotic) regression; best-fit method chosen per measurement.
  - Detection limits: static chamber flux detection ~0.4 nmol m⁻² s⁻¹; dynamic chamber ~0.04 nmol m⁻² s⁻¹.
- Footprint and footprint consistency: chamber measurements distributed to align with the eddy covariance flux footprint (10–200 m from mast); chambers occasionally moved to avoid microclimate bias.

## Data processing and quality control
- Eddy covariance:
  - Corrections for high/low-frequency losses, density fluctuations, and time-lag via established methodologies.
  - Data quality filtering using Foken et al. (2005) scheme; poor-quality data removed (category 2).
- Field attribution:
  - Wind-direction-based separation of flux data to corresponding fields; data outside defined directional bins excluded due to measurement geometry.
- Chamber data:
  - Flux calculations per standard equations for static and dynamic chambers; cross-method validation between static and dynamic approaches.

## Data files and schema
- Easter_Bush_EddyC_Tillage_2012:
  - Contains time-series fields including tau, H (sensible heat), LE (latent heat), co2_flux, h2o_flux, n2o_flux, wind_speed, wind_dir, u*, TKE, L, (z-d)/L, bowen_ratio, and related metadata.
- Easter_Bush_Chambers_Tillage_2012:
  - Records per chamber with location, field name, method, date, flux (nmol N2O m⁻² s⁻¹), time, air temperature, soil/wetness measures, atmospheric pressure, PAR, rainfall, etc.
- File: Easter_Bush_Chambers_Tillage_2012:
  - Tabular structure detailing Chamber-specific measurements (Location, Field, Method, Date, Flux, Air Temp, Soil Temp, Rainfall, etc.).

## Relevance for GIS Specialists
- Spatial context:
  - Two clearly defined fields with precise coordinates and boundaries; delineation of tilled vs. un-tilled areas for spatial analysis.
  - Measurement infrastructure geolocated (mast, chambers) enabling integration with GIS layers (topography, drainage, soil type, land use, management history).
- Temporal richness:
  - High-resolution half-hourly flux data with explicit tillage and fertilization events; enables time-series mapping and change detection around management interventions.
- Data integration:
  - Combines eddy covariance footprints with ground-based chamber measurements; supports cross-validation and spatial extrapolation of fluxes.
  - Compatible with soil, climate, and management layers to assess drivers of N2O fluxes in a GIS-enabled workflow.
- Data quality and provenance:
  - Detailed processing steps and QC criteria documented; traceable to established methodologies and references, aiding reproducibility and audit trails in geospatial analyses.