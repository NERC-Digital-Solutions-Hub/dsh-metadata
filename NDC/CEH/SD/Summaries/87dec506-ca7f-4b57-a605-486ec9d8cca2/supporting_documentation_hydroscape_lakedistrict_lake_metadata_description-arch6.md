# File Uploaded to EIDC: hydroscape_lakedistrict_core_metadata.csv

- ## Overview
  - Metadata for the dataset hydroscape_lakedistrict_core_metadata.csv uploaded to EIDC.
  - Describes lake core samples in the Hydroscape Lake District, including location, depth, core details, dating, and identifiers.

- ## Data schema (key fields and descriptions)
  - EIDC_File_Name: File name uploaded to EIDC (.csv).
  - Waterbody Identification number (WBID): Unique ID for the waterbody; linked to the UK Centre for Ecology & Hydrology Lakes index.
  - Hydroscape: Name of the Hydroscape region used.
  - Name: Lake name.
  - General_location_of_core: Core location typology within the lake (deep central, littoral near vegetation margin, or intermediate mid-depth).
  - OSGB36_E: Easting coordinate (OSGB36 datum) for the lake core site.
  - OSGB36_N: Northing coordinate (OSGB36 datum) for the lake core site.
  - Water_depth_at_core_site_(m): Water depth from surface to sediment at the core site (in meters); measured with a handheld echo sounder from a boat; littoral depths confirmed with Secchi disc to sediment.
  - Secchi_disc_depth_(m): Mean Secchi depth (in meters) recorded as a measure of water clarity; three measurements are taken, mean calculated; taken at the deepest lake position.
  - Core_length_and_type: Core length (in meters) and corer type used; corer types referenced include Tapper, Big Ben, Livingstone, Renberg with corresponding literature.
  - Date_core_collected: Date of fieldwork and core collection (dd/mm/yyyy).
  - UCL_Code: Internal University College London code used on bags/database.
  - UCL_Sample_ID: Internal Amphora code for the entire sample core (unique ID).
  - 210 Pb-dated_Y_N_for_Hydroscape: Indicates whether the core was dated by 210Pb during the project (Yes or No).

- ## Data collection methods and context
  - Water depth measured using handheld echo sounder from a boat; littoral depth cross-checked with Secchi depth method.
  - Secchi depth obtained using a 20 cm Secchi disc; three measurements per site with mean calculated; measured at the deepest lake position.
  - Core length and type documented with specific corers:
    - Tapper: Chambers & Cameron (2001) rod-less piston corer.
    - Big Ben: Patmore et al. (2014) wide-bore piston corer.
    - Livingstone: Livingstone (1955) lightweight piston sampler.
    - Renberg & Hansson (2008) HTH sediment corer.
  - Core dating status (210Pb) recorded to indicate whether radiometric dating was performed for the core.

- ## Spatial and identifiers
  - OSGB36_E and OSGB36_N provide precise OSGB36 grid coordinates for each core site.
  - WBID links the record to the broader Lakes index for cross-referencing.
  - UCL_Code and UCL_Sample_ID provide internal identifiers for sample tracking and database integration.

- ## Dating information
  - 210 Pb dating status captured as Yes/No, indicating whether a 210Pb chronology was established for the Hydroscape lake core.

- ## Usage notes and provenance
  - Metadata supports data integration, mapping, and user-friendly access to core sample information.
  - Facilitates cross-dataset verification (WBID, coordinates, depth, Secchi, core details) and enables data consumers to assess dating status and provenance of each core sample.