# Errata for dataset http://doi.org/1fb2cda3-cb49-414f-ad844a2f88ecce15

## Overview
- Erratum announcing withdrawal of the dataset “Historic grassland survey data with contemporary spatial habitat data for semi-natural grasslands across England” and its replacement with a new version.
- Reason: one author (Richard Pywell) judged that the high-resolution quadrat locations could allow identifying land parcels, potentially upsetting landowners and revealing information about habitat loss.
- The dataset has been superseded by a version that uses coarser location data (10km grid references).

## What changed
- Original dataset withdrawn and replaced with “Historic grassland survey data with contemporary spatial habitat data for semi-natural grasslands across England v2.”
- New version provides locations at 10km grid reference resolution instead of high-resolution quadrats.

## Implications for GIS Specialists
- Spatial precision reduces from high-resolution quadrat data to a 10km grid, affecting analyses that require fine-scale location detail.
- Map visualisations and spatial analyses may need to be reworked to operate at the coarser grid resolution.
- Metadata should reflect the 10km grid resolution; workflows and data pipelines should be updated to ingest v2.
- Demonstrates a privacy-conscious data governance decision balancing data utility with landowner confidentiality.

## Access and provenance
- Original dataset referenced by the provided URL; superseded dataset is v2 with reduced spatial precision. Consult the same data portal for the updated version and accompanying metadata.

## Recommendations for GIS workflows
- Update analyses and maps to use v2 (10km grid) and document the change in spatial resolution.
- If finer-scale insights are essential, explore aggregated or anonymized approaches that preserve privacy while meeting research needs.
- Revalidate any previously produced outputs that relied on high-resolution locations; adjust expectations and interpretations accordingly.