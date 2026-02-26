# Metadata for Woody species

## What this document contains
- Metadata entries for woody plant species, each with a code (e.g., ANAGFOET, ARBUUNED) and associated scientific name.
- A listed functional group or life form for many entries (e.g., Legume), with some entries lacking this information (denoted by a dot).
- Repeated records for certain taxa (e.g., entries labeled with 1 and 2), indicating alternative classifications or subspecies not differentiated.
- A parallel section for herbaceous species and a separate section for spatial and environmental data, illustrating a multi-part data catalog.

## Structure of the data
- Three main blocks:
  - Metadata for Woody species: code, scientific name, and functional group/life form.
  - Metadata for Herbaceous species: similar structure with codes, scientific names, and growth forms.
  - Metadata for Spatial and Environmental data: geographic, soil, grazing, and olive-tree related measurements and indicators.

## Key fields and codes
- Each woody or herbaceous entry uses:
  - Code (e.g., ANAGFOET, CALIVILL)
  - Scientific Name (e.g., Anagyris foetida L.)
  - Functional group / life form (e.g., Legume); some entries may have missing data (shown as ".")
- For spatial and environmental data, fields include:
  - LATITUDE, LONGITUDE, ALTITUDE
  - SLOPE, Aspect
  - ROCKCROP (percentage rock outcropping)
  - SOILPH (soil pH for 50 sites)
  - GRAZING (grazing index with four levels)
  - OLIVDIAA, OLIVDIAB, OLIVDIAC, OLIVDIAD, OLIVDIAE (olive diameter categories at various heights)
  - OLIVBREA, OLIVBREB, OLIVBREC, OLIVBRED, OLIVBREE (olive diameter by another height measure)
  - MEAN30, MEANDBH (mean counts at different heights)
  - FREQ30, FREQDBH (frequency metrics)
- The dataset distinguishes between woody and herbaceous taxa, with a separate section for each and a dedicated section for spatial/environmental measurements.

## Spatial and environmental data specifics
- Geographic coordinates (latitude/longitude) and topographic context (altitude, slope, aspect).
- Substrate and site condition indicators (ROCKCROP, SOILPH).
- Land-use pressure metrics (GRAZING index) to reflect disturbance.
- Tree-scale metrics for olive trees (diameter at various heights, mean counts, and frequency) to enable habitat and productivity analyses.
- Broad taxon metadata supports data discovery, interoperability, and integration with other datasets.

## Observations about data quality
- Functional group/life form is not consistently populated for all entries (some entries use a dot to denote missing data).
- Some taxa are not differentiated at subspecies level (e.g., “2” records indicate nondifferentiation or alternate classifications).
- The dataset appears to be designed for cross-linking woody and herbaceous flora with environmental sensing data, but completeness of fields varies across entries.

## Relevance for Data Leaders
- Demonstrates a standardized approach to cataloging species metadata alongside spatial and environmental measurements, supporting data governance and discoverability.
- Highlights the importance of complete metadata (functional groups, subspecies differentiation) to reduce ambiguity and improve data utility.
- Provides a framework for identifying data gaps (e.g., missing functional forms, unassigned subspecies) and for planning data acquisition or cleansing.
- Facilitates integration with broader data communities and platforms by maintaining consistent codes and descriptive fields across taxa and environmental variables.