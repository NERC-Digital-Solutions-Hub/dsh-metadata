# Experimental design/collection method

- Context and objective
  - Study of host specificity of Maculinea rebeli by comparing the proportion of caterpillars adopted into different Myrmica nests with the proportion that survived to adulthood or pupation.
  - Data come from one population over four years (2001, 2003, 2004, 2005) near Przemyśl, south-eastern Poland.

- Data collection approaches
  - Adoption proportion
    - Estimated by baiting for ants beneath stratified random samples of gentians.
    - Eggs on each plant counted to derive adoption estimates.
  - Adult estimates
    - Maculinea rebeli adults recorded by eclosing individuals along stratified transects across sites.
    - Nest identified after confirming it contained an empty pupal case.

- Sampling design and notes
  - Nests sampled randomly and are considered distinct within each year.
  - No active measures to prevent sampling the same nest in subsequent years; colonies can vacate and move, making exact cross-year continuity uncertain.
  - If a nest is re-sampled in different years, it is unlikely to contain the same ants; however, certainty about recurring individuals is not possible.

- Data files and structure
  - sabuleti.csv
    - Columns: Observation (number), Year, Frequency (number of Maculinea rebeli found in Myrmica sabuleti nests)
  - scabrinodis.csv
    - Columns: Observation (number), Year, Frequency (number of Maculinea rebeli found in Myrmica scabrinodis nests)

- Data governance and quality considerations for data leaders
  - Clear temporal and spatial scope (one population, near Przemyśl, Poland) and year-by-year sampling.
  - Distinct nest-level observations within each year, with potential cross-year nest turnover complicating longitudinal analyses.
  - Metadata needed: nest identity handling, gentian sampling context, exact transect locations, and criteria for defining adoption versus adult eclosed counts.
  - Future data management should address tracking nest lineage across years if longitudinal analyses are intended, and document any changes in sampling effort or location.