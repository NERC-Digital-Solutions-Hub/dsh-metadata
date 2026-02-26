# Brief description of the project, experimental design and data recorded

- A controlled laboratory study on how coloured environmental variation in temperature affects life history and population dynamics in the host Plodia interpunctella and its parasitoid Venturia canescens.
- Environmental variation is described by colour: blue (rapid fluctuations), red (slow fluctuations), and white (random fluctuations); compared against a constant 26°C regime (CST).
- Two main experimental components:
  - Life history experiment (single generation): unparasitized and parasitized Plodia larvae tracked under seven temperature time series (CST, B1, B2, R1, R2, W1, W2).
  - Microcosm experiment (up to ~7 host generations): host-alone (Pi) and host-parasitoid (Pi-Vc) microcosms across 7 time series, with four replicates per combination, monitored weekly.
- A bacterial infection (Bacillus thuringiensis) occurred around week 34, influencing post-infection data collection; infection status is tracked throughout.

## Experimental design and treatments

- Species and system:
  - Host: Plodia interpunctella (Pi)
  - Parasitoid: Venturia canescens (Vc)
- Temperature treatments:
  - Constant: CST (mean 26°C, no fluctuation)
  - Coloured regimes: blue (B1, B2), red (R1, R2), white (W1, W2)
- Experimental scope:
  - Life history: 50 unparasitized and 26 parasitized host larvae per treatment
  - Microcosms: 4 replicates per microcosm type (Pi and Pi-Vc) per time series; total 56 microcosms (4 × 2 × 7)
- Data collection:
  - Weekly counts of hosts and parasitoids, instar stages, pupae, and body size proxies
  - Replenishment of diet each week
  - Host fecundity measurements and common garden experiments to assess transgenerational effects
- Infection event:
  - Bt infection began around week 34, with some microcosms affected; post-infection data are flagged and recommended for exclusion in certain analyses.

## Temperature time series design

- Time series length: 458 days per coloured treatment
- Autocorrelation:
  - White: AR(1) ≈ 0
  - Blue: AR(1) ≈ -0.70
  - Red: AR(1) ≈ +0.70
- Generation of series:
  - White: random standard normal
  - Blue/Red: generated via discrete-time autoregressive process and spectral mimicry
- Temperature characteristics:
  - Mean temperature for coloured treatments: 26°C (varying daily between approximately 21.0°C and 30.6°C, SD ≈ 1.5°C)
  - Constant treatment remains at 26°C

## Datasets and key variables

- Temperature-time-series_Noise.csv
  - Date, Day, Temperature
  - Treatment (CST, B1, B2, R1, R2, W1, W2)
  - Type of temperature fluctuations (none, blue, red, white)
  - Series (replicate)

- Plodia-life-history-data_Noise.csv
  - Treatment, Colour, Series, Individual, Code
  - Demographics (Starting date, Hatching date, Egg stage duration, Egg viability/status)
  - Adult traits (Adult emergence date, Juvenile stage duration, Date of death, Adult lifespan, Sex)
  - Reproductive data (Fecundity in intervals 0–3, 4–6, 7–10 days; Total eggs)
  - Morphometrics (Leg length, Leg measured, Leg photo date)
  - Parental pairing and observational metadata

- Venturia-life-history-data_Noise.csv
  - Treatment, Colour, Series, Individual, Code
  - Parasitism details (Pi stage and age, Parasitism half day, Pi mass, Time of parasitism, Observer)
  - Outcomes (Adult emergence dates for host/parasitoid; Juvenile stage duration)
  - Outcome classification (Pi, Vc, DD, NA), sex, dates of death
  - Leg photo data (leg length, leg photo date)

- Pop-count-data_Noise
  - Date, Day, Period (pre/post infection)
  - Treatment, Species, Temperature treatment, Colour, Series, Replicate
  - Population code, Week, Time point
  - Diet replacement counts (section/half section)
  - Counts: Number dead Pi, Number dead Vc, Number live Pi instars (L1-L3, L4-L5), Number live Pi pupae, Number live Vc pupae
  - Observers, infection status, comments

- Plodia-body-size-fecundity-data_Noise.csv
  - Day, Session, Week, Period
  - Treatment, Colour, Series, Population, Replicate
  - Species (Pi or Pi-Vc), Population infection status, Weekly infection status
  - Individual, Sex, Time in, Time out
  - Daily fecundity, Leg length, Leg measured (R/L), Observer, Comments

- Venturia-body-size-data_Noise.csv
  - Day, Session, Week, Period
  - Treatment, Colour, Series, Population
  - Replicate, Species (Pi-Vc), Population infection status, Weekly infection status
  - Individual, Leg length, Comments

- Plodia-common-garden_Noise.csv
  - Treatment, Population, Code, Colour, Species
  - Series, Week, Time point, Period
  - Population infection status, Weekly infection status
  - Starting date, Hatching date, Egg stage duration, Adult emergence date
  - Juvenile stage duration, Sex, Date leg photo taken, Leg measured, Leg length
  - Comments

- Temperature-time-series_Noise.csv (also listed under datasets)
  - Date, Day, Temperature
  - Treatment, Type of temperature fluctuations (none/blue/red/white)
  - Series

- Plodia-common-garden_Noise.csv
  - (described above in Plodia-common-garden_Noise.csv)

- Temperature-time-series_Noise.csv
  - (described above in Temperature-time-series_Noise.csv)

## Data collection, management and quality control

- Data collected from both life history and microcosm experiments, with weekly population and trait measurements.
- Replenishment of diet and controlled monitoring to minimize disturbance.
- Common garden experiments conducted to assess transgenerational effects.
- Quality control: All data checked for entry errors; outliers rechecked during initial analysis.

## Potential GIS-focused data products and applications

- Time-enabled visualization of population dynamics by microcosm layout:
  - Spatially map microcosm positions and overlay weekly counts of live hosts, parasitoids, and infection status.
  - Animations showing population trajectories across different temperature colour treatments (blue, red, white) versus constant.
- Environmental regime mapping:
  - Link microcosm data to temperature time series to create spatially-indexed layers of environmental regime (coloured fluctuation type) across the experimental layout.
- Trait geovisualization:
  - Map body size proxies (leg length) and fecundity metrics by microcosm, time point, and infection status to identify spatial-temporal patterns.
- Spatio-temporal dashboards:
  - Integrate weekly population counts, infection status, and treatment metadata for interactive exploration.
- Data fusion readiness:
  - Datasets are structured with common keys (Treatment, Colour, Series, Population/Microcosm IDs) enabling join operations to create unified geodatabases or time-enabled feature layers.

## References

- Begon, M., S. M. Sait, and D. J. Thompson. 1995. Persistence of a parasitoid-host system Refuges and generation cycles. Proceedings of the Royal Society B-Biological Sciences.
- Cohen, J. E. et al. 1999. Spectral mimicry: A method of synthesizing matching time series with different Fourier spectra. Circuits System and Signal Processing.
- Harvey, J. A. et al. 1994. Flexible larval growth allows use of a range of host sizes by a parasitoid wasp. Ecology.
- Knell, R. J. et al. 1996. Transmission dynamics of Bacillus thuringiensis infecting Plodia interpunctella. Proceedings of the Royal Society B-Biological Sciences.
- Mugabo, M. et al. 2019. Environmental degradation amplifies species' responses to temperature variation in a trophic interaction. Journal of Animal Ecology.
- rurs, D. 1972. Ichneumon wasp Venturia canescens - Oviposition and avoidance of superparasitism. Entomologia Experimentalis Et Applicata.
- Ruokolainen, L. et al. 2009. Ecological and evolutionary dynamics under coloured environmental variation. Trends in Ecology & Evolution.