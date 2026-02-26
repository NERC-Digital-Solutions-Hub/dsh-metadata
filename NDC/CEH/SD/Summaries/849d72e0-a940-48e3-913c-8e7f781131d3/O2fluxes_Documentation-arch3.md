# Overview of data

## Purpose and scope
- Compilation of results from the stream metabolism component of the NERC Macronutrients consortium, led by Prof. Mark Trimmer, titled "The role of lateral exchange in the seaward flux of C, N and P."
- Aims to quantify oxygen fluxes to understand benthic and water-column metabolism in rivers with varying land–river connectivity within the Hampshire Avon catchment.

## Methods and data collection
- Four field campaigns conducted across seasons: spring 2013, summer 2013, autumn 2013, and winter 2014.
- Measurements include:
  - Benthic O2 fluxes using aquatic eddy covariance (AEC) with processing following Attard et al. (2014) and Rovelli et al. (2015).
  - Water-column O2 fluxes from 100 mL bottle incubations over 24 hours with optical O2 sensors.
- Data describe O2 production and consumption rates in both benthic and water-column compartments.

## Sites and temporal coverage
- Six tributaries of the Hampshire River Avon catchment: CE1 (River Ebble), GA2 (River Avon), GN1 (River Nadder), CW2 (River Wylye), AS1 (tributary of the River Sem), AS2 (River Sem).
- Specifics:
  - CE1 not sampled during winter due to extensive flooding.
  - Winter and autumn data at GA2 did not meet quality requirements and were omitted.

## Data structure and variables
- Column headers and meanings:
  - Campaign: season of data collection.
  - Site: sampling location within each campaign.
  - Depth: average stream depth (m) from flow transects.
  - Day flux (b): average daytime benthic flux (mmol/m2/h) with SE; number of data averaged shown in parentheses.
  - Night flux (b): average nighttime benthic flux (mmol/m2/h) with SE; number of data averaged shown in parentheses.
  - Total PAR (b): daily-integrated PAR at streambed (mol/m2/d).
  - Daylight (b): daytime duration (hours) at streambed; nighttime threshold: 2 µmol quanta/m2/s.
  - Day flux (w): average daytime flux in the water column (µmol/L/h); below-detection values shown as <0.1.
  - Night flux (w): average nighttime flux in the water column (µmol/L/h); below-detection values shown as <0.1.
  - Total PAR (w): daily-integrated PAR in the water column near the surface (mol/m2/d).
  - Daylight (w): daytime duration (hours) based on surface PAR measurements.
- Units and measurement context:
  - Benthos fluxes in mmol/m2/h; water-column fluxes in µmol/L/h.
  - PAR and daylight metrics captured at both streambed and near-surface water-column locations.
- Missing data are marked as not determined (n.d.).

## Data processing and references
- Processing and methodologies aligned with:
  - Aquatic eddy covariance (AEC) principles (Berg et al., 2003).
  - Protocols described in Attard et al. (2014) and Rovelli et al. (2015).
- Descriptions and additional context for the datasets are provided in Rovelli et al. (submitted) and related works (Rovelli et al. 2015; Rovelli et al. 2016).
- Data availability and provenance are linked to the NERC Macronutrients project and dataset records (e.g., data centre entry with DOI).

## Data accessibility and governance notes
- The dataset accompanying this overview is O2fluxes_Avon.CSV.
- Data include site coordinates and campaign metadata, with explicit notes on data that did not meet quality criteria and thus were omitted.
- Metadata completeness can be a barrier in some cases; this entry provides explicit column definitions and quality notes to support reuse and transparency.

## Relevance to monitoring frameworks and policy
- Demonstrates an end-to-end workflow for environmental health monitoring:
  - Selection of relevant aquatic metabolism measures (benthic and pelagic O2 fluxes) across multiple sites and seasons.
  - Transparent data collection, processing, and documentation to support interpretation of stream metabolism and carbon/nutrient dynamics.
  - Clear articulation of data limitations and quality controls to inform future monitoring design and governance.

## Limitations and caveats
- Not all seasonal data are complete for all sites (e.g., GA2 autumn/winter omitted; CE1 winter unavailable due to flooding).
- Some measurements below detection or excluded due to quality highlight the importance of robust data governance and metadata practices for ongoing monitoring.