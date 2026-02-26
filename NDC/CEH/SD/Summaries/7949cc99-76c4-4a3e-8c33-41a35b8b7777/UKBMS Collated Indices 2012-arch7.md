# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK using fixed transects and multiple recording methods.
- All-species transects: fixed-route, 2–4 km long, 45 minutes to 2 hours, 5 m wide belt, sampled weekly April–September (ideally 26 counts/year); transects are chosen to evenly sample habitat types and management activities and remain fixed for year-to-year comparison.
- Other methods: single-species transects (same methodology but for one focal species), timed counts, and egg/larval web counts.
- Transect timing and weather criteria: walks occur 10:45–15:45 under suitable butterfly activity conditions (dry, wind < Beaufort 5, 13°C+ with ≥60% sunshine or >17°C if overcast).

- Data collection methods: field data on standard forms; entered into Transect Walker software; input by recorder or regional transect coordinator; regional coordinators compile data for their region; Transect Walker files uploaded to an Oracle database.

- Analytical framework: after validation, a General Additive Model (GAM) imputes missing values and computes site indices; site indices from all methods are combined to produce a national Collated Index per species. Where sites are not monitored every year, a loglinear regression model estimates missing values, accounting for year and site effects. Collated Indices are updated annually; only species recorded from five or more sites per year are included.

- Nature and units of recorded values: site indices are relative measures of population size, not absolute counts; collated indices are presented as the base-10 logarithm (Log10 Collated Index) and are scaled so that the average index over the series equals 2, enabling relative comparisons over time.

- Quality control: automatic checks in Transect Walker flag data-entry issues (e.g., unusually high counts, records outside flight periods); regional coordinators validate records; additional automated/manual validation screens for out-of-range distributions, unusual flight periods, first-time site records, and extreme abundances.

- Format of stored data: Collated Indices stored as CSV; key columns include Species (scientific name per Fauna Europaea v2.2), Common name, Year, No. Sites, Collated Index, Time period.