# ITE Land Classification of Great Britain (2007)

## Overview
- A GB-wide land classification system (ITE Land Classification) produced in 2007, used to describe environmental characteristics at landscape scale.
- Data product is a shapefile containing 45 land classes that stratify GB by climate, altitude, slope and other environmental attributes.
- Widely used in Countryside Survey work and intended to support environmental monitoring, policy scrutiny, and informed decision-making.
- Metadata and provenance focus: supports data verification, comparability, and potential integration with other datasets.

## Data specification
- Format: Shapefile.
- Extent: Great Britain.
- Resolution: 1 km.
- Coordinate system: British National Grid.
- Projection: Transverse Mercator; OSGB1936.
- Fields:
  - LC2007: ITE Land Class Number (2007).
  - LC2007_COD: ITE Land Class Code (2007).
- Contents: 45 land classes, each representing a distinct environmental typology across GB.

## Classification details
- Summary names exist for the 45 land classes (2007 version), covering regional variants for England, Scotland, and Wales.
- Codes and descriptive labels encode a hierarchical structure (e.g., regional suffixes like 1e/7s) to differentiate England, Scotland, and Wales classifications.
- The classification framework is designed to reflect major landscape types such as flood plains, low calcareous hills, flat plains, coastal plains, upland valleys, mountain tops, coastal and estuarine areas, and other geomorphological/biophysical units.
- The 45 classes provide a standardized basis for comparing land-cover/landscape types across the country.

## Provenance and references
- Source: Countryside Survey data produced by NERC - Centre for Ecology & Hydrology (CEH).
- Supporting documentation and publications provide the methodological basis and validation context, including datasets and sampling strategies:
  - Barr (1998) Sampling Strategy for Countryside Survey (updated 2011).
  - Benefield & Bunce (1982) visual presentation of land classes.
  - Bunce et al. (1991, 1996a, 1996b) Land Classification developments and applications.
  - Howard, Barr & Scott (1998) validity of CS data for Scotland.
  - Clarke, Howard & Scott (2006) Countryside Survey: Wales-only Reporting.
- Related work includes Merlewood land classification developments and subsequent ecological/biogeographical analyses.

## Relevance for monitoring frameworks
- Provides a consistent, nationally comparable spatial unit (1 km) for tracking environmental health indicators and landscape change.
- Facilitates policy scrutiny by enabling standardized comparisons over time and across regions (England, Scotland, Wales).
- Useful for integrating with other environmental datasets (e.g., habitat, biodiversity, climate, land-use) to support comprehensive dashboards, reports, and governance mechanisms.
- Supports traceability of results through defined codes and documented provenance.

## Data quality, metadata, governance considerations
- Metadata gaps can impede verification and reuse; authors may need to contact dataset originators to fill gaps.
- Some datasets require transformation or alignment to be readily usable in modern workflows.
- Public sharing of underlying data can pose barriers for certain datasets or metadata completeness.
- Ensuring data quality requires attention to provenance, update status, and alignment with current data standards.
- Data governance should address storage, sharing, versioning, and ongoing metadata maintenance to keep datasets current and trustworthy.

## Practical notes for authors of monitoring frameworks
- When using the ITE Land Classification:
  - Treat the 45 land classes as the primary spatial monitoring units at 1 km resolution across GB.
  - Link Land Class codes (LC2007 and LC2007_COD) to other environmental indicators to build composite dashboards.
  - Use the GB-wide extent and OSGB36 projection to ensure consistent geographic alignment with other datasets.
  - Reference the supporting literature and methodological documents to justify classification choices and to understand sampling/validation context.
  - Plan for metadata enhancement and data governance processes to support transparency and reproducibility.
- Consider data access and transformation needs early, and engage with data originators if metadata is incomplete or missing.
- Be mindful of potential data silos and promote integration strategies to maximize the utility of the Land Classification within monitoring frameworks.