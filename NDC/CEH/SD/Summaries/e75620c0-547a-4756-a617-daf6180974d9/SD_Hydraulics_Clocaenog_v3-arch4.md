# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

- Overview
  - A dataset of soil hydraulic measurements from the Climoor field site in Clocaenog Forest, North Wales.
  - Contains five data sets: (1) soil bulk density (0–5 cm) and saturated water content; (2) unsaturated hydraulic conductivity measured in the field with a minidisk infiltrometer at tensions of -2 and -6 cm; (3) unsaturated hydraulic conductivity measured with HYPROP on soil cores in the lab; (4) soil water release curves for wet soil from HYPROP laboratory measurements; (5) soil water release curve data for dry soil measured with a WP4 potentiometer.
  - Data were collected 2010–2012, quality checked, with incorrect/missing values removed; no data infilling; NA values added where data were absent.
  - Aimed to monitor site-specific soil properties to study effects of warming and drought on ecosystem processes.

- Datasets included
  - (1) Bulk_density.csv: dry bulk density and related properties; 0–5 cm depth.
  - (2) Minidisk_K.csv: field-measured unsaturated hydraulic conductivity at -2 cm and -6 cm; includes tension, plot, and treatment (Control/Drought/Warming) information.
  - (3) Hyprop_K.csv: laboratory-measured unsaturated hydraulic conductivity using HYPROP; includes data across multiple plots and treatments.
  - (4) Hyprop_SWRC.csv: HYPROP-derived soil water release curves; interpolated to regular suction values.
  - (5) WP4_SWRC.csv: WP4 potentiometer-derived soil water release curves for dry soil; includes temperature, soil moisture, matric potential, and pressure head.
  - Interpolation and data processing: HYPROP data interpolated with spline fitting in R to align with common suction values; minidisk data converted to hydraulic conductivity using standard procedures; HYPROP data interpreted with HYPROP-FIT software.

- Study site and experimental setup
  - Clocaenog climate change field site: upland Atlantic heathland dominated by Calluna vulgaris; automated drought and warming treatments established since 1998.
  - Treatments: three drought plots and three warming plots, plus three control plots.
  - Drought treatment: retractable roof excludes rainfall May–September, reducing annual rainfall by ~20% (some events missed due to sensor limits).
  - Warming treatment: retractable aluminum mesh curtains at night; reflect infrared radiation and reduce heat loss; occasional retraction during rain to preserve rainfall; average annual rainfall reduction ~14%.
  - Sampling location: Hyprop cores collected from the eastern plot edges; samples taken under heather, moss-free.

- Data collection and processing methods
  - Datasets and methods:
    - HYPROP measurements: soil cores (250 cm3) 0–5 cm depth; water release curves via HYPROP evaporation; high suction via WP4 for very dry end.
    - Minidisk infiltrometer: field measurements at -2 cm and -6 cm tensions.
    - WP4 potentiometer: laboratory measurements for very dry conditions.
  - QA/QC: visual inspection of raw data; HYPROP data processed with HYPROP-FIT; spline interpolation in R to achieve a common suction grid; observations and manuals included in dataset supporting materials.
  - Documentation and field notes: detailed field-site protocols, sampling squares near G7/G8, just above rain gauge funnel; clear delineation of plots and treatments in the data files.

- Data structure and file-level details
  - (1) Bulk_density.csv: Dry bulk density, saturated water content; includes plot, treatment, and density values.
  - (2) Minidisk_K.csv: Unsaturated hydraulic conductivity (field); columns include plot, treatment, tension (cm), and mean_k (cm/s and cm/day) with a pairing of suction and conductivity per plot.
  - (3) Hyprop_K.csv: Unsaturated hydraulic conductivity (laboratory HYPROP); columns cover suction values and corresponding unsaturated conductivity (cm/day) for multiple plots/treatments.
  - (4) Hyprop_SWRC.csv: Soil water release curves from HYPROP; includes interpolation number, suction (kPa), and volumetric water content (VWC) for plots with warming/drought/control design.
  - (5) WP4_SWRC.csv: Soil water release curves by WP4 method; includes temperature, soil moisture, matric potential, and pressure head; 60 rows across 4 columns.
  - Each dataset is accompanied by a detailed data-structure description (column headers, units, and notes) and references to supporting manuals and software.
  - Overall dataset includes six columns and ten rows for Bulk_density, 5 columns and 19 rows for Minidisk_K, 18 columns and 45 rows for Hyprop_K, 11 columns and 501 rows for Hyprop_SWRC, and 4 columns and 60 rows for WP4_SWRC, with explicit pairings between suction and conductivity for each plot.

- Quality, limitations, and metadata
  - Data quality: validated by staff scientists; incorrect/missing values removed; no data infilling performed.
  - Some rainfall events may have been missed due to sensor limitations, affecting drought intensity; warming roofs may exclude some rainfall due to response lag.
  - Metadata includes instrument specifics, sampling details, and processing workflows; supporting documentation and manuals are provided.

- References and related materials
  - Domínguez et al. 2015; Reinsch et al. 2016a/b; Robinson et al. 2016; Sowerby et al. 2008; Dominguez et al. 2015; supporting documentation titled Clocaenog_supporting_documentation_Data_series.
  - HYPROP, HYPROP-FIT, and WP4 manuals referenced for methods and data processing.

- Roles and responsibilities
  - D.A. Robinson: HYPROP measurements and soil water release curves.
  - I. Lebron: HYPROP measurements, soil water release curves, and bulk density.
  - A.R. Smith: WP4 measurements.
  - M.R. Marshall: Minidisk measurements.
  - B.A. Emmett: Principal investigator, Clocaenog field site.
  - S. Reinsch: Field site science manager.
  - D.M. Cooper: Statistical interpolation in R.
  - M. Brooks: Field site and roof maintenance.