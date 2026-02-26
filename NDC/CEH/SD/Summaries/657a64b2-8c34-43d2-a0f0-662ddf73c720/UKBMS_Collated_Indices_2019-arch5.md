# About the UK Butterfly Monitoring Scheme

- This scheme is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers contributing data.
- It provides annual, site-based population status data for UK butterflies, collected since 1976 and covering over 2,500 active sites each year.
- Data come from three sampling frameworks and are analyzed together to understand long-term trends and inform biodiversity policy. Further details are available at the UKBMS website.

## Data collection and sampling framework

- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, recording all butterflies along a fixed-width path (about 5 m), weekly from April to September, ideally 26 counts per year; ~2,000 sites sampled annually.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year (minimum 2 in July/August; spring visits encouraged); ~750 squares sampled per year.
- Targeted surveys: single-species transects and alternative methods, including:
  - Timed counts for specific species
  - Egg and larval web counts in suitable habitats

## Data processing and analysis

- The data yield abundance indices (relative measures of population size) rather than absolute counts.
- Site indices reflect a stable proportion of butterflies present; detectability varies by species.
- Collated indices for each species are created using the Generalised Abundance Index (GAI), with a modification weighting site data by the proportion of the species’ flight period surveyed that year.
- Counts from all methods (Pollard walks, reduced surveys, WCBS) are used to model seasonal patterns and extrapolate for gaps, with observed data given greater influence in the final index.

## Quality control and validation

- Field data are recorded on standard forms and entered online (or via Transect Walker) before uploading to a central database.
- Automated checks flag anomalies (e.g., unusually high counts, records outside known flight periods); regional transect coordinators perform ongoing validation.
- Additional automated and manual validation flags records outside known distribution ranges or atypical for a site/year; data edits are performed after verification.

## Data download details

- The download provides annual collated indices of abundance for species with sufficient data from 1976–2019 (earlier years may lack collated indices for some species).
- Format: comma-separated values (.csv).
- Key columns and meanings:
  - SPECIES CODE: unique species identifier
  - SPECIES: scientific name (Fauna Europaea v2.2)
  - COMMON NAME: vernacular name (Emmet & Heath)
  - YEAR: year of the collated index
  - NO. SITES: number of contributing sites for the index
  - COLLATED INDEX: log10 of the Collated Index (LCI), scaled so the series average equals 2
  - YEAR RANK: rank of the CI value within the species’ years
  - TIME PERIOD: the period used to produce the collated indices
  - COUNTRY: origin country/region for the regional index
- Metadata: species names follow standard taxonomic references; data are provided as a historical time-series resource.

## Licence and attribution

- Open Government Licence (OGL) applies, enabling free use with few conditions.
- Citations/DOIs must be included in any publications using the data.
- Attribution statement to be used with any derived information: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, the Centre for Ecology & Hydrology, British Trust for Ornithology, and the Joint Nature Conservation Committee.

## Collaboration and contact details

- UKBMS partners can provide guidance on dataset use and interpretation.
- Opportunities for co-authorship or intellectual input on publications resulting from UKBMS data.
- Contact:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation (Transect co-ordinator): transect@butterfly-conservation.org