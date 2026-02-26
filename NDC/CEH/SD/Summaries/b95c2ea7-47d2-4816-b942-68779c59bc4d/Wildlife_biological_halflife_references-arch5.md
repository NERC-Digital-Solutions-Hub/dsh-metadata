# References for biological half-life database

## Overview
- A comprehensive bibliography of studies on radionuclide bioaccumulation and biological half-life across aquatic and terrestrial organisms.
- Covers uptake, tissue distribution, depuration, and transfer pathways for a wide range of radionuclides (e.g., Cs-137, Co-60, Mn-54, Ag-110m, 239+240Pu, 241Am, Zn-65, Sr-90, I-131, Tc isotopes, etc.).
- Includes diverse taxa: fish (rainbow trout, carp, salmon, eel, catfish, tuna), molluscs (mussels, oysters, clams), crustaceans, invertebrates (Daphnia, Chironomus), birds, mammals, earthworms, amphibians, and reptiles.
- Data originate from both controlled experiments and in situ studies, with some material dating from the 1960s through the 2010s.
- Sources are multidisciplinary and in multiple languages (French, Russian, Japanese, Portuguese, etc.), reflecting the historical breadth of radiological ecology research.

## Dataset scope and content
- For each radionuclide-organism pair, the references contribute information on:
  - Biological half-life (time to depurate or eliminate a radionuclide from the organism).
  - Uptake kinetics (from water and/or diet) and depuration processes.
  - Tissue distribution and organ-specific retention.
  - Transfer from environment to organisms and through food chains.
- Data types include kinetic rates, equilibrium concentration factors, and depuration curves; some entries focus on the effects of environmental factors (temperature, salinity, diet) on uptake and retention.
- The compilation includes primary data sources such as journal articles, conference proceedings, and doctoral theses, with some focus on Chernobyl and Fukushima contexts, as well as general radiological ecology.

## Metadata, standards, and data quality
- To support Data Stewards, the dataset requires standardized metadata for comparability, including:
  - Radionuclide identifier (isotope), chemical form, and energy/half-life context.
  - Species (scientific name) and, when relevant, selected tissues or compartments.
  - Exposure route (water, diet, sediment) and environmental conditions (temperature, salinity, pH, diet composition).
  - Measurements (biological half-life, uptake rate, depuration rate) with units and time scales.
  - Experimental design (laboratory vs. field, duration, sample size) and reference details (authors, year, journal/book, DOI).
  - Language of the original source and any translation notes; access rights or licensing status.
- Given the long span and multilingual nature of the references, harmonization of units, forms of radionuclides, and taxonomic nomenclature is essential.
- Data provenance should trace each numeric value to its source with bibliographic identifiers and, when possible, persistent identifiers (DOIs).

## Access, sharing, and reuse considerations
- The bibliography serves as a foundation for constructing a biological half-life dataset; practical reuse requires:
  - Linking numeric data to their original publications with clear provenance.
  - Documenting any data extraction decisions, conversions, or standardizations performed.
  - Recording licensing or usage restrictions of each source.
  - Providing versioning to accommodate updates as new studies are added.

## Challenges and gaps (from a data stewardship perspective)
- Language barriers and access to older, non-digitized sources (French, Russian, Japanese).
- Heterogeneity in experimental designs, environmental conditions, and measurement methods.
- Inconsistent or missing metadata in older references (e.g., precise exposure routes, environmental parameters, or tissue-specific data).
- Variability in units and radionuclide forms across studies, complicating cross-study comparisons.
- Gaps in coverage for certain species or radionuclides, leading to incomplete pictures of biokinetic behavior.

## Recommendations for data stewardship
- Develop a standardized metadata schema for biological half-life data, including:
  - Core fields: radionuclide, activity form, organism, tissue, exposure route, environment, biological half-life, uptake/depuration rates, units, time scale, method, and source.
  - Provenance fields: full bibliographic citation, DOI (if available), language, and access rights.
  - Quality indicators: data reliability, experimental context (lab vs. field), sample size, and any notable uncertainties.
- Create controlled vocabularies for species (mappings to accepted taxonomic identifiers), tissues, exposure routes, and environmental conditions.
- Implement a data extraction template to consistently capture numeric values (e.g., half-life in days/weeks) and contextual metadata.
- Establish processes for data cleaning, unit harmonization, and form-agnostic comparisons (e.g., converting all half-lives to a common time unit, annotating chemical forms where possible).
- Maintain data lineage and versioning; document all transformations and updates, including when newer studies supersede older estimates.
- Prioritize digitization and cataloging of multilingual sources; consider translations or summaries to improve accessibility.
- Plan for ongoing updates to incorporate new literature (e.g., Fukushima-related data, post-1990s studies) and to reconcile discrepancies among sources.

## Potential data elements to capture (example)
- Radionuclide: Cs-137, Co-60, Mn-54, 110mAg, etc.
- Chemical form: ionic, complexed, particulate (if specified)
- Organism: species with taxonomic authority
- Tissue/compartment: whole body, liver, muscle, gill, etc.
- Exposure route: waterborne, diet, sediment
- Environment: temperature, salinity, pH, diet composition
- Biological half-life: value with units (days, hours)
- Uptake rate: per unit time (optional)
- Depuration rate: per unit time (optional)
- Data type: kinetic rate, transfer coefficient, equilibrium bioaccumulation factor
- Measurement method: radiometric technique, whole-body counting, etc.
- Source: bibliographic citation, DOI, language
- Quality/uncertainty: confidence level or error estimate
- Versioning/date of data extraction

## Implications for users and workflows
- The assembled references underpin dose assessment models and environmental risk evaluations by providing species- and radionuclide-specific biokinetic parameters.
- A well-curated, standardized, and openly accessible dataset enhances cross-study comparisons, meta-analyses, and transparent uncertainty quantification.
- Robust governance around updates, provenance, and metadata quality will improve long-term usability for researchers, regulators, and data users.