# UK Butterfly Monitoring Scheme data download: phenology data

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee; it has monitored butterfly populations since 1976 with volunteer data contribution and about 2,500 active sites annually.
- Data come from multiple sampling frameworks (Pollard walks, stratified random WCBS, and targeted surveys) and are analyzed together to track status and biodiversity trends.
- The dataset described is a phenology-focused data download provided as a CSV, capturing timing metrics of adult butterfly flight periods across species, sites, and years.

## Data scope and contents
- Phenology covered: timing of adult butterfly flight periods on UKBMS transects; includes measures such as first/last recording dates, peak day and count, and flight period length.
- Metrics:
  - Simple: firstday, lastday, peakday, peakcount, flight period range (length).
  - Advanced: mean flight date (weighted), flight period SD (synchrony).
- Generational detail:
  - Some species (13) have data for entire flight period plus separate first and/or second flight periods.
  - For multivoltine and some uni-voltine species (e.g., Brimstone, Peacock), separate broods are reported where possible; for others, only the entire flight period is available.
- Coverage limitations:
  - Phenology calculations rely on standard transects with weekly counts (WCBS provides fewer time points).
  - Flight-period measures may be less accurate where recording is incomplete or outside the standard UKBMS season (April 1 – Sept 30).

## Data schema and columns
- File format: comma-separated values (.csv).
- Key columns:
  - SITENO, SITENAME, GRIDREF
  - SPECIES_NAME (scientific), COMMON_NAME
  - YEAR
  - NUMBER_OF_BROODS, BROOD (0 = entire period; 1 = first brood; 2 = second brood)
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

## Data quality and governance
- Data capture: field recording forms; online entry via UKBMS.mydata or Transect Walker; data uploaded to a central database.
- Validation workflow:
  - Automated checks during entry (e.g., unusual counts, out-of-season records).
  - Regional transect coordinators review records and conduct ongoing checks during the season.
  - Additional automated/manual validation flags records outside known distributions, atypical abundances, or unusual timing; corrections are made via queries and coordination with data collectors.
- Provenance and metadata: site identifiers, grid references, species taxonomy aligned with Fauna Europaea and common references; validation leverages Butterfly Conservation BNMs and existing UKBMS data.

## Licensing, attribution, and reuse
- Licence: Open Government Licence (OGL); permits free use with standard conditions.
- Citation: must include the dataset citation/DOI as specified in the metadata.
- Attribution: any derived information or imagery must credit UKBMS data © Butterfly Conservation, CEH, BTO, JNCC.

## Collaboration and contact
- Partners offer advisory support, interpretation assistance, and potential co-authorship for publications arising from UKBMS data.
- Contacts:
  - Marc Botham, UKBMS@ceh.ac.uk (UK Centre for Ecology & Hydrology)
  - Transect Co-ordinator, transect@butterfly-conservation.org (Butterfly Conservation)

## Practical notes for Data Stewards
- Data governance: ensure consistent use of site and species identifiers, metadata standards, and licensing terms; maintain provenance and data lineage.
- Data discovery and sharing: CSV format facilitates portal-based sharing; ensure proper metadata is available for discovery.
- Data quality: maintain automated and manual validation routines; monitor for updates and corrections; document changes to the main dataset.
- User needs and interoperability: phenology metrics support a range of analyses (timing, duration, synchrony) but be aware of limitations for species with incomplete weekly coverage or complex multi-generation patterns.
- Next steps: capture user requirements, maintain clear data dictionaries, and coordinate with UKBMS partners for updates and potential collaborations.