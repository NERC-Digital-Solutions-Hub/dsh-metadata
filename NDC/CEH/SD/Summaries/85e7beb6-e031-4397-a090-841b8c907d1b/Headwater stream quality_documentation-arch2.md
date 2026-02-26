# Headwater stream quality (Countryside Survey)

- Purpose: Monitor headwater stream health across Great Britain by using macroinvertebrate indicators and model-based expectations to assess environmental condition and support policy evaluation over time.

## Experimental Design and Sampling

- Macroinvertebrates sampled with standard protocols (Murray-Bligh 1999; Murphy & Weatherby 2008).
- At each site, a single stream-bed area is sampled within three minutes of active searching plus one minute of hand searching.
- Survey length typically 5–15 meters, depending on stream width.
- Collection uses a standard Freshwater Biological Association pond net and samples are sent to CEH for sorting and identification.
- Supplemental site measurements include width, depth, and substrate, required for running RIVPACS.
- BMWP scoring is calculated per site to assess biological quality, based on taxa sensitivity to organic pollution.

## Data Processing and Modelling

- RIVPACS is used to compute an expected (reference) macroinvertebrate community for a site based on its physical characteristics.
- Observed vs. expected BMWP (O/E BWMP) scores determined for 478 headwater sites across two survey years (1998 and 2007); sites sampled in both years downstream of the source as shown on 1:50,000 maps.
- Pooled data from both years to model relationships between headwater stream quality and catchment/stream characteristics.
- Boosted Regression Tree modelling estimates observed water quality (Observed BMWP) and extrapolates to 1 km grid squares containing headwater streams at national scale.
- Expected BMWP scores are calculated using RIVPACS scores averaged by land class for randomly generated river sampling sites in unmonitored grid squares.
- Outputs are presented as a 1 km raster image; each headwater stream location is represented by a colored 1 km square. Excludes areas without Strahler order 1–3 headwater streams.

## Key Metrics and Data Products

- Water quality measure: Observed BMWP score divided by Expected BMWP score (O/E BWMP).
- Spatial reference: OSGB 1936 / British National Grid (EPSG:27700).
- Model parameters (1 km square): % arable, % improved grassland, % urban; % woody cover along the stream; slope (1 km window); altitude; Strahler stream order (1–3); Easting; Northing; survey year.
- Data attributes: Value = Observed BWMP / Expected BWMP.

## Collection Methods and Analytical Procedures

- Field collection: pond net in a 5–15 m reach; 3 minutes active sampling plus 1 minute search; measurements of width, depth, substrate; protocols described in Murphy & Weatherby (2008).
- Laboratory processing: identify species, count BMWP taxa, assign RIVPACS status; harmonise taxa to a common modern taxonomy; standardise to derive a mutually exclusive taxa list for species richness.

## Quality Assurance and Calibration

- Follow Defra/NERC Joint Codes of Practice throughout.
- Calibration and methodological details documented in Murphy & Weatherby (2008) and Dunbar et al. (2010).

## Data Accessibility and Storage

- Data are produced in a georeferenced raster format (1 km resolution) for national-scale headwater stream quality.
- Model and dataset integration rely on land cover data (e.g., Morton et al. 2011) and established QA procedures; outputs intended for storage and upload to appropriate data portals.

## References and Supporting Documents

- Armitage et al. (1983) BMWP scoring methodology.
- Bunce et al. (2007) Land classification for GB.
- Dunbar et al. (2010) Countryside Survey headwater streams report.
- Morton et al. (2011) Land Cover Map 2007.
- Murphy & Weatherby (2008); Murphy et al. (2008) Freshwater Manual and QA reports.
- Norton et al. (2016) on scale in ecosystem service indicators.
- Additional methodological details in Murphy & Weatherby (2008) and Dunbar et al. (2010).