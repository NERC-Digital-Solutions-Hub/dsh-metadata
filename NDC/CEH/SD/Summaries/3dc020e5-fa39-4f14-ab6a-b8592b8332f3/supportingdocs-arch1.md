Physical, chemical and biological data from peatland ponds, Pennines, UK, 2012-2014

- Purpose and scope
  - Dataset used in Beadle et al. (in press): Landscape-scale peatland rewetting benefits aquatic invertebrate communities.
  - Combines biological data (invertebrate abundances) with physical (location, pond morphology, elevation) and chemical data (dissolved ions, pH, and other solutes).
  - Aims to study colonization and establishment of invertebrate communities in restored peatland ponds, changes in abundances and diversity (alpha, beta), and associations between physico-chemical variables and ecological communities.

- Study area and time frame
  - Location: peatland ponds in the Pennine hills, northern England.
  - Timeframe: fieldwork conducted 2012–2014.
  - Ponds treated as individual spatial points; both restored/chronosequence ponds and naturally formed ponds included.

- Data collected and formats
  - Biological data: invertebrate abundances (identified to species where possible; Chironomidae subject to subsampling when abundant).
  - Physical data: geographic coordinates, elevation, aspect, pond dimensions (long/short axis, perimeter), pond volume, surface vegetation cover, depth measurements (minimum 40 per pond), and calculated water volume.
  - Chemical data: on-site measurements of dissolved oxygen, water temperature, pH; laboratory analyses of dissolved nutrients and solutes (TN, TP, DOC, Al, Fe, Si) using multiple instruments.
  - Data files (four CSVs) structure:
    - Chron_nat_inverts.csv: 82 columns; pond code plus abundances for invertebrate taxa per pool.
    - MH_inverts.csv: 45 columns; pond code plus invertebrate taxa abundances per pool.
    - Chron_natural_physical_chemical.csv: 26 columns; pond code, location, date, pond age, coordinates, habitat variables, physico-chemical measurements.
    - MH_physical_chemical.csv: 26 columns; pond code, site, date, pond age, coordinates, habitat and morphometric variables, and chemical measurements including nutrients and veg cover.

- Sampling design and sites
  - Sampling regimes:
    - Moor House National Nature Reserve: continuous monitoring from 04/2013 to 06/2014 (ages 4–18 months), two-monthly visits; random pond sampling within each ditch; ponds disturbed due to small size.
    - Chronosequence (six peatlands): each visit samples five ditches with one pond per ditch; 06/2013 and 06/2014 with different ponds (ten ponds per site).
    - Naturally-formed ponds: twenty ponds across four peatlands (07/2012); non-random sampling due to landowner access; pond counts per site varied (2–7).
  - Total ponds sampled: 105.
  - Natural ponds denoted with a prefix (e.g., nWFN01) to indicate natural origin.
  - Detailed site characteristics provided (locations, altitudes, restoration years, pond ages for 2013 and 2014).

- Field and laboratory methods
  - Macroinvertebrate collection: long-handled net (250 µm); 2 minutes across mesohabitats plus 1 minute for surface taxa; vegetation cover visually estimated on-site; samples preserved in 70% methanol and transported to lab.
  - Taxonomic processing: sorting and identifying to species level where possible; Chironomidae subsampling (n=50) when totals exceed 50; specific prep steps for chironomids including chemical treatments and mounting for microscopy.
  - Habitat and physico-chemical measurements: altitude, coordinates (Garmin eTrex); aspect derived from coordinates; pond dimensions measured on-site; depth measurements (≥40 per pond); water volume estimated as area x mean depth.
  - On-site sensors: DO, temperature, pH measured with portable HACH HQ30d meter (pH sensor failed in month 12; missing values imputed using pH–Mg relationship; r = 0.81).
  - Chemical analyses: filtered water samples (0.45 µm) analyzed for TN, TP, DOC, Al, Fe, Si using Analytikjena multi N/C 2100, San++ AFA, and Thermo Fisher iCAP7600 Duo ICP-OES.

- Data quality, completeness and metadata
  - Completeness: dataset described as complete, with five pH values imputed due to sensor failure.
  - Quality control:
    - Independent verification of macroinvertebrate specimens by experts.
    - Pre-visit calibration of sensors (DO, temperature, pH) and laboratory equipment for chemical analyses with standards across the measurement range.
  - Metadata and traceability:
    - Data organized into four CSV files with explicit pond codes to enable cross-file linking.
    - Detailed variable descriptions and units provided in the dataset documentation.

- Important considerations for analysts
  - Linking datasets: pond codes allow merging of biological and physico-chemical data across Chron_nat_inverts, MH_inverts, Chron_natural_physical_chemical, and MH_physical_chemical.
  - Temporal scope: primary periods are 2013 and 2014, with additional 2012 natural ponds data; consider pond age and restoration year as covariates.
  - pH data gaps: a sensor failure in month 12 led to five imputed pH values; consider sensitivity analyses for pH-related results.
  - Sampling design nuances: mixed sampling regimes (restoration chronosequence, natural ponds, and intensive Moor House monitoring) may require stratified analyses or random-effects modeling to account for site and pond-level variation.
  - Taxonomic resolution: high-resolution identification for invertebrates, with Chironomidae potentially resolved to lower taxonomic levels in subsamples; account for sampling effort and subsampling in analyses of abundance.
  - Data provenance: data used to infer relationships between rewetting, invertebrate communities, and water chemistry; appropriate modeling should consider both alpha and beta diversity metrics and multivariate associations with physico-chemical variables.