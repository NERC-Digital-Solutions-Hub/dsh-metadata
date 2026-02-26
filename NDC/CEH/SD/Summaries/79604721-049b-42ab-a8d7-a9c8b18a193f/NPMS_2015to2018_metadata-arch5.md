# National Plant Monitoring Scheme (NPMS) survey data (2015-2018)

- Purpose and scope
  - NPMS is a habitat-based plant monitoring scheme created by BSBI, CEH, Plantlife and JNCC to annually indicate changes in plant abundance and diversity, support volunteer recorders, and provide data for UK biodiversity indicators.
  - Dataset provides a snapshot of the NPMS database held at CEH Wallingford and supports analyses of habitat change and plant communities across the UK, Isle of Man, and Channel Islands.

- Data assets and file descriptions
  - locations_2015to2018.csv: unique location_id, location_type; links to sampling events.
  - sampleInfo_2015to2018.csv: sample_id, survey_id, date_start, location_id, entered_sref, entered_sref_system, created_on, created_by_id; recorder identifiers (not publicly named).
  - sampleAttributes_2015to2018.csv: sample_attribute_id, sample_id, caption, text_value; additional attributes linked to samples.
  - occurrences_2015to2018.csv: id, sample_id, taxonversionkey, preferred_taxon, domin, record_status, sensitivity_precision; taxon and observation details with verification status.
  - npmsHabitatLookup.csv: mapping between NPMS broad habitats and fine-scale habitats.
  - All datasets connect via location_id, sample_id, and survey identifiers; provide plant occurrence data with abundance (Domin scale) and uncertainty attributes.

- Data model, provenance and standards
  - Linking structure: locations -> sampleInfo -> occurrences; sampleAttributes attaches to samples; taxonomic data referenced by NBN taxon keys; recorder IDs map to unique (non-public) identifiers.
  - Spatial and temporal data: entered_sref with system (OSGB EPSG:27700, Irish Grid EPSG:29902, WGS84 EPSG:4326); date_start and created_on records.
  - Habitat classifications: 28 fine NPMS habitats aggregated into 11 broad categories; habitat codes guide species lists and sampling design.
  - Data capture and validation: online data entry with dictionaries of species, controlled terms, and geographic checks; iRecord verification for expert review; dataset designed to support robust statistical analyses.

- Evidence quality assurance (EQA) and governance
  - QA framework supported by peer-reviewed articles and project reports; Data Management Plan; PRINCE2-based project management; external peer review via Steering Group and expert workshops.
  - Data publishing: scheme data intended to be publicly available for independent review; results analyzed by experienced ecologists; reporting to diverse audiences.
  - Versioning and tracking: all design outputs documented; report versions archived and off-site; explicit tracking of outputs and updates.

- Access, use and rights
  - Data are publicly accessible to enable independent review and use by researchers, policymakers, and the public.
  - If online submission is not possible, forms can be mailed for data contribution.
  - Privacy: recorder identity is anonymized in the public dataset; unique recorder IDs are used to track contributions internally.

- Data management, storage and updates
  - Snapshot maintained for current state; dataset is annually updated as NPMS data accumulate.
  - Data are stored in a spatial database with standardized entry procedures to ensure interoperability and traceability.
  - Documentation and guidance (field recording, plotting, and data entry) are provided to ensure consistency across years and participants.

- Roles, responsibilities and practical stewardship
  - Data Stewards should ensure: understanding of user needs, adherence to NPMS metadata and standards, timely data intake from volunteers, and compliance with data sharing and embargo policies.
  - Ensure accurate linking of locations, samples, and occurrences; maintain plot relocation information; manage updates to habitat classifications and species lists as guidance evolves.
  - Maintain data quality through verification status (C, V, R), handling of sensitive records, and clear provenance for each observation.

- Challenges and considerations for data stewardship
  - Incomplete understanding of user needs and priorities; timely data acquisition from volunteers.
  - Aligning data from multiple systems and formats; handling large datasets; updating outdated databases with interoperable solutions.
  - Ensuring up-to-date metadata, comprehensive documentation, and robust version control across yearly releases.

- Practical guidance for data users and stewards
  - Follow the NPMS guidance for plotting, habitat classification, and Domin scale usage to ensure comparability over time.
  - Use the NPMS Habitat Lookup to interpret habitat categories; respect data quality indicators and verification statuses.
  - Leverage online data entry and support channels (support@npms.org.uk) for data submission issues and access inquiries.

- Appendix: Habitat classifications (high-level)
  - 28 fine NPMS habitats grouped into 11 broad categories (e.g., Arable field margins; Bog and wet heath; Broadleaved woodland; Coast; Freshwater; Heathland; Lowland grassland; Marsh and fen; Native pinewood and juniper scrub; Rock outcrops; Upland grassland).
  - Domin scale for percent cover (1–10) and guidance for converting area to percentage in plots (5x5 m or 1x25 m plots).

- Support and resources
  - NPMS website and guidance documents (survey guidance, species lists, habitat descriptions) available for field method standardization.
  - Contact for data submission and troubleshooting: NPMS support.