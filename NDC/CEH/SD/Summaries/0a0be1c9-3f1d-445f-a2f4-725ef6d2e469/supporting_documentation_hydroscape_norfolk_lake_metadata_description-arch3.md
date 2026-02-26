# hydroscape_norfolk_core_metadata.csv

## Overview
- Metadata for lake sediment cores within the Hydroscape Norfolk dataset, capturing core identification, location, physical properties, dating status, and provenance to support environmental health monitoring and policy evaluation.

## Key fields and meanings
- EIDC File Name: File name uploaded to EIDC (CSV).
- WBID: Waterbody Identification number (via CEH Lakes app) linking to the waterbody source.
- Hydroscape: Name of the Hydroscape region used.
- Name: Lake name from which the core was taken.
- General location of core: Indicates cores were collected from the central (often deepest) area of the lake.
- OSGB36_E / OSGB36_N: UK Ordnance Survey coordinates in OSGB36 datum (Eastings and Northings).
- Water depth at core site (m): Distance from water surface to sediment surface at the core site.
- Core length and type: Core length in metres and the type of core used.
- Corer types: References for corers used (Big Ben and Livingstone):
  - Big Ben: Patmore et al. 2014. Big Ben: a new wide-bore piston corer for multi-proxy palaeolimnology. Journal of Paleolimnology, 51(1), 79-86.
  - Livingstone: Livingstone 1955. A lightweight piston sampler for lake deposits. Ecology, 36(1), 137-139.
- Date core collected: Date of fieldwork and core collection (dd/mm/yyyy), with year-only if precise date is unknown.
- UCL_Code: Internal University College London code used on bags/database.
- UCL Sample ID: Internal (Amphora) code for the entire sample core (unique ID).
- 210 Pb-dated (Y/N) for: Indicates whether the core has been dated using ^210Pb (Yes/No).
- Hydroscape: Regional identifier within the Hydroscape framework (field present but description may be incomplete in the snippet).

## Data provenance and references
- Source systems: EIDC repository and UK Centre for Ecology & Hydrology (CEH) access via the Lakes/ Hydroscape datasets.
- Corer references provide methodological context for core sampling (Big Ben and Livingstone) to enable reproducibility and comparability across cores.

## Data quality, access and governance
- Metadata completeness is essential for traceability (site, coordinates, core specs, dating status, and identifiers).
- Open data considerations: internal codes and sample identifiers exist; sharing underlying datasets may require governance and data management controls.
- Metadata integrity challenges include potential missing or partial fields (e.g., Hydroscape description), and the need for consistent coordinate systems and dating status.

## Relevance to monitoring frameworks
- Enables systematic assessment of environmental health indicators derived from palaeolimnological cores.
- Supports data discovery, lineage, and traceability for policy evaluation and future decision-making.
- Facilitates linking physical core properties, geospatial location, dating status, and regional Hydroscape context for monitoring programs.

## Practical considerations for implementers
- Use as a schema for metadata collection to ensure consistency across cores and datasets.
- Leverage coordinates (OSGB36_E/N) for geospatial analyses and mapping within monitoring dashboards.
- Use 210Pb dating status to flag cores with robust or partial dating for interpretation in environmental assessments.
- Ensure clear data governance around internal identifiers (UCL_Code, UCL_Sample_ID) and public sharing of underlying data where appropriate.

## Gaps and limitations
- Some description fields (e.g., Hydroscape) may be incomplete in the provided snippet, indicating potential metadata gaps.
- Public access barriers may arise due to internal codes and data sharing policies; governance structures should be clarified to maximize data usability.
- Standardization across datasets (e.g., core location protocols, dating criteria) is needed to minimize transformation effort for downstream monitoring use.