# Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021

## Overview
- A structured dataset describing life cycle ecology, phenology, host plant relationships, breeding habitats, morphology, conservation status, and distribution/abundance trends for butterflies and macro-moths of Great Britain and Ireland.
- Comprises six files: ecological_traits.csv, excluded_species.csv, excluded_subspecies.csv, hostplant_list_stacked.csv, hostplant_list_unstacked.csv, ReadMe.rtf.
- The dataset should be cited as: Cook, P.M. et al. (2021). Traits data for the butterflies and macro-moths of Great Britain and Ireland, 2021. NERC EDS Environmental Information Data Centre. DOI: 10.5285/5b5a13b6-2304-47e3-9c9d-35237d1232c6.

## File Descriptions
- ecological_traits.csv
  - Contains life cycle ecology and phenology, host plant specificity and characteristics, breeding habitat, and morphological traits.
  - Includes data on conservation status, distribution (occupancy) trends, and abundance trends.
  - Provides multiple resolution levels for broader categories (e.g., habitat split into sub-categories).
  - Metadata describes how data were derived (refer to ReadMe.pdf).
  - Data formatting includes wide columns (e.g., monthly egg/larval/pupal/adult stages) and various trend indicators.
  - Row count and size: 970 rows, 324 KB.

- excluded_species.csv
  - List of Lepidoptera species from Agassiz, Beavan & Heckford (2013) excluded from the database (primarily adventive or micro-moths).
  - 2022 rows.

- excluded_subspecies.csv
  - List of Lepidoptera subspecies/forms excluded from the database.
  - 276 rows.

- hostplant_list_stacked.csv
  - Raw host plant data from Henwood, Sterling & Lewington (2020); multiple rows per species for multiple hostplants.
  - Hostplants named according to Stace (2019).
  - 4,955 rows.

- hostplant_list_unstacked.csv
  - Table-formatted data from Henwood, Sterling & Lewington (2020); one row per species with hostplants as columns.
  - A cell marked with 1 indicates the species is known to use that hostplant.
  - 798 rows.

- ReadMe.rtf
  - Detailed metadata explaining how each column in the above CSVs was derived and numbered.
  - Includes a full list of references used for the data collation.
  - Contains Table 2 (headers for ecological_traits.csv) and guidance on interpretation.

## Data Fields and Structure (Key Points)
- Header and column metadata (Table 2) explain the meaning and source of data such as:
  - Species identifiers (abh_number, b&f_number), scientific and common names, and family.
  - Distribution and presence (England, Wales, Scotland, Northern Ireland, Republic of Ireland) and status (reintroduced, immigrant, resident).
  - Red List statuses for GB and Ireland, occupancy counts (e.g., 10 km squares), and trends (long/short term distribution and abundance) with significance indicators.
  - Life history and biology details: diurnal/nocturnal activity, overwintering strategies, larval/pupal/adult monthly stages, and larval overwintering specifics.
  - Morphometrics and traits: estimated dry mass, forewing measurements, wing morphology, and other female wing characteristics.
  - Host plant specificity (monophagous, oligophagous by genus or family, polyphagous), hostplant counts, and native/non-native status.
  - Hostplant ecology: Ellenberg indicator values (light, moisture, nitrogen, salinity), habitat sections, and broad host plant categories.
  - Breeding habitat categories and subcategories (e.g., woodland types, grassland, hedgerows, wetlands, montane upland).
  - Pupal and larval overwintering locations (in soil, on hostplant, within plant stems, in leaf litter/moss, etc.) and related confidence levels.
- Geographic boundaries and scope
  - Great Britain: England, Scotland, Wales
  - United Kingdom: GB + Northern Ireland
  - Ireland: Republic of Ireland + Northern Ireland
  - Metadata also notes relevance for Channel Islands and Isle of Man where applicable (especially for trend data)
- Data provenance and timeframes
  - Distribution and occupancy data draw from recording schemes such as BNM (Butterflies for the New Millennium), NMRS (National Moth Recording Scheme), MothsIreland, UKBMS, Rothamsted Insect Survey, etc.
  - Long-term and short-term trends based on occupancy models; certain trends may be blank if not estimable or data are unavailable.
  - Some data reflect historical periods (e.g., 2000–20116) and are presented within the context of cited sources.
- Host plant data
  - Stacked vs. unstacked formats to support different analyses.
  - Hostplant lists linked to Henwood, Sterling & Lewington (2020) and Stace (2019) for plant naming and classification.
- Data quality and caveats
  - Some fields contain uncertainties (e.g., larval overwintering status may be uncertain and marked with '?').
  - Mass estimates are model-derived and should be treated with caution; best for cross-family analyses rather than precise mass determinations.
  - Data boundaries and definitions may vary by source; distribution and trend columns clearly annotate the political/geographic scope.

## Geographic Boundaries and Metadata Details
- Distribution and boundary definitions are explicitly described in the metadata; users should refer to ReadMe for exact scope and column definitions when combining data across GB, Ireland, ROI, Channel Islands, and Isle of Man.
- Trend analyses employ occupancy modeling to account for recording effort; results are tied to the respective data sources (BNM, NMRS, MothsIreland, etc.).

## Usage and Citation
- Intended for researchers and analysts combining trait data with ecological questions, distribution modeling, and hostplant associations.
- Data are accompanied by extensive references and acknowledgment requirements; users should cite the dataset as specified in the ReadMe and accompanying metadata.
- The ReadMe provides guidance on data provenance, column derivations, and how to interpret summarized and monthly data points.

## Acknowledgments and References
- The dataset acknowledges numerous trailing sources (e.g., Agassiz et al. 2013; Eeles 2019; Fox et al. 2015, 2019; Henwood et al. 2020; Stace 2019; Randle et al. 2019) and organizations (Butterfly Conservation, UKBMS, Rothamsted Insect Survey, MothsIreland, etc.).
- A comprehensive references list supports data provenance and methodological context for trait and distribution data.