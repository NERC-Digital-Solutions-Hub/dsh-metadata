# Environmental_Riau.csv

- A collection of biodiversity, environmental, and social survey datasets from smallholder oil palm plantations in Riau, Sumatra, Indonesia. Data cover abiotic conditions, vegetation structure, arthropod and insect activity, pollinator observations, pitfall and sticky trap catches, and plantation management/socio-demographic information.

## Data portfolio and core content

- DataLoggers_Riau.csv
  - Locations and air temperatures recorded by data loggers within plots (T1–T4) and per-hour readings (TempHr1–TempHr25 or similar).
  - Key fields include PlantationCode (Plot ID), SamplePoint (logger location within plot), and hourly temperature measurements with units (°C).
  - Metadata notes: some header lines appear with typographical irregularities; watch for data quality issues in temperature fields and descriptions.

- Inflorescences_Riau.csv
  - Data on oil palm inflorescences, including inflorescence IDs, plot IDs, weather, dates, and times.
  - Pollinator observations recorded on two separate days per inflorescence, with numerous response variables (percent open/partially closed/closed flowers, pollinator taxa counts, ground cover, palm metrics, canopy openness, etc.).
  - GPS linkage via GPSCode to GPSDataRiau.csv.

- Pitfalls_Riau.csv
  - Abundance data for arthropods captured in pitfall traps; taxa are tallied by order/group (e.g., ants, termites, Coleoptera, etc.).
  - Includes trap location, setup/collection dates and times, and notes.

- Transects_Riau.csv
  - Observational data for butterflies, orb-weaving spiders, and assassin bugs, including species, weather, date/time, microhabitat, and behavior counts (flying, resting, etc.).
  - Optional flowering plant associations (FloweringPlantID) for nectar/foraging context.

- Traps_Riau.csv
  - Setup and collection timings for pitfall traps, sticky traps, dataloggers, and bait cards; includes weather during setup/collection, unique identifiers, and counts like mealworms remaining on bait cards.
  - Detailed time stamps (dates and times) for each trap type and sampling point.

- StickyTraps_Riau.csv
  - Abundance data for arthropods captured on sticky traps; counts by taxon (ants, termites, various insect groups), plus total specimen counts and ordinal abundance.

- Environmental_Riau.csv
  - Vegetation, microclimate, and soil condition data for plantation mapping surveys; includes plantation dimensions, neighboring habitats, and GPS-linked coordinates.
  - Detailed measurements across sections: canopy openness (via densiometer and visual estimates), soil moisture/pH, soil horizons, litter depth, vegetation height, crop/bare ground/fern/leaf litter cover, herbivore/contact metrics, and palm health indicators.
  - Extensive metadata on plantation characteristics, neighboring habitats, and grove layout (corners, center, and sampling points with GPS).

- Social_Riau.csv
  - Plantation characteristics, management inputs, and managers’ socio-demographic data; includes landowner details, harvesting and intercropping practices, fertilizer/herbicide use and costs, income, and motivations.
  - Also captures attitudes toward nature and the oil palm industry, and rankings of nature’s economic, food, wildlife, beauty, culture, health, and non-importance values.
  - Extensive respondent metadata (age, gender, education, income, employment, years in location/management, etc.) and farm/land ownership details.

## Metadata standards and data linkage

- Field-level metadata are provided for many columns (Description, Unit, Type) to support data understanding and reuse.
- GPS coordinates are linked across datasets via codes (GPSCode, GPSCodeCorner/T1/T2/etc.) with a central GPSDataRiau.csv file referenced for coordinate retrieval.
- Data across datasets cover both temporal (dates/times for day-of observations, setup, collection) and spatial (plot, sampling-point, palm location) dimensions, enabling integrated analyses.

## Data quality, documentation, and interoperability

- The datasets comprise varied formats and measurement types, emphasizing the need for harmonized metadata and standard vocabularies.
- Noted irregularities in headers and descriptions (e.g., typographical errors, inconsistent line breaks) indicate potential data cleaning needs prior to ingestion into a portal or repository.
- To improve interoperability, consider mapping to a shared standard (e.g., Darwin Core for biodiversity data) and providing a consolidated data dictionary with controlled vocabularies.

## Data governance and sharing considerations

- Data types include sensitive socio-economic information (Social_Riau.csv); assess privacy, consent, and anonymization requirements before sharing.
- Clearly define data access, licensing, and update cadence for the data portal; establish versioning to reflect corrections or re-uploads.
- Data stewardship actions should include:
  - Validation of field names, units, and data types across all files.
  - Resolution of header inconsistencies and missing/ambiguous values.
  - Documentation of data provenance, collection methods, and any embargoed datasets.
  - Consistent cross-dataset linking (GPS, plot IDs, sampling points) to enable integrated analyses.

## Practical guidance for Data Stewards

- Standardize data schemas across all Riau CSVs and publish a centralized data dictionary that aligns with shared metadata standards.
- Implement crosswalks to recognized biodiversity and environmental data standards (e.g., Darwin Core) to facilitate discoverability and interoperability.
- Maintain a master GPS dataset (GPSDataRiau.csv) and ensure all GPSCode fields consistently reference it.
- Develop and enforce data quality checks for:
  - Temperature readings and hourly timestamps in DataLoggers_Riau.csv.
  - Consistency of WeatherCondition, Date, and Time fields in Inflorescences_Riau.csv and Transects_Riau.csv.
  - Taxonomic naming consistency and counting methodologies in Pitfalls_Riau.csv and StickyTraps_Riau.csv.
- For Social_Riau.csv, implement privacy-preserving practices (de-identification where appropriate) and obtain appropriate consent disclosures for data sharing.
- Document data collection protocols, sampling designs, and any deviations to support reproducibility and future data reuse.