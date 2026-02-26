# Column header/Determinand

## Overview
- The document defines a data table for river water quality and related measurements, with a set of columns for sampling metadata and multiple determinands (measured properties).
- Each determinand includes: a preferred label, units (with a label and URI), and a determinand URI for standardization.
- Units and labels reference an ontology (CAST) via URIs, aiming to support interoperability and discoverability.

## Data columns and metadata
- Sampling metadata:
  - Sampling Date
  - Sampling time
- Key measured variables (examples of determinands and their typical units):
  - Average daily river flow — measured in cubic metres per second (cumecs); unit label and URI provided.
  - Temperature of water sample — measured in degrees Celsius (°C); temperature determinand label and URIs provided.
  - pH — no units; standard pH determinand with corresponding URI.
  - Electrical conductivity — measured in microsiemens per centimetre (µS cm-1) at 25°C; unit label and URI provided.
  - Gran alkalinity — measured in milliequivalents per litre (mEq l-1); unit label and URI provided.
  - Dissolved nitrate, Dissolved reactive silicon, Total Phosphorus, Total dissolved phosphorus, Soluble reactive phosphorus — various phosphorus and nitrogen species with corresponding microgram per litre (µg l-1) or milligram per litre (mg l-1) units and URIs.
  - Dissolved chloride, Dissolved sulphate, Dissolved sodium, Dissolved potassium, Dissolved magnesium, Dissolved calcium — dissolved ion concentrations, generally in mg l-1 with corresponding URIs.
  - Suspended solids
  - Dissolved ammonium — typically mg NH4-N l-1 with appropriate units and URIs.
- Metadata detail:
  - Some determinand labels are explicitly provided, while others appear as placeholder "." in the source.
  - Unit labels include multiple conventions (e.g., cumecs for flow; degrees Celsius for temperature; no units for pH).
  - Each determinand includes a corresponding URI (often on the CAST ontology), though some entries lack a determinand URI or have repeated/missing URIs.
  - The unit URIs follow http://onto.nerc.ac.uk/CAST/ identifiers (e.g., CAST/152, CAST/157, CAST/156, etc.).

## Ontology and standardization
- The dataset uses standardized ontologies for determinands and units, increasing interoperability across systems and networks.
- CAST URIs are provided for many determinands and units, enabling consistent interpretation and linking to broader data catalogs.
- Inconsistencies exist (e.g., some determinand labels or URIs missing or left as placeholders), which may affect discoverability and automated validation.

## Data quality and accessibility considerations
- Data discoverability is aided by the use of standardized labels and URIs; however, gaps in metadata (missing labels, missing URIs, inconsistent units) may hinder quick verification and reuse.
- Verifying content and format of determinands can be challenging where units or labels are not clearly specified.
- The data structure implies a need for careful data governance: ensure complete, unambiguous metadata, consistent unit usage, and up-to-date URIs.

## Practical implications for Data Leaders
- Ensure comprehensive metadata coverage:
  - Fill in missing Determinand labels and URIs where "." appears.
  - Confirm and standardize units across all determinands (prefer explicit unit labels and consistent URIs).
- Leverage ontology-backed identifiers:
  - Use CAST URIs to improve interoperability with other datasets and partners.
- Improve data quality practices:
  - Validate data content and formats at ingest and prior to dissemination.
  - Maintain clear provenance and update metadata as standards evolve.
- Enhance data discoverability and sharing:
  - Catalog determinands with their labels, units, and URIs to support co-ownership and reuse across teams and partner networks.
- Align with wider data communities:
  - Use the standardized determinand set to facilitate collaboration and reduce duplicated efforts across sectors.

## Endnotes
- The document primarily maps a wide range of river water quality measurements to standardized labels, units, and ontological URIs, highlighting both robust standardization and areas needing metadata completeness.