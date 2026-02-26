# Termite abundance and ecosystem processes in Maliau Basin, 2015-2016 L. A. Ashton , H. M. Griffiths, C. L. Parr, T. A. Evans and P. Eggleton

## Aim and scope
- Investigates the role of termites in ecosystem processes and their potential to mitigate drought effects in a tropical rainforest.
- Combines termite abundance data with multiple ecosystem measurements (leaf litter, soil moisture and nutrients, decomposition, invertebrates, seedling survival) across drought and non-drought periods.
- Conducted on eight 50 x 50 m plots (four termite-suppressed, four controls) within a 42-ha area in Maliau Basin, Sabah, Malaysia, from Oct 2014 to July 2017.

## Data assets (12 CSV files)
- termite_hits_on_T_and_C_plots.csv: termite hit rate data by plot, date, treatment, and termite genus.
- Leaf_litter_depth.csv: leaf litter depth measurements by plot, time, and line.
- Leaf_litter_invertebrates.csv: abundance data for leaf litter invertebrates by plot, treatment, transect position, and taxonomic groups.
- Litter_mass_loss.csv: decomposition measurements from leaf litter bags (open vs. closed; plot and bag treatments).
- Non_target_invertebrates_all_years.csv: counts of non-termite invertebrates by year, plot treatment, and order.
- Seedling_survival_nondrought.csv: seedling survival data during non-drought periods.
- Seedling_survival_drought.csv: seedling survival data during drought period.
- Soil_moisture.csv: soil moisture measurements across plots and sampling dates.
- Soil_nutrients.csv: plant-available soil nutrients measured with PRS probes across drought and non-drought periods.
- Termite_cumulative_attack.csv: cumulative termite attack (using untreated toilet paper rolls) per plot and month.
- Termite_hits_on_C_plots_SPI.csv: termite hits on control plots linked to rainfall and SPI (Standardised Precipitation Index).
- Locations_of_plots.csv: GPS coordinates and elevations for plot corners; notes parallel ant-suppression data.

## Experimental design and sampling regime
- Location: lowland, old-growth dipterocarp rainforest in the Maliau Basin Conservation Area.
- Plots: eight plots (50 x 50 m each); four termite suppression, four controls; at least 100 m between plots; core 50 x 50 m sampled to avoid edge effects.
- Termite suppression: mounds removed; soil treated with imidacloprid; TPRs and TBs (fipronil) deployed across suppression plots; integrated pest management with buffers and repeated applications (six-month intervals) until 2017.
- Sampling timeline: termite and ecosystem measurements conducted in June 2015 and October 2016; drought period defined within 2015–2016.
- Additional data streams: rainfall data from Danum Valley used to derive SPI and relate rainfall to termite activity.

## Data collection methods and instrumentation
- Termite abundance: Jones and Eggleton transect method.
- Leaf litter depth: in situ measurements along transects within plots, during drought and non-drought periods.
- Leaf litter invertebrates: 1 m2 samples, Winkler extraction for three days, identified to order.
- Decomposition: litter bags with macroinvertebrate exclusion vs open bags; lignin-rich Shorea johorensis litter; bags deployed Aug 2015 (drought) and July 2016 (non-drought); 112-day exposure.
- Non-target invertebrates: leaf litter samples across 2014–2016, Winkler extraction.
- Seedling survival: transplant experiment with Agelaea borneensis; 200 individuals; monitored across 2015–2017 under drought and non-drought conditions.
- Soil moisture: Delta-T HH2 meter; 25 sampling points per plot.
- Soil nutrients: PRS resin probes; two phases (drought and non-drought); 10 cm depth; analysis by third-party lab.
- Termite attack: untreated toilet paper rolls scored 0–5 for damage, monthly monitoring and replacement.
- Rainfall and SPI: rainfall data from Danum Valley; 3-month SPI computed to reflect drought intensity.
- Plot locations: geographic coordinates captured for each plot corner.

## Data structure and key variables
- Data are organized into 12 CSV files with consistent plot-level and temporal metadata.
- Common fields include: Plot code (e.g., CC, GC, KC, DC), Treatment (Termite suppression vs. Control), date/month, and treatment-specific measurements (e.g., hits, depth, abundance, mass loss, alive/dead status, soil metrics, nutrient concentrations, SPI).
- Termite data include multiple genera and an overall hits count plus SPI context; leaf litter and soil datasets include depth, nutrient measures, and decomposition indicators; seedling datasets track survival across years; location file provides precise GPS coordinates and elevations.

## Data governance, sharing and usability
- Detailed metadata and explicit column definitions accompany each dataset, aiding reuse and cross-study comparisons.
- Data are provided as CSVs with standardized formats to facilitate integration into monitoring dashboards, analyses, or policy-relevant reporting.
- The collection includes spatial coordinates and time-stamped measurements, enabling spatial-temporal monitoring and trend analysis.
- The study illustrates transparent data collection, provenance, and the potential need for careful data governance when sharing multi-year ecological monitoring data.

## Relevance to monitoring framework aims and challenges
- Aligns with monitoring framework authorship goals by producing a comprehensive, multi-dimensional data package to scrutinise ecological policy implications and guide future decisions.
- Brings together data across taxa (termites, invertebrates, seedlings) and ecosystem processes (decomposition, litter dynamics, soil nutrients) under drought and non-drought conditions.
- Demonstrates practical approaches to data assembly, verification, and dissemination, including metadata sufficiency, data sharing considerations, and data quality controls.
- Highlights typical challenges: ensuring metadata completeness, harmonizing measurements across years, handling data gaps or transformations, communicating complex, multi-variable results, and maintaining data governance for open sharing.