DATA HEADER INFORMATION for Site_description_Ankeniheny_Zahamena_forest_corridor_Madagascar.csv

## Overview
- Describes topographical characteristics of sampling sites in the Ankeniheny-Zahamena forest corridor, Madagascar.
- Part of ESPA programme and P4GES project; DOI provided for dataset.
- Acknowledgement required for products derived from these data to Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Provenance and Access
- Data originate from ESPA/P4GES activities; site codes use the P4GES site_ID.
- Related documentation: Manual_1_Classical_Survey; dataset references DOI.
- Data sharing and publication should respect acknowledgement requirements; details on access/embargo are not explicit, but governance should ensure proper licensing and attribution.

## Data Scope and Structure
- Dataset captures topographical characteristics at each site and sampling point location.
- Key fields include: site_ID, ZOI (zone of interest), Location, LU (land use), Type (Plot vs Transect), and precise geographic coordinates (X, Y), altitude, and GPS precision.
- ZOI categories: ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana, ZOI4 Didy.
- Coordinate system: WGS84 decimal degrees (Longitude X, Latitude Y).

## Metadata and Standards to Enforce
- Field definitions and types are specified (e.g., Text, Numeric, Categorical).
- Units are explicit for numeric fields (e.g., X and Y in decimal degrees, Altitude in meters, Precision in meters, slope in degrees).
- Instrumentation noted: GPS eTrex 30 Garmin; Sunnto MC-2 compass and Mirror Clinometer for slope measurements.
- Data creators and contributors should ensure metadata completeness (values, units, field resources) and alignment with dataset’s publishing standards.

## Data Capture, Quality Assurance, and Transformation
- Data are received from field teams (e.g., locals, botanists, local guides) and may require chasing up.
- Steps implied: QA, cleaning, and transformation prior to sharing; ensure consistency across formats and systems.
- Type field indicates whether a site is a Plot or Transect, aiding in standardization and interoperability with other work packages.

## Data Availability, Updates, and Governance
- Sharing limitations and embargoes should be identified and respected; systems should be in place to manage updates.
- Datasets should be uploaded to relevant portals and catalogued within data holdings.
- Documentation of work conducted on datasets is recommended to support repeatability and reuse.

## Usage Restrictions and Acknowledgement
- Explicit acknowledgement requirement for products derived from these data to the Laboratoire des Radio Isotopes (Université d’Antananarivo).

## Key Fields and Values (highlights)
- site_ID: P4GES site code (Text)
- ZOI: Zone of Interest (Categorical: ZOI1–ZOI4)
- Location: Sampling point location name (Text)
- LU: Land use type (Categorical: Closed Canopy, Tree Savoka, Shrub Savoka, Degraded Land)
- Type: Plot or Transect (Categorical)
- X: Longitude (Numeric, decimal degrees, WGS84)
- Y: Latitude (Numeric, decimal degrees, WGS84)
- Altitude: Elevation in meters (Numeric)
- Precision: GPS precision in meters (Numeric)
- slope_up / slope_down: Slope measurements in degrees (Numeric)
- topographic_position: Position on slope (Text: Mid side, High side, Low side)
- age_of_deforest: Estimated deforestation age (Numeric, years)
- age_of_fallow: Estimated fallow age (Numeric, years)
- Historic: Historic context from local interviews (Text)

## Challenges and Considerations for Data Stewards
- Addressing an incomplete picture of user needs and priorities.
- Ensuring timely data delivery from field teams.
- Achieving consistency with metadata and standards across diverse systems and formats.
- Handling large datasets and potentially non-interoperable, legacy databases.
- Maintaining up-to-date data and managing data sharing restrictions across portals.