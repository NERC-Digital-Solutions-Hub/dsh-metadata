# hydroscape_lakedistrict_core_metadata.csv

- Metadata file for Hydroscape Lake District lake sediment cores uploaded to EIDC.
- Provides standardized fields to identify cores, locate sampling sites, and describe core characteristics and dating status.
- Links and references:
  - WBID: Waterbody Identification number with link to UK CEH Lakes platform.
  - Hydroscape: Name of the Hydroscape region used.
  - Core collection and coring references available for corer types.

## Key fields and definitions

- WBID: Waterbody Identification number identifying the lake/core site.
- Hydroscape: Name of the Hydroscape region used for the dataset.
- Name: Lake name.
- General_location_of_core: Core location category within the lake (deep central, littoral near vegetation margin, or intermediate mid-depth).
- OSGB36_E: Easting coordinate in OSGB36 (UK National Grid).
- OSGB36_N: Northing coordinate in OSGB36 (UK National Grid).
- Water_depth_at_core_site_(m): Water depth from surface to sediment at the core site; measured with a hand-held echo sounder from a boat; littoral depths corroborated by Secchi depth.
- Secchi_disc_depth_(m): Secchi depth measured prior to coring; three measurements taken, mean calculated; recorded at the deepest lake position.
- Core_length_and_type: Core length in metres and the corer type used (Tapper, Big Ben, Livingstone, Renberg) with referenced literature for operation.
- Date_core_collected: Date of fieldwork and core collection (dd/mm/yyyy).
- UCL_Code: Internal UCL code used on bags/databases.
- UCL_Sample_ID: Internal Amphora code for the entire sample core (unique ID).
- 210_Pb-dated_Y_N_for_Hydroscape: Indicates whether the core has been dated using ^210Pb (Yes or No).

## Data collection and methods

- Core depth and location:
  - Depths recorded at the core site with a hand-held echo sounder; Secchi depth used to validate littoral depths.
  - Geographic coordinates provided in OSGB36 datum (E/N).
- Core description:
  - Core length and the specific corer used are documented, with references to coring methods for reproducibility.
- Dating status:
  - A clear Yes/No field indicates if ^210Pb dating was performed for quality assurance and chronological context.

## Data quality, provenance, and use

- Dataset is structured for standardised environmental monitoring outputs and compatibility with data portals.
- Includes internal identifiers (UCL_Code, UCL_Sample_ID) to support dataset linking and provenance tracking.
- Designed to enable data verification, cleaning, and potential integration with other Hydroscape or lake core datasets.

## Access, reuse, and integration

- Metadata enables consistent interpretation and re-use in environmental health and policy monitoring.
- Facilitates combination with other datasets to enhance the value of monitoring outputs and support broader data analyses.
- Intended for storage and upload to appropriate data portals to support open access and interoperability.