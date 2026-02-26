# File Uploaded to EIDC: hydroscape_lakedistrict_core_metadata.csv

- A metadata CSV describing lake sediment core samples from the Hydroscape Lake District, including identifiers, location, core characteristics, and dating status.
- Key identifiers:
  - WBID: Waterbody Identification number
  - Hydroscape: Hydroscape region name
  - Name: Lake name
- Core location and type:
  - General_location_of_core: core designation (deep, littoral, or intermediate)
  - OSGB36_E / OSGB36_N: UK OS grid coordinates (OSGB36 datum)
- Measurements and site characteristics:
  - Water_depth_at_core_site_(m): water depth from surface to sediment at the core site, measured with a handheld echo sounder; littoral depth confirmed with a Secchi disc
  - Secchi_disc_depth_(m): mean Secchi depth (3 measurements) from the deepest lake position
  - Core_length_and_type: core length in metres and the corer type used (Tapper, Big Ben, Livingstone, Renberg) with literature references
- Metadata and identifiers:
  - Date_core_collected: date of fieldwork and core collection (dd/mm/yyyy)
  - UCL_Code: internal UCL code for bags/database
  - UCL_Sample_ID: internal Amphora core sample ID (unique)
- Dating status:
  - 210 Pb-dated_Y_N_for_Hydroscape: whether the core was dated by 210Pb during the project (Yes or No)

- Methods explained:
  - Water depth measured with a handheld echo sounder; Secchi depth used to validate littoral depths
  - Secchi depth computed as the mean of three measurements
  - Core types correspond to established piston corers with references provided for replication

- Data provenance and use:
  - Data originate from UCL and linked to a UK Centre for Ecology & Hydrology hydroscape framework
  - Coordinates in OSGB36 enable spatial analyses and mapping of core locations
  - Dating status informs potential construction of age models and palaeoenvironmental analyses

- Potential uses for analysts:
  - Correlate lake depth, water clarity (Secchi depth), and core characteristics across lakes
  - Build predictive or comparative models of palaeolimnological proxies
  - Integrate with broader Hydroscape datasets for regional trend analyses
  - Validate spatial patterns using precise OS coordinates and lake identifiers

- Considerations and challenges:
  - Local-scale data; may require harmonization with other coordinate systems or lake boundaries
  - Completeness and consistency of internal UCL identifiers across datasets
  - Variability in core collection methods and dating availability across cores may affect comparability