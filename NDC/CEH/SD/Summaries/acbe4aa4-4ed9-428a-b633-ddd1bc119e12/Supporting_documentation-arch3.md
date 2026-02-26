# Feather isotope ratios and sexing of oystercatchers breeding in Iceland

## Purpose and scope
- Investigates environmental and demographic drivers of migratory strategies in oystercatchers (Haematopus ostralegus) breeding in Iceland.
- Study conducted across south, west, north-west, and north-east Iceland during summers 2013–2017.
- Uses stable isotope ratios in chest feathers grown during the wintering period to infer diet and habitat use.
- Includes molecular sexing to determine sex composition where possible.

## Study design and sampling
- Incapture of incubating oystercatchers on nests using a spring trap; birds uniquely marked.
- Chest feathers collected (4–5 feathers per individual) for isotopic analysis; feathers grown on wintering grounds reflect conditions during wintering.
- Subset of birds had blood samples collected for DNA-based sex determination.

## Data files and contents
- OystercatcherFeatherIstotopes.csv
  - Sample size: 552 oystercatchers sampled during breeding in Iceland.
  - Columns include:
    - Year of feather collection (2013–2017)
    - Individual ID (unique ring-based identifier)
    - d15N (Nitrogen isotope ratio)
    - d13C (Carbon isotope ratio)
    - Status (Migrants, Unknown, or Resident)
    - WinterLocation (country/location observed during winter)
- OystercatcherSexing.csv
  - Sample size: 321 oystercatchers with DNA-based sex determination.
  - Columns include:
    - Individual ID
    - DNA-derived sex

## Laboratory methods and quality control
- Stable isotope analysis
  - Feathers washed (2:1 chloroform/methanol), dried, and cut into fragments.
  - Samples weighed (0.45–0.55 mg) and packed in tin capsules for analysis.
  - Analyzed with Costech elemental analyzer + Thermo Scientific Delta XP IRMS; δ13C reported against Vienna Pee Dee Belemnite (V-PDB); δ15N against AIR N2.
  - Internal standard (collagen) used for quality checks.
  - Replicate measurements indicate measurement errors of 0.2‰ for δ13C and 0.1‰ for δ15N.
- Molecular sexing
  - DNA extracted from blood via ammonium acetate method.
  - Sex determined using established molecular protocol (Fridolfsson & Ellegren, 1999).

## Metadata and interpretation
- Key variables:
  - Year (2013–2017)
  - Individual ID (unique identifier)
  - d13C and d15N (isotope signatures reflecting winter diet/habitat)
  - Status (Migrants, Unknown, Resident)
  - WinterLocation (location during winter)
  - Sex (from DNA, for subset)
- Feathers reflect winter-period conditions; combined with breeding-season capture data to infer migratory strategies and habitat use.

## Relevance for monitoring and governance
- Provides longitudinal data on migratory strategies and wintering ecology essential for environmental health monitoring.
- Demonstrates integration of biological indicators (stable isotopes) with genetic sexing to understand population structure and movement.
- Highlights the importance of transparent data handling, robust metadata, and standardized laboratory procedures for monitoring outputs.
- Data can inform policy decisions on habitat protection and management of migratory waterbird populations.

## Limitations and considerations
- Isotope data reflect conditions during wintering, inferred from feathers grown in that period; interpretation assumes stable baseline conditions.
- Status classifications depend on observational data and may have uncertainties.
- Not all individuals have both isotope and sex data; cross-mataset analyses require careful matching by Individual ID.
- Data quality depends on consistent sample processing and metadata completeness across years and sites.

## Usage notes
- Data are provided with clear laboratory and analytical context, enabling reuse in monitoring assessments or meta-analyses.
- When integrating into monitoring frameworks, ensure rigorous metadata documentation, data provenance, and transparency about sampling timelines and population connectivity.