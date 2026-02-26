# Brief description of the project, experimental design and data recorded

- Purpose and scope
  - Experimentally investigated how coloured environmental variation (temporal structure) in temperature affects life history variation and population dynamics in a host–parasitoid system consisting of Plodia interpunctella (host) and Venturia canescens (parasitoid).
  - Comparisons across constant, blue, red, and white temperature fluctuations to assess how fluctuation frequency and autocorrelation influence outcomes.

- Experimental design
  - Two interconnected experimental components:
    - Life history experiment: single generation for unparasitized and parasitized hosts to record individual life-history traits.
    - Microcosm experiment: multi-generation (~7 host generations) with host-alone and host–parasitoid microcosms to monitor population dynamics and trait variation under different temperature time series.
  - Temperature treatments
    - Seven time series: constant 26°C (CST) plus blue (B1, B2), red (R1, R2), and white (W1, W2) noise treatments.
    - Each coloured treatment uses two replicates of time series; CST serves as control.
  - Replicates and organisms
    - Life-history: 50 unparasitized and 26 parasitized host larvae per temperature treatment.
    - Microcosms: four replicates for each combination of microcosm type (Pi = host alone; Pi-Vc = host–parasitoid) and temperature time series, totaling 56 microcosms (4 × 2 × 7).
  - Pathogen event
    - Bacillus thuringiensis (Bt) infection occurred around week 34, affecting some microcosms and leading to data limitations post-infection.

- Temperature time series details
  - Time series length: 458 days with mean temperature around 26°C.
  - Autocorrelation: white = 0.00, blue = -0.70, red = 0.70.
  - Generation of series: white by standard normal draws; red/blue generated via discrete AR processes and spectral mimicry to match desired spectra.

- Data collection and variables
  - Life history data (Plodia life-history dataset)
    - Individual-level measures: egg stage duration, hatch viability, adult emergence, juvenile duration, lifespan, sex, fecundity across time windows, body size proxies, dating for leg measurements, mating pairings, and observational notes.
  - Life history data for Venturia (Venturia life-history dataset)
    - Parasitism events: sex, age, mass, time of parasitism, outcome (host or parasitoid emergence, or both die), duration to emergence, leg measurements, and observational notes.
  - Population counts (Pop-count-data)
    - Weekly live counts of hosts and parasitoids, instar counts (L1-L3, L4-L5), pupae, diet replacement details, infection status (pre/post Bt), and infection timing.
  - Body size and fecundity (Plodia and Venturia body-size datasets)
    - Daily fecundity, leg length as body-size proxy, repeated sampling sessions, infection status, observer, and contextual notes.
  - Common garden (Plodia-common-garden)
    - Post-experiment measurements including juvenile and adult traits, leg measurements, infection status context, and population identifiers.
  - Temperature series (Temperature-time-series_Noise)
    - Date, day, temperature, treatment, and fluctuation type for each series.

- Data structure and metadata
  - Datasets are stored as multiple CSV files with detailed variable dictionaries (examples include Plodia-life-history-data_Noise.csv, Venturia-life-history-data_Noise.csv, Pop-count-data_Noise, Plodia-body-size-fecundity-data_Noise.csv, Venturia-body-size-data_Noise.csv, Plodia-common-garden_Noise.csv, Temperature-time-series_Noise.csv).
  - Key field categories include Treatment, Colour, Series, Population/Individual, timepoints (week, date), developmental stages, sex, fecundity, body size (leg length), infection status (pre/post Bt), and observational metadata (observer, comments).
  - Quality control note: data were checked for entry errors; outliers rechecked during initial analysis.

- Notable limitations and cautions
  - Bt-induced infection caused partial data loss, especially after week 34; post-infection data should be treated with caution.
  - Certain datasets advise using data only up to week 39 or excluding post-infection data for analyses of population counts and host fecundity/body size in infected populations.
  - Some post-infection measurements (e.g., parasitoid data at week 41 in certain red treatments) should be used carefully due to reduced sample sizes.

- Data governance and sharing considerations
  - The study emphasizes data provenance, metadata completeness, and sharing of underlying data; potential barriers include data availability, data silos, and the need to ensure data are up to date and well-governed with clear provenance.
  - Data management practices align with established references on ecological data sharing, metadata standards, and data quality.

- References and methodological underpinnings
  - Methodological and analytical references include: spectral mimicry for time-series generation, colour variation in ecological studies, parasitoid–host growth flexibility, Bt infection dynamics in Plodia, environmental degradation amplification of responses, and foundational work on oviposition and superparasitism.

- Overall takeaway for monitoring framework practitioners
  - Demonstrates a comprehensive, multi-layered data collection approach linking individual life-history traits to population-level dynamics under controlled, ecologically relevant environmental variation.
  - Provides richly described datasets with explicit metadata, designed to support analyses of how different temporal structures of environmental fluctuations shape life-history trade-offs, competition, parasitism, and trophic interactions.
  - Highlights practical governance considerations for monitoring projects, including data availability, metadata completeness, data quality checks, and transparent handling of events (e.g., infection episodes) that affect long-term datasets.