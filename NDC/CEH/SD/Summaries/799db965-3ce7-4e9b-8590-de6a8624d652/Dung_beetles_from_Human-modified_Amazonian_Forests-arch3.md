# Dung beetle community data from a beforeand-after El Niño experiment in the Brazilian Amazon

## Overview
- Time-series dung beetle abundance data from pitfall traps baited with dung, collected in 2010 (pre-El Niño), 2016 and 2017 (post-El Niño).
- Study area: Brazilian Amazon, in Paragominas (PGM) and Santarém/Santarém‑Belterra/Mojuí dos Campos (STM), Pará.
- Part of the NERC Human-Modified Tropical Forest (HTMF) programme; collaboration across institutions with broader funding support (NERC, Darwin Initiative, EMBRAPA, CNPq, etc.).
- Data organized into four sheets/files: 2010 all plots, 2016 subset (36 plots), 2017 subset (36 plots), and plot-position coordinates.
- Data are intended to illuminate how human- and climate-induced stressors influence tropical forest biodiversity; permits and permissions documented.

## Experimental design and sampling regime
- Sampling units: 18 catchments (32–61 km²) across gradients of forest cover; plots distributed to reflect non-forest and forest cover.
- Plot layout: 381 plots in 2010 (totaling 3,429 pitfall traps); within each catchment, 8–12 plots (separated by at least 1.5 km); non-forest plots in pastures and mechanized agricultural lands; forest plots in primary and secondary forests.
- Post-El Niño re-sampling: 2016 and 2017 surveys conducted within a subset of 36 forest plots (from the 381), distributed along a gradient of prior forest degradation (undisturbed, logged, logged-and-burned, secondary).
- Fire impact: half of the 36 plots were fire-affected during the 2015–16 El Niño; the others experienced drought effects.
- Disturbance assessment: forest disturbance classes determined from satellite imagery (1988–2010) and prior field assessments of fire scars and logging/charcoal debris.
- Sampling window: pre-El Niño in 2010 (April–June); post-El Niño in 2016 (July) and 2017 (March–April).
- Sampling method: dung beetles trapped with 50 g dung bait (80% pig, 20% human) using traps filled with a killing solution; traps arranged at three corners of a 300 m transect (3 m apart), with three sampling points per transect; traps active for 48 hours.

## Data collection methods
- Permissions: verbal approvals obtained from landowners; protected areas surveyed under Brazilian legal requirements (SISBIO permits).
- Personnel: study design and plot selection by J. Barlow, T. Gardner, J. Ferreira; data collection and beetle identification by F. França, V. Oliveira, F.Z. Vaz-de-Mello; data interpretation by F. França, J. Ferreira, J. Barlow, V. Oliveira, J. Louzada.
- Data scope: aim to quantify dung beetle community responses to human- and climate-driven stressors.

## Data files and structure
- dung-beetles_ECOFOR_AFIRE_RAS_all.sites_2010.csv
  - Plot-level abundance matrix for 381 plots (2010).
  - Columns: Species (A) and Plots (B onward) with plot codes (e.g., 100_1).
- dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2016.csv
  - Plot-level abundance for 36 plots (2016) in Santarém region.
  - Columns: Species (A) and Plots (B onward) with plot codes.
- dung-beetles_ECOFOR_AFIRE_RAS_subset.sites_2017.csv
  - Plot-level abundance for 36 plots (2017) in the same 2016 subset.
  - Columns: Species (A) and Plots (B onward) with plot codes.
- dung-beetles_ECOFOR_AFIRE_RAS_all_plot-position.csv
  - Plot-level geographical coordinates.
  - Columns: Plot, Municipality, UTM_X, UTM_Y (UTM zones 21M/22M as applicable).

## Licensing, access, and reuse
- Data cited as França et al. (2019) from the NERC Environmental Information Data Centre.
- Licensing and reuse limitations documented at the provided DOI links; data access requires citation and adherence to specified reuse terms.
- Data provenance, metadata, and openness emphasized; permits and field data sharing completed as part of project governance.

## Relevance to monitoring frameworks
- Demonstrates end-to-end monitoring pipeline: study design across disturbance gradients, standardized sampling, multi-temporal data collection, and explicit data governance.
- Illustrates handling of data gaps and metadata via multi-file structure and clear plot identifiers.
- Provides a real-world case for evaluating data access, sharing, governance, and the challenges of communicating complex ecological findings to policymakers.
- Useful for assessing biodiversity responses to climate events (El Niño) and forest disturbance, informing future monitoring decisions and reporting.