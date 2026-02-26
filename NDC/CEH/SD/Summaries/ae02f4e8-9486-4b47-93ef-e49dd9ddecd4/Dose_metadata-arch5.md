# A 'Reference Site' in the Chernobyl Exclusion Zone: radionuclide and stable element data, and estimated dose rates

## Overview
- Metadata description for a RADIONUCLIDE and dose-rate dataset hosted by the NERC-Environmental Information Data Centre.
- Focuses on a reference site in the Chernobyl Exclusion Zone, including radionuclide and stable element data and estimated dose rates.
- File set includes four CSV files related to external, internal, total dose, and dose per radionuclide for various biota.

## Datasets and files
- Biota_external_dose.csv
- Biota_internal_dose.csv
- Biota_total_dose.csv
- Biota_total_dose_per_radionuclide.csv

## Data schema and key fields
- Radionuclide: Nuclides examined (e.g., Cs-137, Sr-90, Am-240, Pu-239, Pu-240 or Pu-238).
- Explanation: Radionuclide examined (textual description).
- Units: Unit descriptions for fields (e.g., External_Dose_Rate_microGy_h-1; may be blank for some entries).
- External_Dose_Rate_microGy_h-1: Dose-rate data with statistical summary fields:
  - Mean, Variance, 5th Percentile, 95th Percentile, Median, Minimum, Maximum, 25th Percentile, 75th Percentile.
- Species metadata (as rows or linked fields):
  - Pinus_sylvestris_wood (pine tree)
  - Agrostis_gigantea (grass)
  - Lumbricus_terrestris (earthworm)
  - Apodemus_agrarius (mouse)
  - Sorex_araneus (shrew)
  - Sorex_minutus (shrew)
  - Apodemus_flavicollis (mouse)
  - Microtus_agrestris_and_Microtus_spp. (mouse)
  - Muscardinus_avellanarius (doormouse)
  - Myodes_glareolus (vole)
  - Bombina_bombina (toad)
  - Bufo_bufo (toad)
  - Pelobates_fuscus (toad)
  - Rana_arvalis (frog)
  - Bombus_and_Xylocopa_spp. (bee)
- Units column for species entries: often not specified (blank in places); a potential target for standardization.

## Data quality and gaps
- Some species/entries have missing or blank Units, indicating incomplete metadata.
- The taxonomy and naming of species should be harmonized to ensure consistent linking across datasets.
- Overall metadata requires verification to ensure complete, machine-readable fields and consistent interval definitions.

## Provenance and accessibility
- DOI provided for the dataset: indicates persistent access and citation traceability.
- Repository: NERC Environmental Information Data Centre (EIDC), supporting discoverability and reuse.
- Data may be subject to standard data-sharing policies, including potential embargoes or disclosure considerations related to sensitive sampling locations.

## Governance and stewardship actions
- Ensure datasets meet standards for accuracy, consistency, metadata completeness, and file formats.
- Provide guidance and tooling to data creators to uphold metadata quality (e.g., explicit Units, Explanation, and standardized species names).
- Document data curation steps and updates to maintain a clear data lineage.
- Upload and catalogue datasets in relevant portals; maintain versioning and update cycles.
- Manage licensing, access controls, and any embargo or sensitivity considerations for the Chernobyl Exclusion Zone data.

## Discoverability and reuse
- The DOI and EIDC hosting support discoverability, citation, and reuse by researchers and data users.
- Dose-rate data across multiple radionuclides and biota enable radiation ecology analyses and risk assessment.

## Challenges and considerations for Data Stewards
- Timely data delivery from multiple data creators and systems.
- Handling diverse formats and large datasets; ensuring interoperability.
- Addressing incomplete user needs depiction to guide data publishing and usability.
- Balancing open data goals with any location-based sensitivity or embargo requirements.

## Recommended next steps for Data Stewards
- Complete and standardize metadata, especially Units for species entries and consistent explanations.
- Harmonize species taxonomy and adopt controlled vocabularies for biota naming.
- Verify radionuclide naming conventions and ensure consistent unit definitions (microGy h-1).
- Establish a clear data submission and update workflow with data creators, including timing and format standards.
- Confirm licensing, access policies, and any embargoes; ensure proper DOIs and dataset landing pages are maintained.