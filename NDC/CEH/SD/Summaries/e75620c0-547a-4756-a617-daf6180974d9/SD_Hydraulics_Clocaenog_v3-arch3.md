# SOIL HYDRAULIC PROPERTY DATA FROM THE CLIMOOR FIELDSITE IN THE CLOCAENOG FOREST 2010-2012

- Purpose and scope
  - Dataset of soil hydraulic properties collected to monitor the effects of warming and drought on ecosystem processes at the Climoor field site in Clocaenog Forest, North Wales.
  - Five data sets capture key soil properties: bulk density, unsaturated hydraulic conductivity, and soil water release curves (SWRC) measured via HYPROP, minidisk infiltrometer, HYPROP lab processes, and WP4 potentiometer methods.

- Field site and climate treatments
  - Location: Clocaenog Forest, upland Atlantic heathland dominated by Calluna vulgaris.
  - Experimental design: automated drought and warming treatments with three replicate plots each, plus three control plots.
  - Drought: retractable roof excludes rainfall May–Sept, reducing annual rainfall by ~20%.
  - Warming: retractable aluminum curtains reduce nighttime heat loss; rainfall exclusion during rain events creates a net reduction in annual rainfall of ~14%.
  - Plot size: 4 m x 5 m; sampling focused on plot edges away from prevailing winds.

- Data collection and measurement methods
  - Data sets
    - (1) Bulk_density.csv: soil bulk density (0–5 cm) and saturated water content.
    - (2) Minidisk_K.csv: field-measured unsaturated hydraulic conductivity at tensions of -2 cm and -6 cm using a minidisk infiltrometer.
    - (3) Hyprop_K.csv: HYPROP in-lab measurements of unsaturated hydraulic conductivity on 250 cm3 soil cores.
    - (4) Hyprop_SWRC.csv: HYPROP-derived soil water release curves for wet soil, interpolated to common suction values.
    - (5) WP4_SWRC.csv: SWRC data for dry soil measured with WP4 potentiometer.
  - Instrumentation and procedures
    - HYPROP: soil cores processed and measured to determine hydraulic properties; data analyzed with HYPROP-FIT software.
    - Minidisk infiltrometer: standard field protocol to derive hydraulic conductivity; data converted per the manufacturer's method.
    - WP4 potentiometer: dewpoint-based technique to measure soil water potential with rapid equilibrium.
  - Sampling timeline
    - Data collected between end of 2010 and early 2012.
    - Specific collection events: 2011 April and September for HYPROP SWRC and bulk density; 2011 samples for HYPROP moisture curves; 2012 May for minidisk measurements; 2010 November for WP4 SWRC.

- Data processing and quality assurance
  - Raw data visually inspected as part of QA/QC.
  - HYPROP data interpolated to a regular set of suction values using spline fitting in R.
  - SWRC data interpolated to common suction values to enable comparison.
  - Data not infilled; missing values marked as NA.
  - Bulk density derived from oven drying (105°C, 16 hours) and sample ring volume; note that samples are fully organic with no stones.

- Data structure and documentation
  - File summaries
    - (1) Bulk_density.csv: bulk density (g/cm3), saturated water content, sample metadata (Plot, Treatment, etc.).
    - (2) Minidisk_K.csv: unsaturated hydraulic conductivity at two tensions, per plot, with units cm/s and cm/day; includes tension and plot identifiers.
    - (3) Hyprop_K.csv: unsaturated hydraulic conductivity from HYPROP, with suction values and corresponding conductivity by plot and treatment.
    - (4) Hyprop_SWRC.csv: SWRC data from HYPROP, with interpolation point numbers and VWC values for each plot and treatment.
    - (5) WP4_SWRC.csv: SWRC data from WP4, with temperature, soil moisture, matric potential, and pressure head records.
  - Metadata and notes
    - Each dataset includes unit definitions, plot and treatment identifiers (Control, Drought, Warming), and descriptive column headings.
    - Data interpretation and software references included (HYPROP-FIT, R spline interpolation, and associated manuals).

- Roles and responsibilities
  - D.A. Robinson: HYPROP measurements and SWRC interpretation.
  - I. Lebron: HYPROP measurements, SWRC, and bulk density.
  - A.R. Smith: WP4 measurements.
  - M.R. Marshall: Minidisk measurements.
  - B.A. Emmett: Principal investigator, Clocaenog field site.
  - S. Reinsch: Field site science management.
  - D.M. Cooper: Statistical interpolation in R.
  - M. Brooks: Field site and roof maintenance.

- Data context and references
  - Field site and climate manipulation described to support interpretation of soil hydraulic responses under drought and warming.
  - Key references include Domínguez et al. (2015), Reinsch et al. (2016a,b), Robinson et al. (2016), and related methodological manuals for HYPROP, HYPROP-FIT, and WP4.