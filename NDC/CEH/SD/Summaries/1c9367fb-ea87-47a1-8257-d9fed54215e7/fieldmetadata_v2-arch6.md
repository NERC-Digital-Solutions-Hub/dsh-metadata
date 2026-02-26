# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

- Overview
  - A long-term, multisite field trial of Pinus sylvestris (Scots pine) conducted in Scotland.
  - Seed collected in March 2007 from ten trees in each of 21 native Scottish populations; germinated and grown at the James Hutton Institute, Aberdeen.
  - Populations chosen to represent the species’ native range in Scotland, including three populations from each of seven seed zones.
  - Field trial established in 2012 at three sites: Yair (FS, Scottish Borders, southern Scotland), Glensaugh (FE, eastern Scotland), and Inverewe (FW, western Scotland).
  - Trees transplanted in 2012; a mix of nursery origins contributed to field cohorts (NW, NG, NE nurseries), with FW including trees from all three nurseries.
  - Experimental design: randomised blocks with 3 m x 3 m spacing; guard row around the blocks; each block contained one tree from eight of the ten families per population (168 trees per site). Some family replacements occurred at FS due to insufficient trees.
  - Across-site representation: most families (N = 159) represented at each site; a few (N = 9) replaced at one site.

- Data collection and time frame
  - Growth measurements:
    - Height measured end of each growing season 2013–2020 at FE and FW; 2014–2020 at FS (start year differs by site).
    - Basal stem diameter measured end of each growing season 2013–2020 at FE and FW; 2020 only at FS.
  - Phenology (spring assessments) conducted 2015–2019; 2020 assessments not possible due to COVID-19 restrictions.
  - Field sites and coordinates:
    - FE (Glensaugh): latitude 56.893567, longitude -2.535736
    - FS (Yair): latitude 55.603625, longitude -2.893025
    - FW (Inverewe): latitude 57.775714, longitude -5.597181

- Data product and structure
  - Dataset file: FieldTraits.txt
  - Key data dimensions captured:
    - PopulationCode and Description; PopulationCode Unit (NA)
    - Family (mother-tree code; half-siblings assumed)
    - FieldSite (FE, FS, FW) and FieldCode (unique tree code; NA if not transplanted)
    - Block and Row/Column position within the field layout
  - Measured traits and time series (examples):
    - Height measurements: HA13–HA20 (height after 7th to 14th growing seasons; in mm)
    - Height increments: HI13–HI20 (yearly height increment; mm)
    - Basal stem diameter: DA13–DA20 (base diameter; mm)
    - Base diameter increments: DI14–DI20 (incremental changes; mm)
    - Budburst phenology: BD15–BD19 (duration from budburst stages; days)
    - Budburst timing: BT15_4 to BT20_6 (days since 31 March 2015/2016/2017, to reach budburst stages 4–6)
  - Additional details:
    - FieldCode ranges by site (e.g., Inverewe codes 5001–5672, 6001–6004, 7001–7672)
    - Data include descriptors for each variable (units noted, e.g., mm for height/diameter, days for phenology)

- Notes on data context and quality
  - Seeds and provenance establish a broad, representative genetic sampling across Scotland.
  - Differences in site start years and nursery origins introduce cross-site variation to be accounted for in analyses.
  - COVID-19 in 2020 interrupted phenology assessments at all sites.
  - Some populations/families were replaced at certain sites due to insufficient trees, which may affect cross-site comparability for a few entries.

- Relevance and potential uses for data support
  - Enables cross-site and cross-population analyses of growth trajectories, wood formation metrics, and phenology under multi-site environmental conditions.
  - Facilitates creation of dashboards or self-serve data products to explore growth (height, diameter), growth increments, and budburst timing across sites, years, populations, and families.
  - Supports investigations into genotype-by-environment interactions, provenance effects, and the influence of nursery origin on field performance.
  - Useful for policy and management contexts where data from non-specialist organisations (e.g., local councils) are used to inform forestry and conservation decisions.