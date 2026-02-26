# Perch weekly mean sizes from Green Tuft 19462012

## Overview
- Dataset of weekly mean sizes of mature perch (Perca fluviatilis) from Green Tuft, Windermere, Cumbria, UK, spanning 1946–2012.
- Collected from Green Tuft in Windermere’s north basin; data originally gathered by the Freshwater Biological Association (FBA) and since 1989 by the Centre for Ecology & Hydrology (CEH) and its predecessor.
- Related to ecological studies on phenology and population responses (e.g., Ohlberger et al. 2014).

## Data content and format
- File: PerchWeeklyMeanSizesGreenTuft1946_2012.csv; CSV format, ~10 KB.
- Columns: Year (year of catch), Week (week of year), Mean_size (cm; mean size of mature perch caught), QA_code (NS = week not sampled; ID = week with insufficient data).
- Location: Green Tuft, Windermere, north basin; OS grid reference provided.
- Related datasets available: Perch weekly catches (Green Tuft 1946-2012) and Windermere monthly temperatures (both via CEH NERC Data Centre).

## Sampling design and collection methods
- Site and effort varied over time (1943–present).
- Trapping method: unbaited wire-netting traps (approx. 0.74 m x 0.59 m x 0.64 m; 12 mm mesh) deployed for six sets per spawning season.
- Deployment: 2–7 m depth, daylight; each set typically lifted after about 7 days.
- Processing: all perch counted, measured (total length to 1 mm), weighed (wet mass to 1 g), and sex/reproductive state determined; mean size of mature perch computed weekly.

## Analytical methods and quality control
- In the laboratory, full catches processed; sub-sampling may occur if numbers are large, stratified by length class.
- Measurements validated via permutations of three individuals as part of quality control.

## Data provenance and references
- Primary authors: Winfield, I. J., Fletcher, J. M. & James, J. B. (2014).
- Trapping methodology reference: Paxton et al. (2004) on recruitment influences in Windermere.
- Connection to broader studies: used in Ohlberger et al. (2014) on phenology and trophic mismatch.

## Practical considerations for analysts
- Suitable for time-series analyses of growth, seasonal size structure, and population dynamics at a local scale.
- Data gaps: NS indicates weeks not sampled; ID indicates weeks with insufficient data; account for these in analyses.
- Site-specific data may limit broader generalizations but can inform local management or comparative studies with environmental covariates (e.g., Windermere temperature data).
- Ensure provenance and methodology are considered when linking to other datasets or performing meta-analyses.