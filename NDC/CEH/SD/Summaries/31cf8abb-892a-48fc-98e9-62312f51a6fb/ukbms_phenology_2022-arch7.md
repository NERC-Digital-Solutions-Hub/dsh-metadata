# UK Butterfly Monitoring Scheme phenology data download

- Purpose and scope
  - Provides phenology data for butterflies across the UK derived from the UK Butterfly Monitoring Scheme (UKBMS).
  - UKBMS is a long-running, site-based monitoring program funded by Butterfly Conservation, CEH, BTO, and JNCC, with data contributed by volunteers.
  - Data support understanding of butterfly population changes and policy-relevant biodiversity trends.

- Data sources and sampling framework (GIS-relevant context)
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, weekly counts (April–September, up to 26 visits/year) at sites chosen by recorders.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares, two parallel transects, 2–3 visits/year (July–August, plus spring visits encouraged).
  - Targeted surveys: single-species transects and other methods (timed counts, egg/larval web counts) focused on specific species.
  - Spatial coverage: >2000 standard transect sites annually; over 3000 actively recorded sites in recent years.
  - Spatial data included: SITENO (site ID), SITENAME, GRIDREF (6-figure OS grid reference), enabling GIS joins to spatial layers.

- Nature of the data (phenology metrics)
  - Phenology refers to timing of adult butterfly flight periods (imago stage) on UKBMS transects.
  - Metrics available:
    - FIRSTDAY, LASTDAY: day numbers after April 1 of first/last records for a brood at a site/year.
    - PEAKDAY, PEAKCOUNT: day and count of maximum abundance for a brood.
    - MEAN_FLIGHT_DATE: weighted mean date of counts for a species/site/year/brood.
    - FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE: variability and duration of the flight period.
  - Brood handling:
    - NUMBER_OF_BROODS and BROOD indicate if data are for entire flight period (0) or a specific brood (1 = first, 2 = second).
    - For certain multivoltine species, separate first/second flight periods are provided; for bivoltine and some uni-/multivoltine species, data limitations may affect separation.
  - Coverage limitations:
    - Phenology metrics are derived from standard transects with weekly counts; WCBS data are not used for phenology calculations.
    - Some species have limited ability to separate multiple generations due to overlapping flight periods.

- Data quality control and validation
  - Field data recorded on standard forms; entered online (UKBMS MyData) or via Transect Walker.
  - Automatic checks during entry flag anomalies (e.g., unusually high counts, counts outside flight period).
  - Regional transect coordinators review records; additional automated/manual validation checks for out-of-range records, new site records, unusual abundances, or records outside known distributions.
  - Data edits and clarifications implemented through queries and coordination with recorders.

- Details of this data download (CSV schema)
  - Format: comma-separated values (.csv).
  - Columns include:
    - SITENO: unique UKBMS site number
    - SITENAME: site name
    - GRIDREF: OS grid reference for site (typical 6-figure accuracy)
    - SPECIES_NAME: scientific name (following standard taxonomic references)
    - COMMON_NAME: common name
    - YEAR: year of metric calculation
    - NUMBER_OF_BROODS: number of distinct flight periods recorded for that species at the site/year
    - BROOD: 0 = entire flight period; 1 = first brood; 2 = second brood
    - FIRSTDAY, LASTDAY: day numbers after 1 April for first/last record of brood
    - PEAKDAY, PEAKCOUNT: day and count of peak abundance
    - MEAN_FLIGHT_DATE: weighted mean day after 1 April
    - FLIGHTPERIOD_SD: standard deviation around mean flight date
    - FLIGHTPERIOD_RANGE: days between first and last record
  - Special notes:
    - For 13 species, data are available for the entire flight period and, where possible, for two distinct flight periods per year/site.
    - For other species, data are available for the entire flight season only.

- Licensing and attribution
  - Open Government Licence (OGL) allowing free use and reuse with few conditions.
  - Required attribution includes the dataset citation (DOI in metadata) in publications using the data.
  - Attribution statement to accompany derived information/images: Contains UKBMS data © Butterfly Conservation, CEH, BTO, JNCC.

- Collaboration and contact
  - UKBMS partners offer advisory support and interpretation of outputs.
  - Potential for co-authorship or intellectual input on publications, conferences, or posters resulting from UKBMS data use.
  - Primary contacts:
    - Marc Botham (UKBMS) at ukbms@ceh.ac.uk
    - Butterfly Conservation transect coordinator at transect@butterfly-conservation.org

- GIS-specific usage notes and recommended workflow
  - Prepare spatial data:
    - Use GRIDREF to geolocate sites and align with UK basemaps or regional GIS layers.
    - Consider converting GRIDREF to geographic coordinates (e.g., OSGB36 / WGS84) for standard GIS workflows.
  - Join and map:
    - Link phenology records to site polygons or point features to visualize spatial-temporal patterns by species, year, and brood.
  - Analysis considerations:
    - Use FIRSTDAY/LASTDAY/PEAKDAY to analyze shifts in flight timing and duration across space and time.
    - Incorporate MEAN_FLIGHT_DATE and FLIGHTPERIOD_SD to assess synchrony and generation overlap.
    - Be mindful of data limitations: standard transects drive phenology metrics; WCBS data are not used for phenology calculations; generation separation is constrained for overlapping species.
  - Data integration tips:
    - Align with other biodiversity layers (land cover, habitat types) to explore drivers of phenology changes.
    - Validate spatial precision against site coordinates and cross-check notable outliers with regional coordinators.

- End-user guidance
  - This dataset enables creation of map-based representations of butterfly phenology across the UK, informing policy-relevant biodiversity assessments and public-facing visualisations.