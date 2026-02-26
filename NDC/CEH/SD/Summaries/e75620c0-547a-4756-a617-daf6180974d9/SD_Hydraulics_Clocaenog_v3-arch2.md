# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

- Overview
  - Five data sets of soil hydraulic properties from the Climoor field site, Clocaenog Forest, North Wales.
  - Measurements include: bulk density and saturated water content; field and laboratory unsaturated hydraulic conductivity; soil water release curves for both wet and dry soils.
  - Data collected 2010–2012; quality checked, with incorrect or missing values removed; no data infilling; NA values added where data are absent.

- Field site and experimental design
  - Location: Clocaenog Forest, North Wales; upland Atlantic heathland dominated by Calluna vulgaris.
  - Long-term drought and warming experiment: three replicated plots for each treatment plus three controls (4 m x 5 m plots).
  - Automated roof and curtain systems to reduce rainfall during drought and to modulate nocturnal warming, with safeguards for high wind and rain events.
  - Soil type: podzolic organo-mineral horizons with high organic matter; intensive monitoring equipment including meteorological stations.
  - Treatments: drought (May–September) reduces rainfall by ~20% on average (and exclusion of most rainfall during active periods); warming uses retractable aluminum mesh curtains that reduce nocturnal heat loss, trimming rainfall in practice (approx. 14% annual rainfall reduction).

- Data sets and contents
  - (1) Bulk_density.csv
    - Dry bulk density measurements (0–5 cm), plus saturated water content indicators and related soil properties.
  - (2) Minidisk_K.csv
    - Field-measured unsaturated hydraulic conductivity at tensions of -2 cm and -6 cm using a minidisk infiltrometer; includes plot-level treatment and tension information; reported as cm/s and cm/day.
  - (3) Hyprop_K.csv
    - Laboratory-measured unsaturated hydraulic conductivity using HYPROP on 250 cm³ soil cores; includes suction (kPa) and corresponding conductivity (cm/day) across plots and treatments.
  - (4) Hyprop_SWRC.csv
    - Soil water release curves from HYPROP in the laboratory; interpolated onto regular suction values; includes interpolation point numbers and volumetric water content (VWC) for plots under warming, control, and drought.
  - (5) WP4_SWRC.csv
    - Soil water release curves using WP4 potentiometer method for dry soil samples; includes temperature, soil moisture, matric potential, and corresponding measurements.

- Methods and data processing
  - Sampling and measurement
    - HYPROP: soil cores (250 cm³, 0–5 cm depth) collected from plot edges; HYPROP equipment used for evaporation-based retention and conductivity measurements; results interpolated to common suction values using spline fitting in R.
    - Minidisk: field measurements at two tensions (-2 cm, -6 cm) with standard conversion to hydraulic conductivity.
    - WP4: laboratory measurements on dry soil samples using WP4 potentiometer method.
  - Data processing and QA
    - Raw moisture-release data processed with HYPROP-FIT software.
    - Interpolations performed in R; manual and device manuals referenced for processing steps.
    - Bulk density calculated from oven-dried mass (105°C, 16 h) and sample volume.
  - Documentation and structure
    - Data file details and column descriptions provided; supporting manuals and data-series documentation referenced.

- Quality assurance and provenance
  - Data visually inspected as part of QA/QC.
  - No data infilling performed; missing values represented as NA.
  - Data interpreted and cross-referenced with published work (e.g., Domínguez et al. 2015; Robinson et al. 2016).

- Lineage and contributors
  - Collected by experienced soil scientists; specific roles include HYPROP measurements, soil water release curves (D.A. Robinson; I. Lebron; A.R. Smith), WP4 measurements (A.R. Smith), minidisk measurements (M.R. Marshall), field site leadership (B.A. Emmett), science management (S. Reinsch), statistical interpolation in R (D.M. Cooper), field site and roof maintenance (M. Brooks).

- Usage and significance
  - Supports analysis of how warming and drought affect soil hydraulic properties and soil moisture dynamics.
  - Data underpin ongoing and published work on drought impacts and soil physical changes in heathland ecosystems.
  - Standardized methodologies enable temporal comparisons and cross-study integration.

- References and related materials
  - Key publications: Domínguez et al. (2015); Reinsch et al. (2016a, 2016b); Robinson et al. (2016); and related HYPROP and WP4 manuals.
  - Supporting documentation: Clocoenog_field-site data series, HYPROP and WP4 manuals, and data processing manuals.

- Access and documentation
  - Data supported by supporting materials, manuals, and data centre records; detailed metadata included in the dataset documentation.