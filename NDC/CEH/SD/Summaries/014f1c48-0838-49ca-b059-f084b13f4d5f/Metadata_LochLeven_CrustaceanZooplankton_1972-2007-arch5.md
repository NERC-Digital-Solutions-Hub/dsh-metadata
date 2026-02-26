# METADATA FOR 'LOCH LEVEN CRUSTACEAN ZOOPLANKTON 1972-2007' DATASET

## Overview
- Dataset of densities of crustacean zooplankton from Loch Leven (1972–2007), collected as part of the lake’s long-term monitoring by CEH Edinburgh and predecessor bodies.
- Data structure captures date, sampling information, methodology, and densities (numbers per litre) for three major crustacean zooplankton taxa.

## Data Content and Structure
- Three taxa covered: Cyclops abyssorum (+ nauplii), Eudiaptomus gracilis (+ nauplii), Daphnia sp.
- Columns include: date of sample, relevant sampling information, sampling methodology, and number of individuals per litre (ind/l) for each taxon.
- If multiple locations/methods are used, values are averaged.
- Zeros mean the species was not recorded at the sampling/analytical resolution; blanks indicate missing values.
- Taxa densities are converted to ind/l and samples are preserved for archiving.

## Spatial Coverage
- Sampling locations are specified with GB national grid coordinates (Table 1 provides easting/northing for each site).
- Sites include: Centre Loch, Kinross Bay, North Deeps, Public Pier, Castle Bay, Reed Bower, Outflow.
- When multiple sites/methods are used, site-level values are averaged.

## Temporal Coverage and Quality Control
- Timeframe: 1972–2007.
- Quality control: pre-1992 data checked by Dr. Linda May; 1992–2007 data checked by Iain Gunn.
- Taxonomic names updated if they have changed over time.

## Sampling Methodology by Era
- 1972–1974: fortnightly sampling using a 5 L Friedinger sampler.
- 1975–1982: vertical plankton net haul (depths to surface; 100 µm mesh, or 125 µm with integrating tube sampler).
- 1992 onwards: 45-degree angled net haul (120 µm mesh).
- Immediately after collection: samples preserved in 4% formaldehyde.

## Laboratory Processing and Data Transformation
- In the lab: samples placed in 250 ml glass vessels, mixed, and subsampled with a 5 ml Stempel pipette.
- Identification and counting under a low-power microscope; typically three subsamples per sample.
- Species identified to the deepest possible taxonomic level given preservation and maturity.
- Subsample counts converted to ind/l using appropriate multiplication factors; samples reconstituted and archived.
- Where taxonomy has changed, older names updated to current equivalents.

## Metadata and Documentation
- Dataset represents a long-term monitoring record; methods and locations documented to support reproducibility and re-use.
- References supporting identification keys and methodology provided (publications from 1966–1996).

## Governance and Use Considerations for Data Stewards
- Standardization: long-running shift in sampling methods requires careful metadata to ensure comparability over time.
- Availability and updates: data are archived with quality checks; ensure ongoing accessibility and clear versioning.
- Interoperability: varying methods and preservation protocols may affect cross-dataset integration; maintain method-change notes in metadata.
- Data completeness: zeros vs. blanks should be interpreted with awareness of sampling resolution and potential missingness.