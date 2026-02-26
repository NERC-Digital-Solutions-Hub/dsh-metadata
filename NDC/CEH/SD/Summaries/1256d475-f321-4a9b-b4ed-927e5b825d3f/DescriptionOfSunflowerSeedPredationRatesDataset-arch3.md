# Sunflower seed predation rates in Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) plots, Sumatra, Indonesia

## Overview
- Study location: three oil palm estates in Riau Province, Sumatra, Indonesia (Ujung Tanjung, Kandista, Libo) owned by Pt Ivo Mas Tunggal.
- Project context: BEFTA (Biodiversity and Ecosystem Function in Tropical Agriculture); part of vegetation management research ( Foster et al., 2014 ).
- Timeframe and scope: 18 plots established in 2013; measurements in 2014 (one time in mature stands) and 2016–2017 (five time points in both mature and replanted stands).
- Primary measure: granivory assessed via sunflower seed predation as an environmental health indicator.

## Experimental design and sampling regime
- Plot framework: each plot 50 x 50 m with 50 m between edges and tracks on three sides; approximately 1000 m from the fourth track.
- Sampling positions: three positions per plot at 45°, 165°, and 285° from plot center.
- Seed predation assay: ten shelled sunflower seeds placed on a ~15 cm paper disc, exposed ~10 cm above soil, protected from rain with a polystyrene plate and kebab sticks.
- Treatments (for each replicate): four conditions
  - cage + grease
  - cage only
  - grease only
  - open (no cage, no grease)
- Exposure duration: approximately 24 hours per trial.
- Special considerations: exclosure-related ant poison (2016–2017) with distance recording (SAFE_distance) for plots where the seed interception point was within 20 m of the focal palm center.

## Data collected and units
- Response variable: seeds remaining out of ten (decimals allowed due to partial seeds).
- Additional fields: date and time of seed placement and collection, rainfall (dayrain) for the 24-hour period, treatment type, plot identifiers, and sampling position.
- Metadata notes: field observations and any changes recorded in allnotes.

## Data quality control
- Basic data checks for impossible values (e.g., more than 10 seeds remaining).
- Data integrity: 50% of entries cross-checked against original field sheets; error rate < 1%; any corrections logged with provenance.

## Data format and storage
- Three separate CSV files:
  - SunflowerSeedPredationRates_2014.csv (mature stands)
  - SunflowerSeedPredationRates_2016_2017.csv (mature stands)
  - SunflowerSeedPredationRates_replants.csv (replanted stands)
- Format: thin, with one observation per line.
- Key columns (examples):
  - Estate_abbrev, Triplet, Plot_no (e.g., C01), Treatment (reduced, normal, enhanced), Period, Position
  - Date_set, Time_set, Date_coll, Time_coll
  - seedstreat (remain_cage, remain_open, remain_cage_grease, remain_open_grease)
  - seedsremaining (numeric, out of ten)
  - dayrain (rainfall over the 24-hour period)
  - allnotes (field observations and data-entry changes)
  - SAFE_distance (present only in 2016-2017 replanted dataset; indicates exclosure proximity)

## Dataset contents and file descriptions
- BEFTA core plots (2016–2017): data from mature plots across three estates; includes multiple sampling periods and treatments.
- Replanted plots: data from replanted stands with SAFE_distance and exclosure-related context.
- Miscellaneous: coordinates and locational details (not all fields are in the CSVs; coordinates mentioned as part of the project metadata).

## Miscellaneous and provenance
- Funding: NE/P00458X/1.
- Data provenance: two data files cover core BEFTA plots (2016–2017) and replanted plots.
- Location details and coordinates referenced in project metadata (section 'Miscellaneous').

## Relevance for environmental monitoring and policy decisions
- Provides a tangible, replicate-based metric of ecosystem function (granivory) linked to vegetation management and stand maturity (mature vs replanted).
- Supports assessment of management effects on biotic interactions and food-web processes in oil palm landscapes.
- Includes robust metadata, quality control, and data governance practices that aid transparency, reproducibility, and data sharing in monitoring frameworks.
- Highlights practical monitoring considerations: spatial arrangement, temporal sampling, treatment effects, data transformation needs, and data governance (sharing, metadata completeness, and exclosure considerations).