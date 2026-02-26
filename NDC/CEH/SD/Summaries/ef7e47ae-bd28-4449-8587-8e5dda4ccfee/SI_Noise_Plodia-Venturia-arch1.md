# Brief description of the project, experimental design and data recorded

- System and aim
  - Experimental study of how coloured environmental variation affects life history traits and population dynamics in a host–parasitoid system: Plodia interpunctella (host) and Venturia canescens (parasitoid).
  - Focus on the temporal/spatial structure of temperature fluctuations (coloured noise): blue (rapid fluctuations), red (slow fluctuations), white (random), plus a constant 26°C control (CST).

- Experimental design overview
  - Two main experimental strands:
    - Life history experiment (single generation) to characterize individual responses.
    - Microcosm experiment (approximately 7 host generations) to characterize population and interaction dynamics.
  - Temperature treatments
    - Seven temperature time series: CST (constant 26°C) and six coloured series (B1, B2, R1, R2, W1, W2).
    - Each coloured series is generated to mimic blue, red, or white noise with specific temporal autocorrelation properties.
    - Time series length: 458 days; mean temperature around 26°C, with 24-hour daily fluctuations; coloured series have daily temperature variation with SD ≈ 1.5°C.
  - Replication and structure
    - For life history: unparasitized and parasitized host larvae per treatment (50 unparasitized, 26 parasitized per treatment).
    - For microcosms: 4 replicates of each microcosm type (host alone Pi and host–parasitoid Pi-Vc) per temperature time series, totaling 56 microcosms (4 × 2 × 7).
    - Microcosms started at 26°C constant, then shifted to assigned temperature treatment after initial development, with regular resource replacement.
  - Infection event and post-infection period
    - Bacillus thuringiensis (Bt) infection occurred around week 34, affecting multiple microcosms and leading to a defined post-infection period.
    - Data are flagged as pre-infection and post-infection; post-infection data for heavily infected populations are to be treated with caution, and some post-infection measurements are incomplete or biased due to infection dynamics.

- Data collection and variables
  - Life history data (Plodia-life-history-data_Noise.csv)
    - Individual-level data across seven temperature treatments (CST, B1, B2, R1, R2, W1, W2) and two series per coloured treatment.
    - Variables include development times (egg stage, juvenile stage), survival, adult lifespan, sex, fecundity metrics, body size proxies, mating pairings, leg measurements, and timing of observations.
  - Life history data for Venturia (Venturia-life-history-data_Noise.csv)
    - Parasitism-related metrics for hosts/parasitism events, parasitoid emergence, durations, outcomes, sex, leg measurements, and timing.
  - Population counts (Pop-count-data_Noise.csv)
    - Weekly population counts for host and parasitoid across microcosm type (Pi, Pi-Vc), temperature treatment, colour, series, and week, including infection status and pre/post infection periods.
  - Body size and fecundity data (Plodia-body-size-fecundity-data_Noise.csv; Venturia-body-size-data_Noise.csv)
    - Sampling sessions with individual-level fecundity and body-size measurements (leg length) for hosts and parasitoids, including infection status and population identifiers.
  - Common garden and developmental data (Plodia-common-garden_Noise.csv)
    - Post-experiment measurements to assess potential transgenerational effects, including egg-stage duration, juvenile duration, adult body size, and leg measurements.
  - Temperature series metadata (Temperature-time-series_Noise.csv; Temperature-time-series_Noise.csv)
    - Daily temperature values, series identifiers, and classification of fluctuation type (none, blue, red, white).

- Key data quality and access notes
  - Quality control: data were checked for entry errors; outliers were rechecked during initial analysis.
  - Datasets include extensive metadata and descriptions of variable meanings, units, and coding to support reproducibility and reuse.

- Usage and potential analyses
  - The dataset suite enables analysis of how the frequency/content of environmental fluctuations (blue vs red vs white) influences life history traits, fecundity, body size, survival, and population interactions in a host–parasitoid system.
  - Suitable for correlational studies and predictive modeling (e.g., population dynamics under different fluctuation regimes, transgenerational effects, and interaction strength).
  - Provides detailed time-series data across multiple scales (individual, cohort, population) and controlled perturbations (Bt infection) to examine resilience and response to disturbance.

- References
  - Includes foundational methods for coloured environmental variation, spectral mimicry, parasitoid–host dynamics, and Bt infection dynamics (Begon et al. 1995; Cohen et al. 1999; Harvey et al. 1994; Knell et al. 1996; Mugabo et al. 2019; rurs 1972; Ruokolainen et al. 2009).