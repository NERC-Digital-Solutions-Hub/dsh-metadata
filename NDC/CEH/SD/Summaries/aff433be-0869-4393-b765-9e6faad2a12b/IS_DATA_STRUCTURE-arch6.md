# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

## Overview

- ECN Data Centre is the originator and is part of the UK Environmental Change Network (ECN) programme, sponsored by a consortium of UK government departments and agencies.
- The dataset focuses on environmental change monitoring and provides annual measurements of spittlebug (philaen species) nymph densities and adult colour morph proportions across ECN sites.
- Data usage requires acknowledgement of ECN datasets and submission of one reprint of any publication citing these data.
- Protocols ensure comparability across sites; an accompanying document (is.pdf) explains data collection methods.

## Dataset Owners and Sponsorship

- Dataset Owners: The UK Environmental Change Network (ECN) programme.
- Sponsors: A consortium including Agri-Food and Biosciences Institute; BBSRC; Natural Resources Wales; DSTL; Defra; Environment Agency; Forestry Commission; Welsh Government; Natural England; NERC; Scottish Environment Protection Agency; Scottish Government; Scottish Natural Heritage, among others.

## Purpose and Scope

- Purpose: Enable analysis of insect sampling data to derive indices of nymph density and adult colour morph proportions, supporting ecological research and data-driven decisions.
- Scope: Data are collected annually using standardized protocols to allow cross-site comparability.

## Protocol and Quality Assurance

- Standard Operating Procedures (SOPs) are in place to ensure data comparability across sites; see accompanying is.pdf for collection methods.
- Quality information is recorded by site managers and included in the data downloads; unusual events are flagged with quality code 999 and described in qtext documentation.

## How to Use the Data

- Use the nymph data (ECN_ISN.csv) to estimate nymph density indices and track morph-related metrics; use the adult data (ECN_ISA.csv) to analyze adult colour morph proportions.
- Each record includes site, location, sampling date, species/morph code, field variable, and measured value.
- Quality codes (Q1–Q8) accompany each record to indicate data quality factors; detailed explanations are in the supporting quality text files.

## Data Download and Structure

- Nymph data: ECN_ISN.csv
  - Key fields: SITECODE (site), LCODE (location within site), SDATE (sampling date), ISN_SPEC (P = Philaenus spumaris; N = Neophilaenus lineatus), FIELDNAME (variable measured), VALUE (measurement).
- Adult data: ECN_ISA.csv
  - Key fields: SITECODE, LCODE, SDATE, ISA_MORPH (adult colour morph), FIELDNAME, VALUE.
- Supporting documentation:
  - ECN_ISN_qtext.csv (quality text for nymph data)
  - ECN_ISA_qtext.csv (quality text for adult data)
- Quality codes: Standard ECN quality codes with multiple entries per record (Q1–Q8); 999 indicates an unusual event with accompanying text.

## Explanatory Information

- Site Codes:
  - T01–T12 with site names (e.g., Drayton, Glensaugh, Hillsborough, etc.) and precise coordinates.
- Variable Being Measured (FIELDNAME):
  - 1–40 correspond to numbers of spittles in quadrats (varied quadrat counts) with units (primarily counts).
  - Additional fields include NSPITCHK (random throw exercise counts), MEANNYM (mean nymphs in random throws), NMAL/NFEM/NTOT (male/female/total adults by morph), and Q1–Q8 quality metrics.
- Adult Colour Morphs:
  - Codes such as ALB, FLA, GIB, LAT, LCE, LOP, MAR, POP, PRA, QUA, TRI, TYP, UUU with corresponding descriptive names (e.g., Albomaculata, Flavicollis, etc.).
- Quality Codes:
  - Ranging from 100 to 513, plus 999 for unusual events; categories cover issues such as no information, sample loss, partial loss, contamination, environmental disturbances, equipment issues, and measurement anomalies. Full descriptions are provided in the dataset documentation.

## Access and Attribution

- Detailed site and variable information is provided to enable precise data integration and analysis.
- For additional context on site metadata, see the ECN site catalogue link: https://catalogue.ceh.ac.uk/id/813712d4-d1624ede-aff8-cf1c337bdc27

## Notes for Data Support and Reuse

- When using these datasets, ensure proper acknowledgement of ECN data and reference the associated quality notes for data reliability.
- Review the accompanying is.pdf for collection methodology to inform processing and harmonization steps across sites.