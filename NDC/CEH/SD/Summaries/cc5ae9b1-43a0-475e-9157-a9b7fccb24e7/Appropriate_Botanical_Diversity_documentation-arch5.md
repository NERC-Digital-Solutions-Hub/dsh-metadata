# Model estimates of expected diversity of positive plant habitat condition indicators

## Overview
- Source: Countryside Survey 2007; 591 one-kilometre squares across Great Britain, stratified by land class.
- Sampling: Five large plots per square (14.14 m × 14.14 m; ~200 m²) with an inner 2 m × 2 m nest; additional plots target unenclosed habitats and small semi-natural biotopes.
- Aim: estimate and map the diversity of positive plant habitat condition (CSM) indicators across broad habitats; provide predictions for 1 km squares not part of Countryside Survey using a statistical model.

## Experimental Design / Sampling Regime
- Plot types within squares: x plots (primary large plots), u plots (unenclosed habitats), y plots (remnant/semi-natural patches).
- Habitat mapping: plots assigned Broad Habitat and Priority Habitat classifications; some Broad Habitats may include non-priority areas.

## Indicators and Habitat Classification
- Indicator selection: characteristic CSM species for priority habitats derived from JNCC guidance and BSBI input.
- Habitat reflection: indicator identity aligns with BAP Priority Habitats within the Broad Habitat; some Broad Habitats use alternative or neutral indicators where standard lists are lacking.
  - Improved grassland: uses neutral grassland indicator proportion (no explicit CSM list).
  - Two Broad Habitats: used alternative ‘desirable’ species lists.
  - Arable & Horticulture: guidance from JNCC and Byfield & Wilson (2005).
  - Broadleaved, Mixed and Yew Woodland: Ancient Woodland Indicators used.
- Dataset includes a list of CSM species by habitat.

## Spatial Reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700).

## Data Attributes
- percentCSM: percentage of CSM plant species in a plot relative to the number of characteristic species for that habitat type.
- SEM: standard error measure for percentCSM.
- Plot-level habitat classifications (Broad and Priority) and derived indicators per habitat type.

## Data Collection Methods
- Flora inventory: every vegetation plot lists all vascular plants and a targeted set of bryophytes and macro-lichens.
- Nomenclature follows Stace (1991) and Watson (1981).
- Cover estimation: to the nearest 5% for species with ≥5% cover.

## Analytical Methods
- Per-plot calculation: sum of positive habitat indicators to produce a per-plot count; plots are then assigned Broad and Priority Habitat classifications.
- Exclusions: coastal and urban habitats excluded; scaling relies on the Land Cover Map that omits linear features (hedgerows, streamsides, roadsides).
- Non-CS square predictions: Generalised Additive Mixed Model (GAMM) with Poisson distribution; response is percent of positive CSM indicators per plot.
  - Random effect: 1 km CS square to account for non-independence of plots within squares.
  - Covariables: broad habitat, temperature, precipitation, nitrogen deposition (N dep), sulfur deposition (S dep), SSSI presence/absence.
  - Output: dominant broad habitat used to create the predictive map.

## Quality Control & Governance
- Adheres to Defra/NERC Joint Codes of Practice throughout data handling and analysis.

## Limitations & Scope
- Exclusions: coastal/urban habitats; linear features not included in scaling.
- Applicability: predictions are for non-CS squares and rely on broad habitat context and environmental covariates; some habitat types rely on alternative indicator lists due to gaps in CSM lists.

## References / Supporting Documents
- Bunce et al. 2007; Byfield & Wilson 2005; Jackson 2000; Maskell et al. 2008; Smart et al. 2003, 2006, 2008; Stace 1997; Watson 1981.