# Palm Frond Decomposition Rates in Oil Palm Plantations in Riau Province, Sumatra, Indonesia

## Aim
- To measure oil palm frond litter decomposition under varying invertebrate access (mesh bag types) across mature and replanted estates, and to assess how management treatments and ENSO-related drought influence decomposition over time.
- To support analyses of correlations, trends, and predictive insights for practical decisions in tropical plantation ecosystems.

## Study setting and experimental design
- Location: three estates in Riau Province, Sumatra, Indonesia, owned by Pt Ivo Mas Tunggal (Ujung Tanjung, Kandista, Libo).
- Estate history: Ujung Tanjung and Kandista are mature/over-mature; Libo replanted in 2014.
- Plots: 18 plots (50 x 50 m), with three sampling positions on the plot edge at 45°, 165°, and 285° from north.
- Grid: Each palm labeled; decomposition measured using litter bags placed on the soil surface under the litter layer.
- Sampling regime: six decomposition events from 2013 to 2017 (with a reduced protocol in May 2016 during ENSO drought).

## Litter bag protocol and treatments
- Litter: four grams of dried Elaeis guineensis frond litter per bag.
- Bag types to vary invertebrate access:
  - 0.1 mm mesh: excludes all invertebrates visible to the naked eye.
  - 2 mm mesh: excludes large invertebrates (e.g., cockroaches).
  - 0.1 mm mesh with four 1 cm holes: allows large invertebrates.
- Deployment: four bags of each type per plot (12 bags total) placed together on the soil surface under the litter layer.
- Sampling times: bags dug up at 10, 30, 60, and 90 days; one bag of each type removed at each time point.
- Replication: three temporal replicates per plot (one at each sampling position).
- Reduced protocol (May 2016): one fine-mesh bag per plot corner left for 30 days (randomly chosen corners).

## Variables and measurements
- Response: grams of dried frond litter remaining in each bag at collection.
- Auxiliary data collected per observation:
  - Estate_abbrev, Plot_no, Triplet (plot sets of three), Treatment (reduced, normal, enhanced), Period (sampling period), Position (edge direction), Date_set/Time_set, Date_coll/Time_coll
  - Bag type, Grammes_remaining, dayrain (rainfall in last 24 hours at nearest station), allnotes (observations and data entry notes)
  - SAFE_distance (BEFTA core plots: distance to focal palm within exclosures where ant poison was applied; data caution for use)
- Metadata and data provenance: dataset includes notes on field changes during checks; 50% data-entry verification against field sheets with <1% error rate.

## Data structure and storage
- Datasets (three CSV files, stored in thin format with one observation per line):
  - PalmFrondDecompositionRates_2013_2015.csv (mature stands, pre-ENSO period)
  - PalmFrondDecompositionRates_2016_2017.csv (mature stands, during ENSO period)
  - PalmFrondDecompositionRates_replants.csv (replanted stands)
- Data origin and funding:
  - BEFTA-related core plots funded under NE/P00458X/1 (core plots 2013–2014 and 2016–2017)
  - Replanted-stands data funded by NERC (2016–2017)  
- Data format notes:
  - “Thin format”: each line is a single observation
  - Columns include estate abbreviations, plot identifiers, treatment, period, position, sampling and collection timestamps, bag type, grams remaining, daily rainfall, notes, and safety/exclosure related fields

## Data quality and notes
- Quality control: basic checks for impossible values; 50% of 2016–2017 data entry cross-checked with field sheets; error rate <1%; all changes recorded with the dataset.
- Data notes:
  - The SAFE_distance field pertains to BEFTA exclosure sites (should be used with caution for BEFTA-related analyses).
  - The May 2016 reduced protocol provides a supplemental dataset for shorter-term decomposition under a simplified setup.

## Plots and data scope
- Mature stands: data reflect decomposition across plots in UTNE and KNDE with various Triplets and Plot identifiers (examples include plots coded C01–F06, G07–G16, etc.).
- Replanted stands: data reflect Libo (LIBE) plots with coordinates and plot identifiers (e.g., C18, D19, E22, E23, etc.).
- Spatial and temporal coverage:
  - 2013–2015: before/early ENSO period for mature plots
  - 2016–2017: during ENSO period for mature plots, plus replanted data
  - Three sampling positions per plot and four sampling times across each period, with multiple bag types to parse the effect of invertebrate access

## Potential uses and considerations for analysts (data-driven focus)
- Analyze decomposition rate as a function of:
  - Bag type (invertebrate access)
  - Plot treatment (reduced, normal, enhanced management)
  - Time since deployment (10, 30, 60, 90 days; and 30 days for the reduced protocol)
  - Rainfall (dayrain) and environmental context (ENSO period)
  - Estate type (mature vs replanted)
- Develop predictive models of litter decomposition incorporating:
  - Invertebrate access and disturbance regimes
  - Spatial factors (plot position, BEFTA exclosure proximity where applicable)
  - Temporal dynamics across pre-ENSO and ENSO periods
- Data integration potential:
  - Merge across the 2013–2015 and 2016–2017 mature datasets for longitudinal analyses
  - Combine mature and replanted datasets to compare decomposition dynamics across stand history
- Cautions:
  - Use SAFE_distance data only within BEFTA-related contexts
  - Be mindful of potential missing data or entry notes when aligning periods and treatments
  - Consider potential confounding effects of ENSO drought in 2016 when interpreting decomposition rates

## Summary of what is included
- Detailed experimental design, bag-type treatments, sampling framework, and replication
- Clear data definitions, time points, and measurement units
- Three accessible CSV data files covering mature and replanted stands across distinct periods
- Metadata and quality-control documentation to support reproducible analysis