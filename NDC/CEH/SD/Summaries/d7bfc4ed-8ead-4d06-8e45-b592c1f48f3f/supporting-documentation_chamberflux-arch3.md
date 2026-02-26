# Net ecosystem exchange and methane fluxes measured from a hemi-boreal ombrotrophic fen in Southern Sweden

- Purpose and scope
  - Provides near-continuous greenhouse gas flux measurements (CO2 and CH4) to assess carbon balance and responses to drought.
  - Data span August 2017 to September 2019, enabling drought versus nondrought year comparisons (2018) and recovery assessment (2019).

- Site description
  - Location: Mycklemossen, an ombrotrophic fen north of Gothenburg, Sweden (approx. 58.3673 N, 12.1686 E; ca. 75 m a.s.l.).
  - Part of the Skogaryd research catchment, monitored since 2013.
  - Vegetation: four ecotypes—Sphagnum, Eriophorum vaginatum (eriophorum), Calluna vulgaris (heather), and open water.
  - Hydrology: typically high water table with some year-round open water; 2018 drought year had reduced rainfall and higher temperatures and solar radiation.

- Experimental design
  - January 2017: transect established across all vegetation types with spatial blocks.
  - 24 measurement points: 6 replicates per ecotype (sphagnum, heather, eriophorum, water) distributed along the transect.
  - PVC collars installed at each point (20 cm inner diameter, 10 cm height, ~2 cm below soil or sediment).

- Greenhouse gas flux measurements
  - Instrumentation: SkyLine2D automated chamber system (University of York) with a clear cylindrical chamber (20 cm diameter, 40 cm height) on a motorised trolley.
  - Sampling: chamber lowered to a collar to measure flux over ~4 minutes; cycle total ~2.5 hours; ~10 measurements per day per collar.
  - Gas analysis: headspace analysed sequentially with LICOR LI-8100 for CO2 and a cavity ringdown laser (LGR UGGA-91) for CO2 and CH4.
  - Chamber characteristics: no dedicated fan; previous tests showed no significant difference with/without fan; air flow deemed sufficient for mixing.
  - Data: collected on a data logger; fluxes calculated from rate of change in gas concentrations; adjustments for area, temperature, gas volume, daylight light response for CO2.

- Data processing and quality control
  - Software: analyses conducted in SAS 9.4; QC and filtering aided by R.
  - CO2 flux QC: R^2 of CO2 flux regression must be ≥ 0.9.
  - CH4 flux QC: CH4 flux regressions must have P < 0.05 to be accepted; otherwise treated as zero flux.
  - Outlier handling: data points outside ±1.96 standard errors of the mean flux excluded.
  - Night-time/atmospheric conditions: additional filtering to remove overestimations during still night conditions.
  - Specific rejection rule: fluxes where pre- and post-chamber CO2 concentrations dropped by >25 ppm in a 20-second window were discounted.
  - Result: 329 flux measurements excluded.
  - Metadata and units: dataset described in detail; eight columns (see below).

- Nature and units of recorded values; data structure
  - Dataset consists of one table with eight columns:
    - DATETIME: date-time of flux measurement (dd:mmm:yyyy:hh:mm:ss)
    - DATE: date of measurement (dd/mm/yyyy)
    - TIME: time of measurement (hh:mm:ss)
    - PLOT: experimental plot number
    - ECOTYPE: dominant vegetation type per plot (sphagnum, heather, eriophorum, water)
    - BLOCK: block number in the experimental design
    - CH4_flux: methane flux (nmol m^-2 s^-1)
    - CO2_flux: net ecosystem exchange of CO2 (µmol m^-2 s^-1)
  - References for methodological context
    - Heinemeyer et al. (2013) on evaluating automated chamber-derived carbon balance
    - Jarveoja et al. (2020) on diel patterns in peatland respiration
    - Keane et al. (2018, 2021) on flux measurements and drought response
    - Koskinen et al. (2014); Lai et al. (2012) on night-time flux measurement challenges
    - Mosier (1989) on chamber and isotope techniques

- Relevance for monitoring and policy frameworks
  - Demonstrates a rigorous, transparent workflow from field measurements to QC and data curation, appropriate for monitoring environmental health indicators (GHG fluxes) under climate stressors (e.g., drought).
  - Highlights the importance of:
    - Defined experimental design with replicated ecotypes to capture ecosystem response variability.
    - Automated, high-frequency data collection to improve temporal resolution of flux dynamics.
    - Clear QC criteria and documentation of data exclusions to ensure reliability and reproducibility.
    - Detailed metadata and units to facilitate data reuse and governance.
  - Policy-relevant insights include potential to inform carbon balance assessments under drought, resilience of peatland ecosystems, and the role of different vegetation types in GHG flux responses.