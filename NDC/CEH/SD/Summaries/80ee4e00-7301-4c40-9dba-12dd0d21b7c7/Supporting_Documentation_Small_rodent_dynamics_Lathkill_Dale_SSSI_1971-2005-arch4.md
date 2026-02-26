# Dataset: Small rodent dynamics at Lathkill Dale SSSI, Derbys, 1971-2005

- Purpose and scope
  - Long-term dataset describing 35 years of 6-monthly population sampling for bank voles (Myodes glareolus) and wood mice (Apodemus sylvaticus) in a Derbyshire ash woodland.
  - Includes annual and seasonal ash fruit-fall data and a measure of winter severity; plus a 4-year experiment with supplementary ash fruit in two winters.
  - Aims to explain between-year variations in reproductive and population growth rates using a state-space model; fruit-fall supplementation aids interpretation.

- Study area and sampling design
  - Location: Lathkill Dale, Derbyshire, England; ash Fraxinus excelsior woodland (0.45 ha grid), with 90 Longworth traps across 30 points.
  - Time frame: 1971–2005 for main study; 1981–1985 for an experimental/alternative area comparison (control vs experimental grid ~150 m apart).
  - Sampling regime: population data collected during two 24-hour trapping periods per year (December–November cycle), roughly every six months; juvenile and adult counts recorded for May/June and November/December.
  - Data collection specifics: density indices derived from captured individuals using Zippin estimates; fruit-fall measured as dry weight of edible ash seeds per m2; winter severity index from mean minimum daily temperature (December–March).

- Key variables and data structure
  - For Apodemus sylvaticus (wood mouse) and Myodes glareolus (bank vole):
    - Year of June population data collections
    - Winter severity: mean minimum daily temperature (Dec–Mar, °C)
    - Annual ash fruitfall: Sep–Dec, Jan–Mar, and Sep–Mar (g m-2 dry weight edible seeds)
    - Collection dates and trapping counts for Nov/Dec and May/June
    - Population estimates: adult and juvenile numbers (two daily counts per period) and density indices (Zippin estimates)
  - Data files cover control and experimental areas with similar schema, enabling comparative analyses of natural vs. augmented fruit-fall dynamics.

- Experimental manipulation
  - In 1981–82 and 1984–85 winters, 60 kg of heat-sterilized ash fruit were distributed in the experimental grid (0.45 ha) to simulate strong fruit-fall years.
  - Resultant population dynamics in the experimental area were tracked and compared to the main study area to isolate fruit-fall effects.

- Modelling and findings
  - Modelling approach: state-space model applied to live-trapping data to parse influences on reproductive and population growth, incorporating density dependence and climate variables.
  - Primary drivers:
    - September–March fruit-fall strongly drives bank vole spring reproductive rates and population growth (and can influence subsequent years).
    - September–December fruit-fall has a weaker influence on wood mouse spring reproduction; December–March fruit-fall also exerts some influence on wood mouse summer growth.
    - Winter severity affects bank vole winter growth and wood mouse spring reproductive rate; neither species shows winter breeding.
  - Demography and dynamics:
    - Density dependence significantly affects winter and summer growth for both species.
    - Fruit-fall effects on bank vole demography are often delayed, lasting a year or longer.
    - Experimental fruit additions confirmed the causal role of autumn–early winter fruit-fall on bank vole winter growth.
    - Inter-species differences noted; bank voles show independent food and weather influences, with delayed, lasting impacts, while the broader pattern aligns with general rodent masting responses.
  - General insights:
    - Long-term data reveal robust links between masting (fruit-fall), climate, and small mammal demography.
    - Dense coupling between environmental variability and population dynamics is modulated by density dependence and delayed responses.

- Data access and documentation
  - Primary dataset described via multiple CSV files:
    - FlowerdewApodemusData041212csv.csv (wood mouse and environment, 1971–2005)
    - FlowerdewApodemusExData040613Controlcsv.csv (wood mouse control area, 1981–1985)
    - FlowerdewApodemusExData040613Experimentalcsv.csv (wood mouse experimental area, 1981–1985)
    - FlowerdewMyodesData291112csv.csv (bank vole and environment, 1971–2005)
    - FlowerdewMyodesExData040613Controlcsv.csv (bank vole control area, 1981–1985)
    - FlowerdewMyodesExData040613Experimentalcsv.csv (bank vole experimental area, 1981–1985)
  - Data columns include yearly and seasonal counts, dates of collections, and environmental covariates with explicit units (e.g., g m-2 of ash seed, °C).
  - Temperature and fruit-fall data are partitioned into relevant seasonal sub-totals for robust analysis.

- Relevance for data leadership and reuse
  - Demonstrates long-term, multi-factor ecological data collection with clear metadata and structured files suitable for time-series and state-space analyses.
  - Provides a case study of linking environmental variability (masting, climate) to animal demography, including experimental manipulation to establish causality.
  - Highlights data governance aspects relevant to Data Leaders:
    - Clear documentation of variables, measurement methods, and timing to support future discovery and reuse.
    - The necessity of curated, accessible metadata for long-running datasets spanning multiple collection regimes and experimental conditions.
    - Potential to integrate with broader data networks for cross-site comparisons, replication studies, or meta-analyses on the effects of mast seeding and climate on small mammal populations.