# Model estimates of expected diversity of positive plant habitat condition indicators

## Overview
- Uses Countryside Survey 2007 data to model diversity of positive plant habitat condition indicators (percentCSM) across Great Britain.
- Aims to predict positive habitat indicators for 1 km squares not part of Countryside Survey using a statistical model.

## Experimental Design / Sampling Regime
- Data come from Countryside Survey 2007, surveying 591 1 km squares via stratified random sampling by land class (geology, soils, etc.).
- Within each square, five large random plots (x plots) of 14.14 m × 14.14 m (200 m²) contain an inner 2 m × 2 m nest.
- The inner nest was used for consistency with plots sampling unenclosed habitats (u plots) and small biotope patches (y plots).

## Indicators and Habitat Classification
- Indicator species were defined for priority habitats using guidance from JNCC and consultation with BSBI.
- Plot-level species reflect the BAP Priority Habitats within the Broad Habitat; some Broad Habitats are defined entirely by Priority Habitats (e.g., Dwarf Shrub Heath via Upland and Lowland Heath).
- Some Broad Habitats lack specific CSM lists; alternative “desirable” species lists were used (e.g., Arable and Horticulture). For Ancient Woodland Indicators (AWI), indicators were counted for Broadleaved, Mixed, and Yew Woodlands.
- A dataset includes a list of CSM species by habitat.

## Spatial Reference
- Coordinate System: OSGB 1936 / British National Grid (EPSG:27700).

## Data Attributes
- percentCSM: percentage of CSM plant species in a plot relative to the number of characteristic species for that habitat type.
- SEM: standard error of percentCSM, representing variance in the percentCSM attribute.

## Collection Methods
- In each vegetation plot, a list of all vascular plants plus a selected range of easily identifiable bryophytes and macro-lichens were recorded.
- Nomenclature followed Stace (1991) and Watson (1981).
- Cover estimates were recorded to the nearest 5% for species with at least ~5% cover.

## Analytical Methods
- Positive habitat indicators for each plot were summed to yield a plot-level count.
- Each plot received Broad and Priority Habitat classifications.
- Coastal and urban habitats were excluded; scaling is based on Land Cover Map, which omits linear features (hedgerows, streamsides, roadsides) that can act as refugia in intensive landscapes.
- For squares not part of Countryside Survey, a Generalised Additive Mixed Model (GAMM) predicts percentCSM.
  - Response variable: percentCSM per plot.
  - Random effect: 1 km CS square to account for non-independence of plots within the same square.
  - Distribution: Poisson.
  - Covariates: Broad habitat, Temperature, Precipitation, Nitrogen deposition, Sulphur deposition, SSSI presence/absence.
  - Mapping: dominant broad habitat within a 1 km square is used to create the map.

## Quality Control
- Defra/NERC Joint Codes of Practice followed throughout.

## References / Supporting Documents
- Bunce et al. 2007; Byfield & Wilson 2005; Jackson 2000; Maskell et al. 2008; Smart et al. 2003, 2006, 2008; Stace 1997; Watson 1981; plus related Countryside Survey technical reports and data handbooks.