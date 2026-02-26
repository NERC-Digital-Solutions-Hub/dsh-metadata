# UnknownsUplandLowlandMetabolomics.csv

## Overview
- Metabolomics dataset describing urine from sheep, processed using untargeted primary metabolism analysis.
- Samples collected in autumn from two pasture sites: semi-improved and improved pasture (n=4 per site; total of 8 samples).
- Procedures included syringe-filtering, flash-freezing, storage at -80°C, shipping on dry ice to UC Davis for GC-TOF-MS analysis.
- Data contains peak intensity values for identified compounds from the untargeted analysis; blanks (ultra-pure water) were syringe filtered and blank-corrected.

## Data structure and processing
- File format: CSV.
- Key headers:
  - Sample: combines sheep ID and site of urine collection.
  - Season: site/pasture context (autumn in both cases described).
  - Remaining columns: numerical identity values representing peak intensities for unidentified compounds detected in the primary metabolism analysis.
- Data provenance notes:
  - ALEX-CIS GC-TOF-MS instrument used (Gerstel Inc.).
  - Procedural blanks used for blank correction.
  - Data explicitly includes peak intensity values for unidentified metabolites.

## Spatial relevance and GIS potential
- Useful for GIS-based analyses by linking metabolomic profiles to geographic locations of sampling sites.
- Potential map layers:
  - Sample locations by site (semi-improved vs improved pasture) and season.
  - Site-level environmental covariates (soil type, land management, climate) to explore spatial associations with metabolomic patterns.
- To enable GIS workflows:
  - Geocode or attach coordinates to each sample via site identifiers.
  - Create a point shapefile or layer representing sample sites; join with this CSV.
  - Consider aggregating by site to compare metabolomic features across pasture types.

## Variables and data quality considerations
- Variables:
  - Sample: sheep ID and site of urine collection.
  - Season: autumn (per the description).
  - Compound columns: unidentified primary metabolism metabolites, represented by peak intensities (numerical values).
- Data quality and limitations:
  - Small sample size (8 samples total) and single-season (autumn) data; limits generalizability.
  - Compounds are unidentified; no chemical identities provided, which constrains interpretation and cross-referencing with external metabolite databases.
  - Metadata gaps for richer GIS use (no explicit coordinates, limited site descriptors beyond semi-improved/improved pasture).
  - Data processing steps are described (blank correction, storage, transport, analysis method), but more detail on QC metrics would aid reproducibility.

## Access, reuse, and provenance
- Grant: NE/M015351/1.
- Authors: Karina A Marsden; Lucy Lush; Jon A Holmberg; Mick J Whelan; Andrew J King; Rory P Wilson; Alice F Charteris; Laura M Cardenas; Davey L Jones; Dave R Chadwick.
- Citation reminder: If data are reused, ensure full citation.
- Licensing: Not specified in the provided text; treat as requiring appropriate citation and confirmation of reuse rights.

## Recommended GIS workflows and notes
- Transform to a GIS-ready dataset:
  - Add spatial coordinates for each sample site or attach to an existing site polygon layer.
  - Create a point feature class with attributes: site type (semi-improved vs improved), season (autumn), sample ID, and metabolomic intensities.
- Analysis ideas:
  - Compare metabolomic profiles between pasture types using multivariate analyses (PCA, PLS-DA) and map results by site.
  - Overlay sample points with environmental rasters (soil properties, elevation, climate) to explore spatial drivers.
  - Produce thematic maps of aggregate metabolomic signals by site or by identified compound groups (once identities are available or via dimension-reduced components).
- Data preparation considerations:
  - Normalize or transform peak intensities (e.g., log transformation) for comparability.
  - Address the lack of compound identities by focusing on relative patterns or principal components rather than individual metabolite names.
  - Document any site-specific labeling inconsistencies (note minor typos such as "semi-imporved") to ensure consistent GIS tagging.