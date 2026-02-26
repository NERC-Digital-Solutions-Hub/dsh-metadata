# Manual n°3

## Overview
- Aimed at soil and plant dynamics research; LRI (Laboratoire des RadioIsotopes), University of Antananarivo, conducts physico-chemical analyses at national scale.
- Produces datasets on soil properties (SOC, texture, bulk density, isotopic abundance) and related sampling metadata for GIS and environmental analyses.
- Data and publications are archived for public access and further use.

## Data collection and sample management
- Field samples collected and sent to the laboratory; strict sample registration and storage processes.
- Sample tracking includes:
  - Person in charge and field/lab IDs
  - Program/project name and ID
  - Sampling period and site
  - Sample type (soil, plant, etc.)
  - Sampling method and depth
  - Land cover or cropping system
  - Number of samples and list of sample IDs
  - Analysis requirements (which analyses to perform)
- A unique ID is generated per sample; field IDs and lab IDs are reconciled with a final electronic concordance list.
- Emphasis on linking sampling locations and land-use context to enable spatial analysis.

## Analytical methods and data types
- Sample preparation: field samples sent to lab, then dried, ground, and sieved as required.
- Soil organic carbon (SOC)
  - Measured by Walkley-Black method (wet oxidation, titration).
  - Mid-Infrared Spectroscopy (MIRS) on all samples to develop predictive models; MIRS-based predictions used for remaining samples.
- Soil texture
  - Chemical analyses and MIRS used to predict texture fractions (sand, silt, clay).
  - Organic matter removal with H2O2; particle size analysis via dry sieving and pipette methods.
- Bulk density
  - Determined from dry soil weight after removing coarse fraction (>2 mm).
- Natural 13C abundance (13δ)
  - Analyzed for a subset and sent to external labs for additional analyses.
- MIRS details
  - Scanning with Agilent 4100 ExoScan FTIR; used to build predictive models for soil properties.
- Data are produced with standardized methodologies and calibration/validation via MIRS models.

## Data publication and accessibility
- All generated datasets archived at Environmental Information Data Centre (EIDC).
- Datasets published or in publication pipeline; multiple papers listed (e.g., soil carbon stocks, land-use changes, and soil organic carbon variability).
- References provided for standard methods (e.g., AFNOR 1999; Walkley & Black 1934).

## GIS-relevant data and potential uses
- Core variables and metadata for map-based analysis:
  - Sampling site and coordinates context (site IDs, land cover, sampling depth)
  - SOC values (laboratory and MIRS-predicted)
  - Soil texture fractions (sand, silt, clay; predicted via MIRS)
  - Bulk density
  - 13C abundance (where available)
  - Temporal context (sampling period)
- Enables mapping of soil properties, their spatial distribution, and changes with land-use or cover changes.
- Supports integration with land-use, vegetation, and climate datasets for ecosystem and carbon-stock studies.
- Data quality, traceability, and standardization enhance reproducibility for GIS workflows.

## Metadata, standards, and quality assurance
- Sample registration and concordance between field and lab IDs ensure traceability.
- Use of established methods (Walkley-Black) and calibration via MIRS with explicit prediction for remaining samples.
- Archiving in EIDC ensures long-term accessibility and reusability.

## Key references and notes
- AFNOR (1999). Quality standards for soils.
- Walkley, A.; Black, J. (1934). SOC determination method.
- Publications arising from the data include studies on land-use impacts on soil and aboveground carbon stocks, SOC variability, and carbon stock changes following land-cover change.

## How this supports GIS Specialists
- Provides a structured, mineral soil dataset with spatially referable sampling metadata and derived properties suitable for map-based visualization and analysis.
- Offers a pathway to build predictive soil-property layers (via MIRS models) across larger areas.
- Ensures data provenance and availability through systematic registration, QA, and centralized archival (EIDC) for reproducible GIS workflows.