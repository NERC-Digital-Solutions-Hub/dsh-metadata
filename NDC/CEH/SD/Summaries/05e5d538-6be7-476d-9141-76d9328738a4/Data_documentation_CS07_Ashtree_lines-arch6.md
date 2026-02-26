# Countryside Survey: Ash tree distribution in woody linear features 2007

- The document presents estimates of ash trees for Great Britain within woody linear features, based on Countryside Survey 2007 data.
- Data are organized for two woody linear feature types: lines of trees (hedgerows) and belts of trees, including natural and unnatural shapes.
- The dataset supports national-scale estimation by stratifying sampling across land classes and applying area-weighted aggregation.

## Data and coverage

- Extent: Great Britain
- Resolution: 1 km
- Coordinate system / projection: British National Grid (OSGB1936)
- Associated datasets: ITE Land Classification (2007); Countryside Survey outputs (UK CS 2007)
- Data are produced from a stratified random sample of 1 km squares across GB, linked to land classes representing ecological gradients (so that national estimates can be scaled from sample data)

## Dataset contents and columns

- LC2007 (numeric Land Class)
- LC2007_COD (text Land Class code)
- LC_2007 (land class description; same as LC2007 but with no code for LCs where no hedges occur)
- Area of Land Class (m2; from the original land classification file)
- Size_of_LC (area-related metric)
- WNS_km: length of ash in natural-shaped woody linear features (in km per land class)
- WUS_km: length of ash in unnatural-shaped woody linear features (in km per land class)
- Belt_km: length of ash in belts of trees (in km per land class)
- All_WLF_km: total of WNS_km, WUS_km, and Belt_km (ash length in all woody linear features)
- Mean_km_km: mean length of all linear features per km2 (per land class)

## Methods and interpretation

- Sampling design: 1 km squares sampled using stratified random sampling based on land classes (ecological gradients, soils, geology, climate)
- For lines of trees (Natural Shape): ash proportion is recorded in species bands (e.g., <10%, 10-25%, ..., 95-100%, “Individual Tree”)
- Ash length per 1 km square is estimated using the midpoints of these proportion bands
- National estimates: mean ash length per sampling stratum is multiplied by the area of each Land Class and summed to produce country-wide totals
- For belts of trees: similar methodology; belts of shrubs/trees included; ash length estimated across belts
- In unnatural-shape WLFs, species composition is recorded as mixed, >50% hawthorn, or >50% other; ash proportion is inferred using adjacent D plots (vegetation diversity plots next to hedges)
- D plots provide total percentage cover for each species; ash length estimates are derived by applying mean percentage cover from D plots to hedge length within each sampling stratum

## Practical use and insights

- Enables exploration and visualization of ash distribution within hedgerows and belts across GB
- Supports data products (dashboards, pivot-like summaries) to enable self-serve analysis of ash presence in woody linear features
- Can inform monitoring related to ash presence and changes in hedgerow structure across land classes
- Can be integrated with other Countryside Survey outputs for broader landscape and ecological analyses
- Useful as a historical baseline (2007) for tracking changes in ash distribution and informing disease risk assessments and hedgerow management decisions

## Considerations and limitations

- Data reflect 2007 survey methods and sample design; subsequent years require careful comparability
- Ash proportions in certain WLF categories rely on midpoints of bands or adjacent vegetation plots, which introduces estimation uncertainty
- Some woody features are categorized by shape (natural vs unnatural) with different data collection approaches
- Data are provided at the land-class level and require area-weighted aggregation to obtain country-scale estimates

## References and further information

- Distribution methods and related CS outputs: www.countrysidesurvey.org.uk
- Related readings and methodological sources listed in the document, including:
  - Distribution of Ash trees in Countryside Survey data (2013)
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - CS Sampling Strategy and related land classification references
  - LCM2007 and associated reporting on land cover and class areas