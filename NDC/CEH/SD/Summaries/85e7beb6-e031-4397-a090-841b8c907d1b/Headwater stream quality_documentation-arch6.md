# Headwater stream quality (Countryside Survey)

- A dataset and modelling framework linking headwater stream quality to landscape and site characteristics in Great Britain, based on two survey years (1998 and 2007).

## Experimental design and data collection

- Macroinvertebrates sampled in streams using standard protocols with a single 5–15 m sampling reach, plus a 1-minute hand search, within a three-minute active sampling window.
- Supplemental measurements collected at each site: width, depth, substrate composition.
- BMWP score calculated as a biological quality index; RIVPACS used to generate expected (reference) macroinvertebrate communities based on site characteristics.
- 478 headwater stream sites surveyed across both years, located downstream of mapped sources (1:50,000 scale); sites used for headwater analysis are those where Strahler order is 1–3.
- Samples processed in the lab to record species, BMWP taxa, and RIVPACS status; taxonomy harmonised to a common modern standard; standardisation to derive a mutually exclusive taxa list for species richness.

## Data attributes and spatial reference

- Primary data attribute: Value = Observed BMWP score divided by the Expected BMWP score (ratio of observed to expected).
- Output product: a 1 km raster image representing headwater stream water quality (per headwater stream location).
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Inclusion criteria: areas without Strahler order 1–3 headwater streams are excluded from the models.

## Modeling and analytical methods

- Observed BWMP scores estimated with actual macroinvertebrate data; Expected BWMP scores derived from RIVPACS scores averaged by land class for unmonitored grid cells.
- Relationship between observed and expected stream quality modeled using a Boosted Regression Tree approach.
- Model training and validation performed on a subset of data and then extrapolated to 1 km grid squares containing headwater streams at a national scale.
- Model inputs (Table 2 covariates): 
  - 1) % Arable, 2) % Improved Grassland, 3) % Urban in 1 km square (LCM)
  - 4) % woody cover along the stream within 1 km square
  - 5) Slope over 1 km around the site (from upstream to downstream)
  - 6) Altitude of sampling site
  - 7) Strahler stream order (1, 2, or 3)
  - 8) Easting, 9) Northing
  - 10) Survey year
- Note: Strahler-1–3 streams are the focus; higher-order streams are excluded from these headwater analyses.

## Data processing, quality assurance, and standards

- Data harmonisation: taxa data aligned to a common modern taxonomy; standardisation performed to create a mutually exclusive taxon list for species richness.
- Quality control: adherence to Defra/NERC Joint Codes of Practice; detailed QA steps described in Murphy & Weatherby (2008) and related CS reports.
- Calibration and references: method details and calibration steps described in Murphy & Weatherby (2008) and Dunbar et al. (2018/2010) with supporting methodological papers (e.g., Armitage et al. 1983; Norton et al. 2016).

## Output products and applications

- 1 km raster product representing headwater stream quality (Observed/Expected BWMP ratio) across monitored headwater locations.
- Outputs enable spatial assessment and communication of headwater water quality, and support policy and management decisions at national and sub-national scales.
- Outputs support exploration of relationships between stream condition and landscape/land-cover variables, informing data-driven habitat and water quality strategies.

## References and supporting documents

- Core methodological and contextual references include:
  - Armitage et al. 1983; Murray-Bligh 1999; Murphy & Weatherby 2008; Murphy et al. 2008; Dunbar et al. 2010; Bunce et al. 2007; Morton et al. 2011; Norton et al. 2016.
- Key CS reports and technical documents linked to sampling design, QA, and modelling approaches.

## Data provenance and intended use

- Data originate from Countryside Survey headwater stream monitoring, designed to quantify biological quality and compare observed versus expected community composition.
- Intended for broad use in data-informed decision making, policy support, and landscape-scale analyses of headwater stream condition in relation to land cover and terrain characteristics.