# The National Plant Monitoring Scheme (NPMS) data package 2015to2020: files and evidence quality assurance

- Purpose and scope
  - NPMS is a habitat-based plant monitoring scheme designed by BSBI, UKCEH, Plantlife and JNCC.
  - Aims: detect change in priority habitats, understand drivers/pressures of change, and contribute data for the UK Biodiversity Indicator C7 (plants of the wider countryside).
  - The dataset provides an annually updated snapshot of the NPMS database held at UKCEH Wallingford.

- Overview of files provided (2015–2020)
  - locationTypes_2015to2020.csv (165 kb)
    - Links a unique location_id to a location_type describing the survey plot (square or linear).
    - location_id connects to the sampleInfoWithLatLong_2015to2020.csv for repeated samples at the same location.
  - sampleAttributes_2015to2020.csv (8490 kb)
    - Additional data about samples, linked by sample_id to sampleInfoWithLatLong_2015to2020.
    - Each row includes a caption and text_value describing the attribute.
  - sampleInfoWithLatLong_2015to2020.csv (2485 kb)
    - Information about individual plant community samples.
    - Fields include id (sample_id), survey_id (sample type: 87 Wildflower, 154 Inventory, 155 Indicator), date_start, location_id, entered_sref, entered_sref_system, created_on, created_by_id, LATITUDE, LONGITUDE, monad, monadCRS, country.
  - occurrences_2015to2020.csv (11689 kb)
    - Records species occurrences observed during sampling visits.
    - Includes id, sample_id, taxonversionkey, preferred_taxon, domin (Domin score), record_status (C, V, R), sensitivity_precision (blurring to protect sensitive records).
  - npmsHabitatLookup.csv (2 kb)
    - Lookup between NPMS broad habitat categories and fine-scale habitats.
  - dominScores.csv (1 kb)
    - Lookup and harmonisation of Domin scores across survey types; includes dominIndex and midPoint for cover categories.

- How to link and access habitat information (example)
  - Use sampleInfoWithLatLong_2015to2020.csv together with sampleAttributes_2015to2020.csv.
  - Filter sampleAttributes where caption is 'NPMS Habitat' and join on sample_id to obtain habitat information for each sample.
  - Example approach (R): merge samples with habitat attributes using an inner/left join on id and sample_id, respectively.

- Evidence Quality Assurance (EQA) and governance
  - EQA is supported by multiple publications and internal guidance to ensure data quality and reliability.
  - Key publications and reports cited for EQA:
    - Pescott et al. 2019; 2016; 2015 (design, models for interval-censored data, and ecological monitoring with citizen science).
    - Additional articles: Walker et al. 2015; Pescott et al. 2015.
    - Reports on NPMS data use for air pollution inferences (2018) and technical reviews (2019).
  - EQA considerations across NPMS:
    - Sample stratification and survey design developed with statistical and botanical experts; random plot design (square grid and linear plots) to reduce landscape bias.
    - Habitat definitions developed through habitat expert peer review.
    - Target species list selected with a method balancing unbiased responses to drivers and suitability for volunteer engagement.
    - Field recording involves volunteers with varying botanical expertise; three levels of contribution; extensive guidance and training; formal field-recording QA not currently part of NPMS but under consideration.
    - Data input and verification via online capture, species dictionaries, standardized dates, spatially precise locations, controlled terms; iRecord verification for expert review of exceptional records.
    - Data publishing planned to be publicly available to enable independent review.
    - Analysis performed by experienced quantitative ecologists using R; results disseminated via NPMS newsletters and peer-reviewed publications.
  - Q&A style governance highlights:
    - Q1: Peer review and involvement of experts in methods/publications; design and testing with statistical and botanical input.
    - Q2: Risk-aware QA with a project Steering Group and external peer review when needed.
    - Q3: Uncertainty, quality, assumptions, and limitations communicated via reviewed outputs; openness to external critique.
    - Q4: Bias avoidance through robust statistical design enabling uncertainty estimation via models.
    - Q5: Document tracking and version control via a Data Management Plan; PRINCE2 project management standards; off-site backups; communication of design outputs and archived versions.

- Practical considerations for analysts
  - The NPMS dataset provides a linkable structure: location_type (locationTypes_2015to2020) -> samples (sampleInfoWithLatLong_2015to2020) -> attributes (sampleAttributes_2015to2020) and occurrences (occurrences_2015to2020).
  - Spatial and temporal context is available through coordinates (LATITUDE, LONGITUDE), monads, and date_start.
  - Data quality is supported by verification systems (iRecord) for expert review and by a governance framework emphasizing documentation, versioning, and model-based uncertainty estimation.
  - Outputs are designed to be publicly available and subject to scientific review, making datasets suitable for independent analysis and replication.

- End notes
  - For further details and up-to-date survey resources, refer to NPMS resources and the evidence QA publications listed in the document.