# Supporting Information for data deposit EIDCHELP-29311

- This document describes a factorial experiment investigating how daily temperature fluctuations and host resource degradation affect life history traits in a Plodia interpunctella – Venturia canescens host–parasitoid system.
- The data are organized into separate datasets corresponding to temperature series and life history measurements for unparasitized hosts and parasitized hosts.

## Aim and scope

- Characterizes individual responses over a single generation under controlled conditions.
- Evaluates combined effects of:
  - Daily stochastic temperature fluctuations vs. constant temperatures
  - Host diet degradation levels (0, 25, 50, 75% replacement with methyl cellulose)
- Data include development, survival, and morphological measurements for hosts and parasitoids.

## Experimental design and treatments

- System: Plodia interpunctella (host) and Venturia canescens (parasitoid).
- Organisms: Hosts from laboratory stock; parasitoids from a parthenogenetic strain.
- Environment: Constant 28°C rearing prior to experiments; experimental treatments conducted at mean 26°C.
- Temperature treatments:
  - Constant (CST): mean 26°C with no fluctuation
  - Variable (VAR): 26°C ± 1.5°C daily fluctuations (range 22.3–30.2°C; AR(1)=0.02)
- Diet treatments:
  - Degradation levels: 0, 25, 50, 75% of wheat germ replaced with methyl cellulose
- Design: Full factorial combination of temperature × diet
- Duration: Life history assay spanned 74 days starting on day 5 of the temperature time series

## Life history assays

- Unparasitized hosts: 40 individuals per temperature/diet treatment
- Parasitized hosts: 25 hosts per temperature/diet treatment
- Procedures:
  - Unparasitized eggs kept individually with 0.3 g diet; monitored daily
  - Parasitized eggs grouped (8 groups of 100 eggs) and parasitized over 3 days (days 20–22)
  - Post-parasitism, larvae kept individually under assigned temperature/diet for monitoring

## Datasets and key variables

- VariableTemperatureTimeSeries_DQE.csv
  - DAY: day in the temperature time series
  - Date: date of temperature; Week: experimental week (0 seed to 1+ by emergence)
  - Temp: temperature (°C)

- LHE-LH-Data_DQE_Pi.csv (Host life history data, unparasitized)
  - Treatment: combination of species (Pi), temperature (Cst/Var), and diet level (0,25,50,75)
  - Individual / Individual code: unique identifiers
  - Diet: degradation level (0–75)
  - Temperature: CST or VAR
  - Starting_Date: experiment start date per individual
  - Egg_viability, Egg_status, Hatching date, Adult_emergence-date
  - Date_of_death, Sex
  - Egg_length, Leg_length (body size proxy)
  - Date_leg_photo_taken, Leg_measured, leg_side (R/L)
  - Comments: additional daily monitoring notes

- LHE-LH-Data_DQE_PiVc.csv (Host-parasitoid life history data)
  - Treatment, Diet, Temperature, Individual, Individual code
  - Starting_Date, Vc_mother_ID, Vc_mother_stock_origin, Vc_mother_age
  - Pi_larval_stage_at_parasitism, Pi_larvae_mass_at_parasitism, Pi_sex
  - Time_at_parasitism, Adult_emergence_date
  - Parasitism_outcome (e.g., 'Live Pi', 'Live Vc', 'Pi-Vc death before emergence', NA)
  - Date_of_death, Date_photo_taken, Leg_length, Leg_measured
  - Parasitism_observer, comments

## Data quality and provenance

- Quality control: Data checked for entry errors; outliers rechecked in early analysis stages.
- References for experimental design and data interpretation:
  - Boots (2011)
  - Cameron, Wearing, Rohani & Sait (2007)
  - Harvey, Harvey & Thompson (1994)

## GIS-relevant considerations and opportunities

- Structure and metadata quality support GIS-like data product development:
  - Clearly defined treatments and temporally explicit observations enable faceted filtering by temperature regime and diet level.
  - Time-series (VariableTemperatureTimeSeries_DQE.csv) can be linked with environmental context datasets or experimental layout maps if spatial metadata of microcosm arrangement is available.
  - Non-spatial data can be mapped conceptually (e.g., visualization dashboards) to illustrate treatment effects across conditions, and can be spatially augmented if experimental grid coordinates are provided.
- Data integration potential:
  - Combine with external environmental data (precise temperature profiles, humidity) to build spatiotemporal visualizations of treatment effects.
  - Cross-reference host and parasitoid life history metrics to create network or flow diagrams illustrating outcomes by treatment.
- Key considerations for GIS-style data products:
  - Ensure consistent data standards and units across datasets (dates, temperatures, mass in mg, lengths in mm).
  - Maintain linkage keys across datasets (Treatment, Individual, Diet, Temperature) to enable joined analyses and visualizations.
  - Preserve date formats and time stamps to support temporal analyses and animation of experimental progression.

## References

- Boots, M. (2011) The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
- Cameron, T.C., Wearing, H.J., Rohani, P. & Sait, S.M. (2007) Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.
- Harvey, J.A., Harvey, I.F. & Thompson, D.J. (1994) Flexible larval growth allows use of a range of host sizes by a parasitoid wasp. Ecology, 75, 1420-1428.