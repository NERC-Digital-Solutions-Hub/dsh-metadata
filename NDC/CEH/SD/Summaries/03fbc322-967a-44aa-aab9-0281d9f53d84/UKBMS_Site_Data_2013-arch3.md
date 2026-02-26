# UK Butterfly Monitoring Scheme (UKBMS)

- Purpose and scope: The UKBMS combines data from over 1,000 sites annually to monitor butterfly population abundance and trends using standardized, repeatable methods designed for long-term assessment.

- Experimental design and sampling regime:
  - All-species transects: Fixed-route line transects (2–4 km) sampled weekly from April to September under predefined weather conditions, recording all butterfly species within a fixed 5 m belt to enable year-to-year comparisons.
  - Method specifics: Transects are chosen to represent habitat types and management activities; routes remain fixed to maintain comparability.
  - Frequency and duration: Typical weekly counts (April–September) with 26 counts per year; 10:45 am to about 3:45 pm with weather-based activity criteria.
  - Single-species transects: Similar to all-species transects but focused on one or a few focal species during selected weeks.
  - Timed counts and egg/larval web counts: Additional methods recording abundance for specific species during set time periods or counting eggs/larval webs in suitable habitats.

- Data collection methods:
  - Field data capture: Site location and transect data recorded in the field and entered into Transect Walker software.
  - Data submission: Transect Walker files are uploaded to an Oracle database; route changes create a new site number and new dataset entry.

- Nature and units of recorded values:
  - Site location data: OS grid reference, transect length (m), number of sections per transect.
  - Grid references: Converted to Easting and Northing coordinates.
  - Some site data may be incomplete.

- Quality control:
  - Regional coordination: Each site belongs to a region with a transect coordinator who validates records.
  - Validation workflow: Preliminary checks followed by automated and manual validation to verify site location and data integrity.

- Format and storage of data:
  - Storage format: Site Location Data stored as CSV.
  - Key columns include: Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. of Sections, No. of Years Surveyed, First Year Surveyed, Last Year Surveyed (with specific details such as 6-figure OS grid references and year ranges up to 2013/2012 for relevant fields).