# Pollinator effectiveness in oilseed rape ( Brassica napus L.) in relation to behavioural and morphological characteristics .

- Purpose of the dataset
  - Assess the number of pollen grains delivered in a single visit by a variety of pollinators to oilseed rape (Brassica napus L.).
  - Record behavioral and morphological data for a subset of visits to identify traits linked to improved pollen delivery.
  - Enable integration with other Wessex BESS datasets, especially landscape-scale pollinator surveys.

- Field and study context
  - Location: Wiltshire, UK (central point 51.185988° N, -1.832657° W).
  - Timeframe: April–June, 2014–2016, across three field seasons.
  - Site pool: 15 fields of winter sown oilseed rape.

- Data collection and experimental design
  - Flower inspection and sampling: OSR flowers checked for ripe anthers and receptive stigmas; suitable flowers collected with minimal pollen transfer.
  - Visitor handling methods:
    - Bouquet method for solitary bees, bumblebees, and honeybees.
    - Plastic box method for beetles, flies, and sawflies.
  - Field measurements per flower visit:
    - Visit duration (seconds) and visit type (probing, crawling, short).
    - Post-visit collection of the visitor for lab analysis.
  - Controls: Non-visited (control) flowers processed to assess baseline pollen on stigmas.

- Measurements and outcomes
  - Pollen deposition (SVD): Stigmas were processed to count total pollen grains deposited during a visit.
  - Pollen loads on bodies: Swabbing of body parts (head, thorax, legs, etc.) with fuchsin jelly to quantify free pollen carried on the body.
  - Morphological traits: 
    - Body length (distance from eyes to abdomen tip).
    - Intertegular distance (ITD) where available; proxies used for certain beetles.
    - Hair density on the thorax (percentage) and hair type (branched, smooth, or no hair).
  - Additional data captured:
    - Species/visitor identity and groupings, method used, and detailed visit-type descriptors.
    - Pollen counts by body part (Back, Feet, Head, Under) from pollen swab data.

- Data quality and structure
  - Protocols: Standardized field and lab procedures with dedicated datasheets; training provided.
  - Data management: Entered in MS Access; anomaly checks performed.
  - Files:
    - NERCPollinatorEfficiency
    - NERCPollenSwab
  - Data linkage: Datasets can be linked via PollinatorID; pollen swab data capture multiple body parts and can be mapped to pollinator efficiency observations.

- Data quality notes and missing data
  - Missing data: PollinatorID 94 could only be identified to genus; some morphological fields incomplete.
  - Taxonomic and measurement details: Species codes and descriptions defined; some measurements (e.g., ITD proxies) require averaging across individuals.
  - Swab limitations: Tarsi of small beetles could not be swabbed; seven NA values for feet in one dataset.
  - Data fields include comprehensive metadata for traceability (dates, methods, visit types, body parts, and measurements).

- Practical uses for monitoring and analysis
  - Evaluate pollination effectiveness across pollinator groups and species in OSR systems.
  - Analyze relationships between behavioral/morphological traits and pollen delivery efficiency.
  - Integrate with landscape-scale pollinator surveys to assess spatial drivers of pollination services.
  - Support environmental health monitoring by providing standardized, time-stamped records of pollinator-mediated pollen transfer.

- Context for reuse
  - Dataset designed to be used with the broader Wessex BESS pollinator datasets, enabling cross-study, landscape-scale analyses.
  - Data are organized with clear fields and a data dictionary, supporting reproducible monitoring and policy-relevant evaluations.