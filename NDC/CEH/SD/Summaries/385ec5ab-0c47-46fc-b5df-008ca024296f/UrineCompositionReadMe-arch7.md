# UrineComposition.csv

## Overview
- Dataset describing sheep (Welsh Mountain ewe) urine chemical composition plus metadata.
- Intended for analysis of chemical constituents in relation to spatial (site) and temporal (season, date) factors.
- Authored for a project on uplands and nitrogen cycling; includes guidance to cite if reused.

## Data content and headers
- Key fields (data headers): 
  - Season (spring, summer, autumn)
  - Site (two sites: semi-improved or improved pasture)
  - Sheep (replicate sheep identifier)
  - Date (dd/mm/yyyy)
  - Time (approximate time of urination)
  - Vol (urine event volume, ml)
  - TOC (dissolved organic carbon, g C l-1)
  - TN (total nitrogen, g N l-1)
  - pH
  - EC (electrical conductivity, mS cm-1)
  - Urea (g urea-N l-1)
  - Nitrate (mg NO3- -N l-1)
  - Ammonium (mg NH4+ -N l-1)
  - AA (amino acids, mg amino acid-N l-1)
  - Allantoin (g compound l-1)
  - Creatinine (mg compound l-1)
  - Uric (mg compound l-1)
  - Hippuric (g compound l-1)
  - Benzoic (mg compound l-1)
  - Ca (mg Ca l-1)
  - Na (mg Na l-1)
  - K (g K l-1)

## Methods and processing
- Sample handling:
  - Urine samples filtered on ice through Whatman No. 1 filter (11 μm) to remove large particulates.
  - Subsamples frozen at -20 °C prior to analysis.
- Measurements:
  - pH and EC measured with standard electrodes.
  - TOC: total dissolved organic carbon measured with Multi N/C 2100S.
  - Urea: enzymatic method.
  - Nitrate: colorimetric method (Miranda et al. 2001).
  - Ammonium: colorimetric method (Mulvaney 1996).
  - Amino acids: fluorometric method (Jones et al. 2002).
  - Allantoin, creatinine, uric acid, hippuric acid, benzoic acid: HPLC with specified column and detection parameters.
  - Potassium, calcium, sodium: flame photometry.
- References for methods:
  - Jones, D.L. et al., 2002
  - Miranda, K.M. et al., 2001
  - Mulvaney, R.L., 1996
  - Orsenneau, J.L. et al., 1992

## Spatial and temporal context
- Spatial: two sites with pasture types (semi-improved and improved) enabling spatial comparisons.
- Temporal: data captured across seasons (spring, summer, autumn) plus exact collection date and approximate time.
- Units are specified for all measurements, enabling cross-site and temporal comparisons.

## Potential GIS applications
- Map-based visualization of urine constituents by site and season (e.g., choropleth or dot maps using site-level data).
- Time-series visualization of key constituents (e.g., Urea, TN, TOC) across seasons.
- Linking urine chemistry data to pasture management layers, soil properties, or climate layers for upland nitrogen cycling analyses.
- Integration with other GIS datasets to explore spatial patterns in livestock metabolism or excretion related to land-use type.

## Data quality, provenance, and usage notes
- Lab-based dataset with detailed processing steps enhances reproducibility and quality assurance.
- Geographic coordinates are not provided; sites are described by pasture type, so GIS use requires linking to external site shapefiles or coordinates.
- Two sites limit broad spatial generalization; suitable for site-level mapping and temporal analyses when combined with additional data.
- Clear citation requirements: fully cite if data are reused.
- Authors and project details provided for provenance.

## References
- Jones, D.L., Owen, A.G., Farrar, J.F., 2002. Simple method to enable the high resolution determination of total free amino acids in soil solutions and soil extracts. Soil Biol. Biochem. 34, 1893-1902.
- Miranda, K.M., Epsey, M.G., Wink, D.A., 2001. A rapid, simple, spectrophotometric method for simultaneous detection of nitrate and nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L., 1996. Nitrogen - inorganic forms. In Sparks, D.L. (Ed.), Methods of Soil Analysis. Part 3. SSSA, pp. 1123-1184.
- Orsenneau, J.L., Massoubre, C., Cabanes, M., Lustenberger, P., 1992. Simple and sensitive determination of urea in serum and urine. Clin. Chem. 38, 619-623.