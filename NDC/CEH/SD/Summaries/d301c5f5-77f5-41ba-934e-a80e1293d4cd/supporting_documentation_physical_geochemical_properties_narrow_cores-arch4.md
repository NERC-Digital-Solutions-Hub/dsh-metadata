# Physical_geochemical_properties_narrow_cores.csv

- Project context: Part of the Carbon Storage in Intertidal Environments (C-SIDE) initiative funded by NERC (NE/R010846/1). Team includes researchers from University of St Andrews, University of Glasgow, University of York, University of Leeds, Bangor University, and UK CEH among others.

- Data resource purpose: Physical and geochemical measurements of saltmarsh soils to calculate organic carbon soil stocks across UK saltmarsh ecosystems.

- Data scope and content:
  - 462 narrow-diameter gouge cores (30 mm) collected from 22 UK saltmarshes (2018–2021).
  - Measurements include: elevation above ordnance datum, substrate (Troels-Smith classification), wet bulk density, dry bulk density, and organic carbon content (% OC).
  - Core and site metadata: Core_ID, Saltmarsh name, Marsh_type (Natural or Realigned), Marsh_zone (Low or High), Nation (Scotland/Wales/England), Collection_year.
  - Spatial data: latitude/longitude (WGS84), X_easting, Y_northing, elevation, and sampling depths (Sample_depth_cm, Mid_Point_depth_cm).

- Location and coverage:
  - UK-wide sites chosen to represent saltmarsh variability; locations provided as decimally-referenced coordinates and Easting/Northing coordinates.
  - All sites are within similar environmental regions to enable comparability across Scotland, England, Wales.

- Variables and data structure:
  - Core-level fields: Core_ID, Saltmarsh, Marsh_type, Marsh_zone, Nation, Collection_year.
  - Location fields: Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, Elevation_above_OD__m.
  - Sampling fields: Sample_depth_cm, Mid_Point_depth_cm, Substrate.
  - Measurements: Wet_bulk_density_g_cm_3, Dry_bulk_density_g_cm_3, OC_perc.
  - File format: .csv with descriptive headers and a data/resource description detailing each field and format.

- Methods and procedures:
  - Field sampling: 462 cores collected using a 30 mm gouge corer; sub-samples (n=3434) taken at 10 cm intervals in the field.
  - Core descriptions follow Troels-Smith classification; DGPS used for site locations.
  - Sample handling: cores frozen at -20°C; moisture is determined via drying at 60°C for 72 hours to compute bulk density.
  - Lab analysis: 50 mg subsamples analysed for organic carbon using Elementar Soli TOC with a temperature gradient method (DIN 19539; Natali et al., 2020; Smeaton et al., 2021).
  - Calibration: TOC analyses calibrated with CaCO3 and standard soils (B2290).

- Quality control and provenance:
  - Laboratory equipment calibrated according to University of St Andrews practices.
  - Data checks conducted; documentation includes data descriptions, units, and field formats.
  - References provided for methods and calibration standards (Dadey et al., 1992; DIN 19539; Natali et al., 2020; Smeaton et al., 2021; Troels-Smith, 1955).

- Data access and documentation:
  - Data resource described with detailed headers, formats, and cell formats; notes indicate NA where data are not applicable.
  - File type: CSV; metadata and resource descriptions accompany the dataset to support discoverability and reuse.

- Relevance for data leadership and strategy:
  - Demonstrates end-to-end data collection, from field sampling to laboratory analysis, with clear documentation of methods, units, and coordinates.
  - Supports the management of data assets through comprehensive metadata, enabling cross-site comparisons and UK-wide carbon stock assessments.
  - Addresses key data-system considerations: discoverability (metadata fields), data quality (calibration and QA), and user-oriented outputs (carbon stock calculations across saltmarsh ecosystems).