# Soil dates using radiocarbon in profiles from permafrost in subarctic Canada

## Overview
- Radiocarbon dating of soil core samples from permafrost in subarctic Canada.
- Site codes and meanings:
  - FFU - FireFox Unburnt (unburnt black spruce forest)
  - FFB - FireFox Burnt (burnt in 1998)
  - TPP - Teslin Peatland Plateau (peatland plateau near Teslin)
  - TW - Teslin Wetland (thawed peatland plateau)
  - MCU - Mosquito Creek Unburnt (unburnt black spruce forest)
  - MCB - Mosquito Creek Burnt (burnt black spruce forest)
  - WTP - White Truck Plateau (peatland plateau near Yellowknife)
  - WTM - White Truck Moss (recently thawed peatland plateau with moss)
  - WTS - White Truck Sedge (recently thawed peatland plateau with sedge/moss)
  - WTW - White Truck Wetland (older potential collapse feature in thawed peatland)
- Sample depth chosen based on criteria described in the column "Explanation."
- Bulk samples were taken from each soil core; plant macrofossils identified when possible using microscopy and selected for analysis.
- Samples sent to the NERC Radiocarbon Facility in East Kilbride, UK for analysis; results assigned a publication_code.
- Radiocarbon enrichment values are expressed as percent modern carbon.
- Ages are reported as conventional radiocarbon age in years BP (present defined as AD 1950).

## Dataset content and structure
- Core fields include: site code, depth, Explanation (depth criteria), Description_of_sample (plant macrofossil identification when possible), and Publication_code.
- Publication_code links results to the corresponding publication.
- Radiocarbon results expressed as percent modern carbon; ages reported as conventional radiocarbon age (years BP).
- The dataset covers multiple sites with both unburnt and burnt conditions, plus thawed peatland profiles.

## Methods and processing
- Field collection: bulk soil samples taken from identified depths within each core.
- Laboratory processing: plant macrofossils identified where possible; samples submitted to NERC Radiocarbon Facility for analysis.
- Output: radiocarbon enrichment values and conventional ages, with publication codes for traceability.

## Data provenance and publication
- Data originate from the NERC Radiocarbon Facility analyses.
- Each result is associated with a publication_code, enabling traceability to published outputs.
- All ages are presented in conventional radiocarbon years BP, with present defined as AD 1950.

## Governance, quality, and practicality for data stewards
- Metadata completeness: explicit fields for Explanation (depth criteria) and Description_of_sample support data discovery and reuse.
- Standardization: use of consistent units (percent modern carbon; years BP) and a uniform publication_code linking results to sources.
- Interoperability considerations: clear site codes and descriptive labels facilitate cross-dataset integration.
- Data quality considerations: reliance on bulk samples and occasional macrofossil identifications; results depend on lab analysis from a single radiocarbon facility, which may affect comparability across datasets if different labs are used.
- Operational challenges highlighted by the dataset (relevant to stewardship):
  - Managing multiple sites with varying environmental contexts (burnt vs. unburnt; thawed peatlands).
  - Ensuring depth criteria are consistently documented across cores for reproducibility.
  - Maintaining up-to-date publication links for traceability of results.