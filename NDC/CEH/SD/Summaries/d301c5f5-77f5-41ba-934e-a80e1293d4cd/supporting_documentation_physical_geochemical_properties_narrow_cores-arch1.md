# Physical_geochemical_properties_narrow_cores.csv

## Overview
- Dataset of physical and geochemical properties of saltmarsh soils.
- Based on 462 narrow-diameter gouge cores collected from 22 UK saltmarshes between 2018 and 2021.
- Purpose: to calculate organic carbon soil stocks across UK saltmarsh ecosystems.

## Data scope and coverage
- Geographic scope: United Kingdom, with sites chosen to represent saltmarsh diversity in Scotland, England, and Wales; coordinates provided in WGS84.
- Spatial fields include latitude/longitude, as well as X (easting) and Y (northing) coordinates, plus elevation above ordnance datum.
- Substantial sampling depth structure: sub-samples (n=3434) taken at 10 cm resolution within cores.
- Data intended to enable UK-wide comparisons of saltmarsh soil properties and organic carbon stocks.

## Variables and structure
- Core_ID: identifier for each core.
- Saltmarsh: site name.
- Marsh_type: Natural or Realigned.
- Marsh_zone: Low (LM) or High (HM) within marsh.
- Nation: England, Scotland, or Wales.
- Collection_year: year of core collection.
- Lat_dec_deg / Long_dec_deg: geographic coordinates (decimal degrees, WGS84).
- X_easting / Y_northing: alternative location coordinates.
- Elevation_above_OD__m: height above ordnance datum (m).
- Sample_depth_cm: depth interval of sub-sample (cm).
- Mid_Point_depth_cm: midpoint of depth interval (cm).
- Substrate: Troels-Smith soil classification.
- Wet_bulk_density_g_cm_3: measured wet bulk density.
- Dry_bulk_density_g_cm_3: measured dry bulk density.
- OC_perc: organic carbon content (% by weight).

## Sampling and laboratory methods
- Sampling: 462 cores collected using a 30 mm gouge corer.
- Sub-sampling: 3434 subsamples distributed across cores at 10 cm intervals.
- Core handling: DGPS location, cores frozen at -20°C until analysis.
- Sample preparation: drying at 60°C for 72 hours to determine bulk density; milled to fine powder.
- Carbon quantification: 50 mg per sample analyzed for total organic carbon (TOC) using a Soli TOC analyzer with a temperature gradient method (DIN 19539; Natali et al., 2020; Smeaton et al., 2021).
- Calibration: Soli TOC calibrated with CaCO3 and silty soil TOC/ROC/TIC standards.
- Quality control: laboratory equipment calibrated according to University of St Andrews practices.

## Data quality and metadata
- Statistical treatment: not applicable (NA) for this dataset.
- Data checking/quality control: calibration standards used; equipment calibration documented.
- File format: CSV.
- Metadata coverage: dataset description includes site-level context, sampling scheme, depths, and measurement methods.

## Spatial and temporal context
- Temporal span: samples collected 2018–2021.
- Spatial representation: designed to capture variability across UK saltmarsh soils (scales from core to marsh, across multiple nations).

## Access, format, and reuse
- Data resource is provided as a CSV file with a described header and fields mapping.
- Data designed to support calculation of organic carbon stocks and comparative analyses across UK saltmarsh ecosystems.

## References
- Dadey, K.A., Janecek, T., Klaus, A. (1992). Dry-bulk density: its use and determination.
- DIN 19539 (2015). Investigation of solids: Total Carbon differentiation (TOC/ROC/TIC).
- Natali, C., Bianchini, G., Carlino, P. (2020). Thermal stability of soil carbon pools.
- Smeaton, C., Hunt, C.A., Turrell, W.R., Austin, W.E. (2021). Marine Sedimentary Carbon Stocks of the UK EEZ.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments.