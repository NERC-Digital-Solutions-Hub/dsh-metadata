# Plant community surveys and sampling design

- Purpose: Document plant species distribution and abundance on Jebel (Tunisia) using a standardized, multi-scale sampling framework to enable analyses of grazing effects and environmental drivers.

## Study design and sampling logistics

- Timeframe: 18 June – 7 August 1983.
- Survey area: Jebel, Tunisia; 78 quadrats located across widely dispersed sites, excluding inaccessible crags/cliffs.
- Quadrats and nested design: 2 x 2 m, 5 x 5 m, 7.07 x 7.07 m, 10 x 10 m, and 14 x 14 m; at each site a central stake was located randomly within a quadrat.
- Coverage: sampled all vegetated areas guided by Fay (1980) vegetation maps; areas not randomly chosen but representative of community types.
- Data collection pace: each site involved about three nested quadrats, completed in 8–10 hours per day.

## Plant identification and taxonomy

- Field vs. voucher: plants not identified in the field were collected and pressed; comparisons made with herbarium specimens (Tunis or British Museum).
- Temporal limitation: late flowering period for many herbaceous species likely led to under-recording of some taxa (e.g., Liliaceae, Orchidaceae).
- Taxonomic adjustments: many names updated post hoc (Euro-Med PlantBase and MedChecklist); final taxonomy aligned with Tunisia flora references (Le Floc'h et al. 2010; Daoud-Bouattour et al. 2007).
- Taxonomic limits: certain species pairs could not be distinguished and were combined (e.g., Hypochoeris achyrophorus/H. saldensis).
- Functional grouping: species categorized into taxonomic/functional groups (Graminoids, Legumes, Geophytes, Forbs, shrub legumes, shrubs/trees); annual vs. perennial not distinguished due to single-season study.

## Assessing grazing intensity and herbivory

- Focus: browsing intensity assessed at woody species within the 10 x 10 m quadrat; herbaceous grazing not quantified.
- Browsing levels (4 categories): 
  1) unbrowsed; 2) lightly browsed; 3) moderate to heavy browsed; 4) severely clipped to short stunted bushes.
- Additional indicators: signs of herbivorous mammals (e.g., droppings, hair on trunks, feeding signs) noted qualitatively but not quantified.
- Sample distribution: among 78 sites, 71% unbrowsed, 12.8% lightly browsed, 16.7% moderately to heavily browsed; heavily browsed sites tended to be low-altitude with rocky outcrops and smaller olive trees.
- Interpretation caveat: grazing effects may vary by plant life stage and species preference; herbaceous grazing impact inferred from woody plant browsing.

## Abiotic environmental measurements

- Altitude: measured with a barometric altimeter.
- Slope and aspect: measured with inclinometer and compass to proxy solar insolation.
- Substrate/parent material: recorded as percentage rock outcropping/rock cover at each quadrat center.
- Rationale: to separate environmental covariates from grazing effects on plant community turnover.

## Olea europaea as a proxy for anthropogenic activity

- Rationale: olive trees influence shade, herbaceous composition, and reflect historic to ongoing human activity (grazing, woodcutting).
- Measurements: density of Olea stems >4 cm DBH at ~1.5 m, recorded at 69 sites; additional measurements at 30 cm above ground height when possible.
- Size classes: stems categorized by circumference into 0–5, 6–10, 11–15, 16–20, >20 cm; multiple stems per tree aggregated into an equivalent radius formula.

## Data structure and files

- Data files (three flat CSVs):
  - woody_comm.csv: counts of woody plants at each of 78 sites.
  - herb_comm.csv: counts of herbaceous plants at each of 78 sites.
  - spatial_env.csv: environmental variables at each of 78 sites.
- Metadata: detailed column headings and variable definitions documented in a supplementary file (Metadata_for_Tunisia plants.rtf).

## Data quality, limitations, and governance notes

- Taxonomy and nomenclature: updated to current standards post-field; some synonymy and indistinguishable species merged to maintain data usability.
- Sampling representativeness: non-random site selection but designed to cover multiple community types; potential biases acknowledged.
- Data usage and attribution: authors indicate possible future use in separate papers; permission to contact authors prior to reuse is advised.
- Metadata availability: explicit metadata file supports understanding column definitions and data structure, aiding interoperability and reuse.
- Compatibility considerations: multi-scale sampling and nested quadrats may require careful harmonization with other datasets due to scale, units, and taxa groupings.

## Practical implications for data stewardship

- Standardization: consistent data formats (CSV) and the inclusion of a metadata document facilitate discoverability and reuse, but taxonomy updates should be tracked for reproducibility.
- Provenance and versioning: field methods are well-documented; future users should note the historical context (1983) and potential taxonomic changes.
- Access and reuse: clear note on potential additional analyses; consider metadata-driven data sharing agreements if used in new studies.
- Potential applications: baseline data for grazing-environment interactions in Mediterranean shrub communities; useful for comparative ecological analyses incorporating abiotic and anthropogenic proxies (Olea europaea).