# Column header/Determinand

## Overview
- A data dictionary mapping river water quality column headers to standardized determinands and units, using OntoNERC CAST URIs to facilitate semantic interoperability for GIS workflows.
- Designed to support map-based data visualisation and spatial analysis by standardising measurements and units across datasets.

## Key Determinands and Units (highlights)
- Sampling Date and Sampling Time: temporal metadata for time-enabled GIS layers.
- Average daily river flow: units m3/s (cumecs).
- Temperature of water sample: degrees Celsius (deg C).
- pH: no units.
- Electrical conductivity: µS cm-1 (units labeled as uS/cm @25C).
- Gran alkalinity: mEq L-1 (microequivalents per litre).
- Dissolved nitrate: typically reported in mg NO3-N, mg Si l-1, or µg L-1 (micrograms per litre), with URI references.
- Dissolved reactive silicon: (units µg L-1, etc., as applicable).
- Total Phosphorus, Total dissolved phosphorus, Soluble reactive phosphorus: various phosphorus-related units (µg L-1, mg L-1 as indicated).
- Dissolved Cl (Chloride), Dissolved SO4 (Sulfate), Dissolved Na (Sodium), Dissolved K (Potassium), Dissolved Mg (Magnesium), Dissolved Ca (Calcium): all specified with mg L-1 (milligrams per litre) in the snippet, with corresponding URIs.
- Suspended solids: (implicit unit handling in dataset; typically mg/L in water quality data).
- Dissolved NH4 (Ammonium): mg L-1, with URI references.
- For each determinand: a Determinand preferred label and a determinand URI; for each, a Units preferred label and a Units URI.

## Semantic Linking and Ontology
- Each determinand and unit is paired with a standardized label and an ontology URI (e.g., http://onto.nerc.ac.uk/CAST/…).
- Enables consistent interpretation across GIS datasets and supports faceted querying by parameter and unit.

## GIS Implementation Guidance
- Ingest as time-enabled layers using Sampling Date and Sampling Time for temporal analysis.
- Use determinand URIs to join or compare across datasets from different sources.
- Normalize units where necessary to ensure comparability (e.g., convert all phosphorus measurements to the same unit before mapping).
- Leverage units URIs to maintain consistent unit handling during data processing and visualization.

## Considerations and Challenges
- Data may be spread across multiple sources with inconsistent standards; the mapping provides a framework to harmonise them.
- Some determinands use multiple possible units; care is needed to select and convert to a consistent unit set.
- Missing data and large/complex datasets require careful cleaning and transformation before GIS integration.
- Developing teams with sufficient data-handling and GIS skills are essential to implement and maintain these mappings effectively.