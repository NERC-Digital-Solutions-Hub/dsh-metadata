# Overview of the dataset

- This dataset records net ecosystem CO2 exchange (NEE) and methane (CH4) fluxes measured at a hemi-boreal ombrotrophic fen in Southern Sweden (Mycklemossen) using an automated chamber system (SkyLine2D) from August 2017 to September 2019.
- Four ecotypes were studied to assess drought responses: sphagnum, eriophorum, heather, and open water (water); the 2018 drought year is included for drought vs. nondrought comparison, with recovery data from 2019.
- Primary responsible researchers for data collection and interpretation are Ben Keane, Sylvia Toet, Phil Ineson, Per Weslien, James Stockdale, and Leif Klemedtsson; Sylvia Toet is the initial contact.

## Site and ecological context

- Location: Mycklemossen bog-like fen, ombrotrophic, ~100 km north of Gothenburg, Sweden (59?; coordinates 58.36732626 N, 12.16856373 E; ca. 75 m above sea level).
- part of Skogaryd research catchment, monitored since 2013.
- Vegetation: predominantly heather, sphagnum moss, and sedges, with year-round open water areas possible.
- 2018 drought: reduced rainfall, higher temperatures, greater solar radiation; 2019 conditions served as a nondrought reference.

## Experimental design

- In January 2017 a transect including all vegetation types was established with spatial blocks and random replicate points.
- For each block, 24 measurement points were defined across ecotypes: eriophorum (n=6), heather (n=6), sphagnum (n=6), and open water (n=6).
- At each point a 20 cm inner-diameter, 10 cm-high PVC collar was installed ~2 cm below surface (or into sediment at water points).

## Measurement methods and instruments

- Instrumentation: SkyLine2D automated chamber system (assessed in Keane et al. 2018).
- Chamber: clear Perspex cylinder (20 cm diameter, 40 cm height) on a motorized trolley; cycle visits pre-selected points along transect.
- Measurement cadence: approximately 2.5 hours per full cycle, yielding roughly 10 measurements per day per chamber.
- Gas analysis: CO2 and CH4 measured in the headspace using a LI-8100 infrared gas analyser and a cavity ring-down laser (LGR UGGA-91); no chamber fan used.
- Data capture: headspace gas concentrations recorded with a data logger.
- Flux calculation: linear regression of concentration changes; minimum 20 seconds deadband for mixing; specific warmth for CO2 (90 s window) and CH4 (240 s window).
- Corrections: fluxes adjusted for area, air temperature, gas volume; daylight CO2 flux adjusted using the light response curve to account for chamber attenuation.

## Data processing and quality control

- Software: SAS 9.4 used for data manipulation and analyses; QC with R^2 for CO2 flux (<0.9 flagged/discarded); CH4 flux regressions require P < 0.05 to be accepted; otherwise treated as zero flux.
- Outlier handling: values beyond ±1.96 standard errors excluded.
- Night-time/atmospheric conditions: filters applied to avoid overestimation during still atmospheric nights (per Koskinen et al. 2014; Lai et al. 2012).
- Additional screening: fluxes were discounted if the mean CO2 concentration before and after chamber closure dropped by more than 25 ppm (per Jarveoja et al. 2020).
- Result: 329 fluxes excluded based on quality criteria.

## Data structure and metadata

- File structure: a single table with eight columns in the following order:
  - DATETIME: Date and time of flux measurement (units: dd:mmm:yyyy:hh:mm:ss)
  - DATE: Date of measurement (units: dd/mm/yyyy)
  - TIME: Time of measurement (units: hh:mm:ss)
  - PLOT: Experimental plot number (numeric)
  - ECOTYPE: Dominant vegetation type at the plot (string: sphagnum, heather, eriophorum, water)
  - BLOCK: Block number of experimental design (numeric)
  - CH4_flux: Methane flux (units: nmolm^-2 s^-1)
  - CO2_flux: Net ecosystem exchange of CO2 (units: µmol m^-2 s^-1)
- Data dictionary and units are provided to support reuse and interoperability.

## Provenance, contact, and references

- Data collection and interpretation credited to the listed researchers; primary contact for the dataset is Sylvia Toet.
- The dataset is described in related publications, including Keane et al. (2021) on carbon dioxide and methane flux responses to drought, and supporting methodological references (e.g., Heinemeyer 2013; Koskinen 2014; Lai 2012; Jarveoja 2020; Mosier 1989).

## Data governance and stewardship considerations

- Clear provenance and responsibility: explicit authorship and contact person for inquiries.
- Rich metadata and data dictionary: supports discoverability, interoperability, and reuse.
- Quality assurance traceability: explicit QC criteria and exclusion rules documented for reproducibility.
- Update and availability: methodologies for data processing and criteria for data acceptance are stated, enabling ongoing updates and maintenance, with issues such as data availability and potential embargo given consideration in the broader governance context.