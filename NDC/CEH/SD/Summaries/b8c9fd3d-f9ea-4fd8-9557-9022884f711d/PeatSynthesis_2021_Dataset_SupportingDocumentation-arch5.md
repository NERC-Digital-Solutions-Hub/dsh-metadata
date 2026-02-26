# Net ecosystem carbon dioxide (CO 2 ) exchange and meteorological observations collected at peatland ecosystems across Wales, Scotland and England, 2008 to 2020

- Overview
  - Time period: 2008–2020; turf/peatland ecosystems across Wales, Scotland and England
  - Data type: time series observations of net ecosystem CO2 exchange (NEE) and supporting micrometeorological observations from thirteen peatland eddy covariance (EC) flux sites
  - Format and access: data provided as a subset of variables in the UK_Peatlands_NEE_Flux_Dataset.zip; full range of variables available via Environmental Data Centre (EIDC) records or by contacting the authors
  - Publication context: supplementary material to Evans et al. (in press)

- Data content and structure
  - Contents: time series of NEE and micrometeorological measurements from 13 peatland EC sites with varying activity periods
  - Key variables included: NEE (g CO2 m^-2 day^-1), NEEunc, air temperature (TA), vapour pressure deficit (VPD), incoming shortwave radiation (SWIN), among others
  - Data format: separate .csv files per site; records spanning site-specific start/end dates (Table 1)
  - Data quality and limitations: missing records denoted by -9999; site-level QC and processing described below

- Study sites
  - Geographic scope: peatlands across Wales, Scotland and England
  - Site types: semi-natural and managed peatlands, including blanket bogs and valley fens; some cropland/grassy peatlands
  - Coordinates: site coordinates not provided in this document for security; can be obtained by contacting the authors
  - Site specifics: 13 sites with varying operational periods (e.g., Crosslochs, Conwy, Moor House, Auchencorth Moss, Cairngorms, Anglesey 1/2, Wicken Fen, Bakers Fen, Tadham Moor, Redmere 1/2, Rosedene)

- Instrumentation and sampling regime
  - Measurements: turbulent fluxes of NEE obtained with eddy covariance (EC) systems above the canopy
  - Data cadence: raw data at 20 Hz; fluxes computed as 30-minute averages
  - Supporting instrumentation: meteorological measurements (TA, RH, SWIN) at or near 2.0 m height; varied by site
  - Site-specific details: Table 2 lists the instrumentation, sensor models, towers, and heights per site

- Data processing, QC and gap filling
  - Processing: EddyPRO Flux Calculation Software used to compute fluxes; includes QC, angle-of-attack corrections, coordinate rotation, corrections for co-spectral attenuation, humidity effects, and density corrections
  - Sign convention: positive NEE = CO2 source to atmosphere; negative NEE = CO2 uptake by ecosystem
  - Quality control: provider-level QC including outlier removal, exclusion during unfavourable conditions, plausible-range checks, and fetch representativeness
  - Footprint assessment: for croplands with limited homogeneous fetch, representativeness assessed via the ART Footprint Tool with >80% flux originating within target ecosystem
  - Data gap filling: Marginal Distribution Sampling via REddyProc for gap-filling of LE and H (and related components); Crosslochs site gap-filling with a generalized additive model
  - Uncertainty: NEEunc provided (2 SD)
  - Data validation: weekly visual checks of flux and ancillary data, removal of clearly erroneous values

- Biomass fluxes for agricultural peatlands
  - Focus: imports/exports of biomass at grasslands and croplands summarized in Table 3
  - Data sources: direct measurements and/or farm records
  - Notable examples: Tadham Moor, Redmere, Rosedene with crops such as hay, lettuce, maize, sugar beet, potatoes; biomass fluxes reported in g C m^-2 for various years

- Data access, governance and provenance
  - Data availability: complete site time series provided as separate CSV files; missing values marked as -9999
  - Documentation and metadata: Table 3 (variables and units) and Table 2 (instrumentation) provide essential metadata; variable descriptions adapted from LI-COR and Reichstein et al. (2016)
  - Access pathways: full variable range via Environmental Data Centre (EIDC) records or by contacting the authors
  - Acknowledgments and funding: multiple UK funders (Defra SP1210/SP1218, NERC, Scottish Government, NRW, UK-SCAPE, and others)
  - Security considerations: site coordinates withheld in this document for security; available on request to authors

- Notes on usage and limitations
  - Time coverage varies by site; dataset is a subset of variables with more complete data accessible through EIDC or authors
  - While processing and QC are robust, users should consider site-specific metadata (start/end dates, heights, instrumentation) when integrating with other datasets
  - Biomass flux data for agricultural peatlands are included for selected sites and years; cross-site comparability may be limited by differing management practices and data sources

- References and provenance
  - Methods and processing references include EddyPRO, footprint modeling, QC protocols, and gap-filling approaches (e.g., Reichstein et al., Moncrieff et al., Papale et al., etc.)
  - Related publications and datasets provide context for site-specific measurements and broader peatland CO2 flux research (e.g., Evans et al., Morrison et al., Helfter et al., Artz et al., etc.)