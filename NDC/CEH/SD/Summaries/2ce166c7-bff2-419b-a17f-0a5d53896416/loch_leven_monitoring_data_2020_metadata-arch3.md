# Loch Leven long-term monitoring dataset

- Overview
  - Long-term monitoring programme of Loch Leven, a lowland lake in Scotland, started in 1968 and ongoing.
  - Conducted by staff from former Natural Environment Research Council (NERC) institutions, most recently NERC / UK Centre for Ecology & Hydrology.
  - This document describes the data, sampling and analysis methods, data processing, and output format. Part of the UK-SCAPE WP7 LEVEN project.

- Sampling regime and sites
  - Fortnightly sampling with two main sites visited per occasion; three sites are represented in the dataset: Harbour (H), Reed Bower (RB/RB5), and Sluices / Outflow (L/Sl8).
  - Reed Bower is boat-access only; Sluices can be sampled by boat or from shore. Outlet measurements are recorded as Sluices for ease of use.
  - Some sampling cannot occur due to resource constraints, bad weather, or ice cover.
  - Sampling locations and coordinates are provided, with site codes used throughout the long-term programme.

- Measurements, sampling, and analyses
  - In situ measurements: conductivity, pH, and temperature at most sites; Secchi depth measured at Reed Bower.
  - Water samples: duplicate 2 L samples from each site; Reed Bower uses an integrated sample via weighted PVC tube; Sluices uses a bottle held ~10 cm below surface.
  - Laboratory analyses (on filtered or unfiltered samples as appropriate): soluble reactive phosphorus (SRP), total soluble phosphorus (TSP; filtered and frozen), soluble reactive silicate, total diatom silica, total phosphorus (TP; unfiltered and frozen), chlorophyll a (by filtering 400 mL per site).
  - Phosphorus methods follow Murphy & Riley (1962) for SRP; TP uses Wetzel & Likens (2000) methodology with an added acid digestion step; TSP mirrors TP but on filtered samples.
  - Weather data (cloud cover, wind direction, wind force) recorded at Reed Bower when possible; wind force linked to a Beaufort scale as described in a lookup table.

- Crustacean & zooplankton data
  - Densities of crustacean zooplankton collected at Reed Bower and Sluices; taxa include various Daphnia, Eudiaptomus, Cyclopidae/Cyclops, Bosmina, Leptodora, Bythotrephes, Chydoridae, Polyphemus pediculus, etc. Densities given as individuals per litre (ind/L); zeros indicate non-detection within sampling/analysis resolution; NA indicates missing values.
  - Sampling and preservation: Reed Bower samples collected with a 4 m, 120 µm mesh net; Sluices samples passed 30 L surface water through a 120 µm net. Preserved in 4% formaldehyde.
  - Laboratory processing: samples reconstituted to 250 mL, sub-sampled, identified (to species where feasible) and counted under a microscope; counts converted to ind/L using standard factors; preserved samples archived.

- Data processing and quality assurance
  - Data processing performed with an R import script that standardises and sensibly handles data.
  - Wind force field: when a range (e.g., 4-5) is given, the first value is used in the database.
  - Probe replicates (conductivity, pH, DO, and related temperatures) undergo replication validation using Median Absolute Deviation (MAD); values falling outside MAD bounds are adjusted according to defined rules. pH values are converted to 10^pH, median/MAD calculated, then transformed back and rounded (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
  - Automated and manual quality assurance checks identify and correct anomalies or out-of-range values.
  - Data are stored in a single CSV file with explicit units and site identifiers; missing data are marked as NA.

- Format of stored data and column descriptions
  - CSV file contains columns for site conditions, lake chemistry, and crustacean/zooplankton counts; units and site references are included.
  - Example columns (descriptions): Date, Week_of_Year; wind and cloud data (Cloud_cover_Eighths_Site_RB, Wind_Direction_Site_RB, Wind_Force_Beaufort_scale_Site_RB); depth and Secchi depth; Conductivity and Temperature (Site_RB and Site_L); DO (mG/L and %); pH; TP, SRP, TSP; chlorophyll a; zooplankton taxa densities (e.g., Daphnia_hyalina_ind/L_Site_RB, Eudiaptomus_gracilis_ind/L_Site_RB, etc.).
  - Replicates are indicated in column names (e.g., RB1, RB2; L1, L2); site codes include Harbour (Site_H), Reed Bower (Site_RB), Sluices (Site_L).
  - Column descriptions and exact determinands are detailed in Table 3 of the document.

- Data sources, references, and further reading
  - Analytical methods: Golterman et al. (1978); Murphy & Riley (1962); Wetzel & Likens (2000).
  - Crustacean zooplankton identification references: works by Dussart & Defaye (1995), Einsle (1996), Flößner & Kraus (1986), Harding & Smith (1974), Scourfield & Harding (1966).
  - Additional reading and related reports include Hydrobiologia special issue and Scottish Natural Heritage reports (e.g., 2008–2010 monitoring report) and Loch Leven 40 years of research (2012).