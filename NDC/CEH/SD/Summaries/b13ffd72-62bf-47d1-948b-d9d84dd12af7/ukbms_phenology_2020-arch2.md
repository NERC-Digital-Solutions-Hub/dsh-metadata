# About the UK Butterfly Monitoring Scheme

## 1. About the UK Butterfly Monitoring Scheme
- A collaborative, funded program organized by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee; volunteers contribute data.
- Objective: provide annual data on butterfly population status from a wide-scale, site-based monitoring framework to support understanding of insect population changes and policy-related biodiversity trends.
- Sampling framework includes:
  - Standard butterfly transects (Pollard walks): fixed-route transects, 2–4 km long, visited weekly (up to 26 counts per year) along a 5 m wide belt, across almost 2000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits per year (minimum two visits in July/August; spring visits encouraged), sampling ~800 squares per year.
  - Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focused on specific species.
- Data have been collected since 1976; current activity involves over 2500 actively recorded sites annually.
- All sampling methods are analyzed together to produce a cohesive UKBMS dataset used for status and trend analyses across the UK.
- For policy relevance, outputs support assessments of biodiversity status and trends over time.

Key challenges for analysts
- Increasing the value of monitoring datasets by integrating UKBMS with other relevant environmental data (moving beyond single-use datasets).
- Enabling broad access to the underlying data used to create final outputs.

## 2. Nature of data collected
- Focus on phenology: timing of adult butterfly flight periods (imago stage) across sites and years.
- Phenology metrics are derived from standard Pollard transects (weekly counts during the main activity season); WCBS data are less suitable for phenology due to reduced sampling frequency.
- Metrics include:
  - First and last recording dates at a site for a given year and brood.
  - Peak date and peak count.
  - Flight period length (days between first and last observation).
  - Mean flight date (weighted mean date) and the standard deviation around this date (measure of synchronisation).
  - For multi-voltine species, separate measures for first and second flight periods where possible; for some uni-voltine species (e.g., Brimstone, Peacock) separate early and summer flight periods are provided.
  - For species with overlapping generations, phenology is reported for the entire flight period; for certain species, first and second flight-period data are provided in addition to whole-period measures.
- Use of multiple generations and overlapping flight periods is acknowledged with limitations in separating distinct generations.

## 3. Quality control
- Field data collected on standard forms and entered online via the UKBMS data entry site or Transect Walker; uploaded to a central database.
- Automated checks flag potential data issues (e.g., abnormally high counts, records outside known flight periods); recorders can adjust or accept flagged records.
- Regional coordinators validate data within their region, with ongoing checks throughout the season.
- Post-entry validation includes automated and manual checks for:
  - Records outside known species distributions.
  - Records outside expected flight periods.
  - First-time records at a site.
  - Atypical abundances or marked deviations from local norms.
- Data corrections are performed via bespoke queries and, if needed, consultation with transect coordinators or recorders before updating the main UKBMS dataset.

## 4. Details of this data download
- This download provides phenology data for all species in the UK at all sites and years with sufficient data.
- Data format: comma-separated values (CSV).
- Coverage: thirteen species with full flight-period data (and separate data for two distinct flight periods where possible); for all other species, data cover the entire flight season only.
- Column descriptions:
  - SITENO: unique site number within UKBMS.
  - SITENAME: site name.
  - GRIDREF: 6-figure OS grid reference for the site/start of transect.
  - SPECIES_NAME: binomial scientific name (Fauna Europaea v2.2 reference).
  - COMMON_NAME: vernacular name (Emmet & Heath reference).
  - YEAR: year of phenology metric calculation.
  - NUMBER_OF_BROODS: number of distinct flight periods for which data are separated.
  - BROOD: flight period for the data (0 = entire flight period; 1 = first flight period; 2 = second flight period).
  - FIRSTDAY: day after 1 April when first record was observed for the brood.
  - LASTDAY: day after 1 April when last record was observed for the brood.
  - PEAKDAY: day after 1 April of the peak count.
  - PEAKCOUNT: peak count value.
  - MEAN_FLIGHT_DATE: weighted mean day number after 1 April for the brood.
  - FLIGHTPERIOD_SD: standard deviation around the mean flight date.
  - FLIGHTPERIOD_RANGE: days between firstday and lastday.
  
## 5. Licence and attribution statement
- Data download is provided under the Open Government Licence (OGL), enabling free use and reuse with minimal conditions.
- Required actions:
  - Include full citation with the dataset DOI in any reports/publications using the data.
  - Include the attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © copyright and database right Butterfly Conservation, CEH, BTO, and JNCC.
  
## 6. Offer of collaboration and contact details
- UKBMS Partners offer guidance on dataset details and interpretation of outputs.
- Collaboration opportunities include potential co-authorship and intellectual input for scientific publications, conference presentations, or posters resulting from UKBMS data use.
- Contacts:
  - UK Centre for Ecology & Hydrology, Marc Botham: ukbms@ceh.ac.uk
  - Butterfly Conservation, Transect co-ordinator: transect@butterfly-conservation.org