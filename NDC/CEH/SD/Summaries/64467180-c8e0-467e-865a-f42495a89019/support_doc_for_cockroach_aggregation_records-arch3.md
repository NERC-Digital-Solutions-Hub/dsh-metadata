# What has been recorded and what form does the data take?

- Subject and experimental setup
  - Records of social aggregations among female cockroaches (Blaptica dubia).
  - Four groups of 24 individuals each, housed in boxes with four shelters and fixed cameras over each shelter.
  - Four humidity conditions: 50%, 40%, and 30% relative humidity; each condition applied for four days per week across three weeks.
  - Experiment repeated with random regrouping, yielding four replicates in total.
  - Incubator environment: 28°C with lights on; cameras (Akaso V50) fixed above shelters.

- Data collection and capture
  - Each shelter’s camera captured one photograph every minute.
  - Cockroach identities were detected from photos using a custom program (image_to_assoc) based on registered dorsal tags.
  - Each photograph (aggregation) has a unique identifier; each cockroach in a group has a unique tag.

- Data records and storage
  - 192 CSV files total: four replicates × three weeks × four days × four groups per day.
  - File length varies (1378 to 3719 lines) due to differing numbers of detectable individuals per photograph.
  - Records are stored per shelf, per day, per week, per replicate (one folder per shelf per day per week per replicate).

- Data processing and quality control
  - Tag detections from photographs processed with confidence scores; detections below 0.95 were removed.
  - To standardise across cameras, only the first 200 photographs from each camera were used (first 200 minutes of each trial).
  - Aggregations from the four cameras within a box are combined to form the group’s aggregations over 3 hours 20 minutes.

- Metadata and file structure
  - Files named to reflect experimental structure: S1_R1_WK1_1_001.csv (Shelf 1, Replicate 1, Week 1 (50% humidity), Day 1, file index 001).
  - Each aggregation/photo reference appears as V1 in the CSV (format: A1_R1_WK1_1_001.JPG) replicating the camera, replicate, week, day, and aggregation number.
  - V2 contains the cockroach tag (from the 24-character set); V3 contains the detection confidence (0.95–1 or NA if no detections).

- Data content per line and organization
  - Each line represents a single detected individual within an aggregation; thus, a single photograph may yield multiple lines (one per detected cockroach).
  - Over time, an individual may appear in up to 200 photographs and appear in multiple lines.
  - The three-column format (V1, V2, V3) captures: aggregation identifier, cockroach tag, and detection confidence.

- Responsibilities and provenance
  - Data collection and initial interpretation conducted by Callum McLean (research associate) and David Fisher (principal investigator).
  - Purpose: to study the evolution and plasticity of social network traits and how social positions adapt to varying humidity.