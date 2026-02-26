# LAC water chemistry_dataset.csv

## Dataset overview
- Water chemistry data collected from lakes across multiple regions (Norway, Greenland, Russia during ice cover; Alaska during ice-free periods).
- One sample per lake, collected from the upper 1 m of the water column at the deepest point.
- Dataset compiled by Erika Whiteford, Loughborough University.

## Experimental design and sampling
- Sampling regime targeted shallow to mid-depth water chemistry during distinct seasonal states (ice-covered vs ice-free).
- Lakes selected across diverse Arctic-aligned regions; single sampling event per lake.

## Collection, generation, and transformation methods
- Water chemistry analysed colourimetrically by developing a color from known standards; raw absorbance recorded at specified wavelengths.
- Standard curves used to calculate concentrations; standard curve and raw absorbance logged in lab notebooks and transferred to CSV.
- Field procedures included filtering for most analytes and preserving samples for specific analyses; some samples collected unfiltered for TP, TN, and total alkalinity.

## Abbreviations and terminology
- TP: Total Phosphorus
- SRP: Soluble Reactive Phosphorus
- TN: Total Nitrogen
- NO3-: Nitrate
- NH4+: Ammonium
- Chl a: Chlorophyll a
- SiO2: Silicate
- Na+: Sodium
- Mg2+: Magnesium
- K+: Potassium
- Ca2+: Calcium
- SO4 2-: Sulphate
- Cl-: Chloride
- DOC: Dissolved Organic Carbon

## Analytical methods and sample handling
- Analytes (DOC, SRP, SiO2, NO3-, NH4+, Na+, K+, Mg2+, Ca2+, Cl-, SO4 2-) filtered in the field using pre-combusted 0.7 µm GF/F; TP, TN, and total alkalinity analyzed from unfiltered water.
- Samples kept cold and dark in the field; returned to the lab typically within 8 hours; stored at 4°C in the dark until analysis.
- DOC measured by Pt-catalysed combustion after removing inorganic carbon; Chl a measured via spectrophotometry; algal pigments measured by high-performance liquid chromatography (HPLC).
- Chlorophyll a extraction and measurement followed established protocols (Jeffrey & Humphrey, 1975).

## Calibration, quality control, and data validation
- Machine drift checks performed; standard curves checked for linearity and fit to absorbance data.
- Where absorbance fell below detection, adjustments and checks performed; quadratic calculations verified for errors.
- Water chemistry values cross-validated against previous samples from the same locations.

## Data format and structure
- File format: CSV
- Core fields include: Region, Lake code, Date of collection, TP, SRP, TN, NO3-N, NH4-N, SiO2, Sodium, Potassium, Magnesium, Calcium, Chloride, Sulphate, Total Alkalinity, Chlorophyll a, DOC.
- Missing/below detection values indicated as BDL (below detectable level).

## Data units and value types
- TP, SRP, TN, NO3-, NH4+, Chlorophyll a: µg/L
- SiO2, Sodium, Potassium, Magnesium, Calcium, Chloride, Sulphate: mg/L
- DOC: ppm
- Total Alkalinity: meq/L
- Date format: DD/MM/YY
- Region and Lake code provide geographic and identifying metadata

## Data governance, discoverability, and reuse
- Metadata captures region, lake identifier, collection date, and variable definitions to support cross-lake comparisons.
- Clear documentation of methods, preservatives, storage conditions, and analytical references (e.g., Mackereth et al. 1989; Koroleff 1983; Jeffrey & Humphrey 1975) to support reproducibility.
- Useful for analyses of nutrient status, productivity indicators (Chl a, DOC), and chemical gradients across Arctic freshwater systems.
- Data collection notes highlight potential data gaps (e.g., single sampling per lake, regional scatter) and accessibility considerations (e.g., paywalls not indicated here; data stored in a shareable CSV).

## References
- Golterman et al., 1978; Jeffrey & Humphrey, 1975; Koroleff, 1983; Leavitt & Hodgson, 2001; Mackereth et al., 1989; McGowan et al., 2012; Qualls, 1989.