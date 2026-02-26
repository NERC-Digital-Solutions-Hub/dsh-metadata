# Dung beetle community data from a beforeand-after El Niño experiment in the Brazilian Amazon

## Data context and purpose
- Time-series dataset of dung beetle abundance from dung-baited pitfall traps collected in 2010, 2016, and 2017, within the Brazilian Amazon.
- Part of the NERC Human-Modified Tropical Forest (HTMF) programme, aimed at understanding how human disturbance and climate events (El Niño) affect tropical forest biodiversity.
- Data described here include plot-level abundance, spatial coordinates, and sampling design across a gradient of forest disturbance.

## Data holdings and structure
- Four data files (CSV) comprising the ECOFOR_AFIRE_RAS dung beetle dataset:
  - dung-beetles_ECOFOR_AFIRE_RAS_all.sites_2010.csv: plot-level beetle abundance for 381 plots (2010).
  - dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2016.csv: plot-level abundance for 36 plots (2016, subset from 381).
  - dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2017.csv: plot-level abundance for 36 plots (2017, same 36 as 2016).
  - dung-beetles_ECOFOR_AFIRE_RAS_all_plot-position.csv: geographical coordinates for all study plots.
- Each file includes:
  - Species column (species/morphospecies identities).
  - Plot identifiers (e.g., 100_1, 100_10) as columns for abundance data.
  - For plot-position: Plot, Municipality, UTM X, UTM Y coordinates.

## Study design and sampling regime
- Study regions: Paragominas (PGM) and Santarém/Belterra/Mojuí dos Campos (Santarém STM) in Pará, Brazil.
- Catchment-based sampling: 18 catchments (32–61 km²) with 381 plots total, stratified along forest cover gradients (non-forest and forest plots).
- Forest plots distributed among primary forests and secondary forests; non-forest plots in pasture and mechanised agriculture.
- 2010: sampling Apr–Jun across all 381 plots (3429 pitfall traps).
- 2016 and 2017: sampling within a subset of 36 forest plots, arranged along a degradation gradient (undisturbed, logged, logged-and-burned, secondary forest); roughly 333 traps per year.
- Disturbance context defined using satellite-based canopy disturbance (1988–2010) and field assessments of fire/logging.

## Data collection methods
- Beetle sampling with pitfall traps baited with 50 g dung (80% pig, 20% human).
- Trap setup: corners of a 3-m equilateral triangle along a 300-m transect; traps left for 48 hours.
- Permitting: verbal permits for private land; formal SISBIO permits for protected areas (2010–2011 and 2016 surveys).
- Objective: quantify dung beetle community responses to human and climate stressors.

## Reuse, licensing, and access
- Data citation provided: França et al. (2019), entry in the NERC Environmental Information Data Centre.
- Data access and reuse limitations, including licensing details, are described at the provided DOI links:
  - https://doi.org/10.5285/799db965-3ce7-4e9b-8590de6a8624d652
  - Data reuse limitations and licensing: https://doi.org/10.5285/799db965-3ce7-4e9b-8590-de6a8624d652

## Provenance and authorship
- Collected and processed by researchers including F. França, V. Oliveira, F.Z. Vaz-de-Mello, J. Ferreira, J. Barlow, E. Berenguer, J. Louzada, and T. Gardner, with roles spanning study design, plot selection, data collection, beetle identification, and interpretation.
- Data support and documentation exist to enable reproducibility and enable self-service analyses of dung beetle community changes over time.

## Practical notes for researchers
- The dataset provides a clear, plot-level time series (2010, 2016, 2017) suitable for biodiversity change analyses in relation to El Niño events and habitat disturbance gradients.
- Metadata includes sampling protocol, plot coordinates, and sampling effort (trap counts), facilitating normalization and cross-year comparisons.
- Appropriate citation is required when reusing; licensing details are accessible via the linked DOIs.