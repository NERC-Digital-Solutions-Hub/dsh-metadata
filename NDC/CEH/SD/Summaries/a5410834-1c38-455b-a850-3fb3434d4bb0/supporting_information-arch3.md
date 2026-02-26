Supporting document for
'Nitrous oxide emissions and associated microbial diversity, soil biochemical properties and crop growth and yield from a field trial of winter barley with the addition of microplastics, Abergwyngregyn, UK, 2020-2021'

## Purpose and relevance to monitoring frameworks
- Evaluates how conventional versus biodegradable microplastics affect N2O emissions, soil chemistry, microbial diversity, and crop performance.
- Demonstrates end-to-end data capture, processing, and dissemination suitable for informing policy monitoring and future decision-making.
- Highlights data governance, metadata, and openness considerations critical for monitoring frameworks.

## Experimental design and measured variables
- Location and design: field trial at Henfaes Research Centre, Abergwyngregyn, North Wales; randomized block design with three treatments (conventional microplastic, biodegradable microplastic, control) and four replicates (n=4).
- Measurements in-field: N2O flux, soil moisture, rainfall, air temperature.
- Laboratory analyses: soil pH, electrical conductivity (EC), ammonium (NH4+), nitrate (NO3-), microbial community composition, and crop yield.
- Crop data: barley growth metrics and final yield.
- Microplastics: conventional PE and PHBV biodegradable microplastics, 100 kg/ha, applied to top 0–10 cm of soil.

## Data collection, processing, and analysis workflow
- Nitrous oxide data: collected with a mobile gas chromatograph; processed to obtain flux values, then integrated to cumulative N2O flux via trapezoidal integration; exported for deposition.
- Soil and climate data: collected via field sensors and weather station; stored as CSVs after standard processing.
- Nutrients: ammonium and nitrate quantified with microplate method and standard calibration curves; results stored as mg/kg (or equivalent per hectare metrics).
- Microbial data: 16S rRNA sequencing (Illumina MiSeq); reads processed with Python and QIIME v1.3.1 to produce ASV count tables and taxonomic assignments.
- Data provenance: clear linkage from raw measurements to processed outputs and final datasets.

## Data resources and file structure
The data resource comprises 10 CSV files:
- crop_harvest.csv: two 50 cm x 10 cm middle-of-plot harvests; agronomic harvest metrics.
- crop_yield.csv: per-plot stem count, grain per ear, ear weight, straw weight, grain weight.
- n2o_cumulative.csv: date, time, chamber, treatment, cumulative N2O flux (mg N2O-N m^-2).
- n2o_flux.csv: date, time, chamber, treatment, flux_best (μg N2O-N m^-2 h^-1).
- soil_n.csv: nitrate and ammonium contents by date, plot, treatment.
- soilph_ec.csv: soil pH and EC with date/time and plot-level context.
- weather.csv: date, time, air temperature, rainfall.
- wfps.csv: date, time, treatment, plot, water-filled pore space (%).
- asv_count_table.csv: counts of Amplicon Sequence Variants by treatment/replicate.
- taxa_table.csv: taxonomic assignments (domain to species) for ASVs with SILVA v138 references.
- Notes: some fields include blanks due to early-stage measurements or data gaps; extensive metadata describes units and methods.

## Sampling regime and field notes
- Sampling frequency varied by variable (e.g., 30-minute intervals for soil moisture, EC, pH; 30-minute to weekly for others; reductions in 28/05/2021 for some measurements due to field conditions).
- Important dates outline sequence of treatments, sowing, fertilizer applications, greenhouse gas chamber setup, bird-related disturbances, and harvest; field damage resulted in partial data loss and adjustments in sampling cadence.

## Data governance, metadata, and openness
- Data prepared for public sharing; some outputs explicitly described as deposit-ready (e.g., N2O flux, cumulative flux).
- Documentation includes measurement methods, instruments, and calibration details; data types and units clearly specified.
- Data formats (CSV) and processing steps (GC measurements, Flux.NET, QIIME, Gen5) facilitate reproducibility and potential integration with monitoring systems.

## Implications for monitoring frameworks
- Key measures for policy monitoring: cumulative N2O flux (and peak flux), soil nutrient pools (NH4+, NO3-), soil properties (pH, EC), soil moisture/water balance (wfps), microbial community structure, and crop yield metrics.
- Highlights the importance of:
  - Standardized data schemas across studies for comparability.
  - Detailed metadata on methods, instruments, and processing to enable data reuse.
  - Data sharing and governance to support transparency and policy evaluation.
  - Handling of data gaps and field contingencies (e.g., wildlife disturbances, changing sampling schedules) in monitoring plans.
- Demonstrates end-to-end data lifecycle from field measurements to published datasets, suitable for informing environmental health monitoring and decision-making.

## References
- Marsden, K.A., Holmberg, J.A., Jones, D.L., Chadwick, D.R., 2018. Sheep urine patch N2O emissions are lower from extensively-managed than intensively-managed grasslands. Agric. Ecosyst. Environ. 265, 264-274.
- Miranda, K.M., Espey, M.G., Wink, D.A., 2001. A Rapid, Simple Spectrophotometric Method for Simultaneous Detection of Nitrate and Nitrite. Nitric Oxide 5, 62-71.
- Mulvaney, R.L., 1996. Nitrogen-Inorganic Forms, in: Methods of Soil Analysis. John Wiley & Sons, Ltd.