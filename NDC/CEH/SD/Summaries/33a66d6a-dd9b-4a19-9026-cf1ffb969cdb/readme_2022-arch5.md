# A traits database for the Butterflies and Macro-moths of Great Britain and Ireland

## Overview
- A six-file dataset describing life cycle traits, host plant associations, distribution and abundance indicators for Lepidoptera in Great Britain and Ireland.
- Core components: ecological_traits (traits across life stages, ecology, morphology, distribution), hostplant_list_stacked and hostplant_list_unstacked (larval hostplants in two formats), plus excluded_species and excluded_subspecies lists.
- Includes ReadMe with metadata explanations, data provenance, and a formal citation requirement for use in publications.

## Files in the dataset
- ecological_traits.csv (Format: CSV; Size: 293 KB; 970 rows)
  - Life cycle ecology, phenology, host plant specificity, breeding habitat, morphology, conservation status, distribution and abundance trends.
  - Data are tied to political boundaries; metadata explains the scope (Great Britain, United Kingdom, Ireland, etc.).
- excluded_species.csv (Size: 97 KB; 2022 rows)
  - Lepidoptera species excluded from the database (mainly adventive or micro-moth species).
- excluded_subspecies.csv (Size: 19 KB; 276 rows)
  - Lepidoptera subspecies/forms excluded from the database.
- hostplant_list_stacked.csv (Size: 179 KB; 4955 rows)
  - Raw hostplant data from Henwood, Sterling & Lewington (2020); multiple rows per species for multiple hostplants.
- hostplant_list_unstacked.csv (Size: 612 KB; 798 rows)
  - Each species in a single row with hostplants as columns; binary indicators denote known usage.
- ReadMe.docx (Size: 286 KB)
  - Detailed methodology, column derivation, and data sources; includes Table 1–6 headers mapping and references.

## Metadata and header information
- Headers and data mapping are documented in ReadMe and Table 2 (ecological_traits.csv), including how merged headers are represented in the data.
- Political boundary definitions used in the dataset:
  - Great Britain: England, Scotland, Wales
  - United Kingdom: GB plus Northern Ireland
  - Ireland: island including Northern Ireland and the Republic of Ireland
  - Specific notes mention the Republic of Ireland, Isle of Man, and Channel Islands where relevant to trend data.
- Key data columns capture presence/absence, statuses, and movements (e.g., recorded_present, reintroduced, immigrant, resident, extinct_gb, red_list_gb/ireland, 10 km squares, distribution and abundance trends).
- Life cycle and phenology are captured with monthly indicators for egg, larva, pupa, and adult stages, plus overwintering strategies.
- Habitat, hostplant specificity, and hostplant categories are detailed, including native status, Ellenberg values for hostplants, and broad/narrow hostplant classifications.
- Data use conventions (e.g., 1 indicates presence or affirmative status; other codes such as 2, 3, or ? indicate partial, uncertain, or conditional data) are described, with caveats for certain columns (e.g., latitudinal differences in phenology not accounted for).

## Data provenance and sources
- Data compiled from multiple authoritative sources, including:
  - Agassiz, Beavan & Heckford (2013)
  - Henwood, Sterling & Lewington (2020)
  - Waring & Townsend (2017)
  - Emmet & Heath (1991, 1992)
  - Hill et al. (1999) for Ellenberg indicators
  - Rothamsted Insect Survey and UKBMS for distribution/abundance trends
  - National Moth Recording Scheme (NMRS), MothsIreland, and other regional datasets
- Acknowledgments to primary data authors and publishing bodies; permission noted for incorporating raw hostplant data.

## Citation and reuse
- The dataset must be cited as:
  Cook, P.M., Tordoff, G.M., Davis, A.M., Parsons, M.S., Dennis, E.B., Fox, R., Botham, M.S., Bourn, N.A.D., 2021. A traits database for the Butterflies and Macro-moths of Great Britain and Ireland. Butterfly Conservation & Centre for Hydrology and Ecology, United Kingdom.

## Data quality, limitations, and governance
- Strengths: integrated trait data across life stages, hostplant associations, distribution and trends, with cross-referenced sources and detailed metadata.
- Limitations and challenges:
  - Data come from diverse sources with varying political boundaries and timeframes; some trends and distributions are region-specific.
  - Latitudinal variation in phenology is not accounted for in certain columns.
  - Some data, especially life-cycle stages and overwintering, use varying levels of certainty (e.g., '?' markers, partial generations).
  - Excluded taxa (adventive or micro-moths) are not included, which may affect completeness for some users.
- Governance aspects aligned with Data Stewards aims:
  - Clear metadata, cited sources, and a formal data-use citation.
  - Structured formats (CSV and ReadMe) to facilitate discoverability, reuse, and update workflows.
  - Documentation of data derivation criteria and hostplant taxonomy (Stace 2019 references) to support consistency and interoperability.

## Acknowledgments and references
- Extensive acknowledgments to data providers and referenced literature (e.g., Henwood et al. 2020; Randle et al. 2019; Emmet & Heath 1992; Fox et al. 2019; NMRS; MothsIreland; Stace 2019; Hill et al. 1999).
- References section includes key taxonomic checklists, red lists, monitoring schemes, and field guides that underpin the dataset content.