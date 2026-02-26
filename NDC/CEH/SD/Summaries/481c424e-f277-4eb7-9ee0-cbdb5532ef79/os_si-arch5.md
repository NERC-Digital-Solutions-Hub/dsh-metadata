# Oxidative stress markers in banded mongooses at Queen Elizabeth National Park, Uganda, 2017-2021

## Purpose and scope
- Characterizes oxidative state markers in banded mongooses at Queen Elizabeth National Park, Uganda, collected from 2017 to 2021.
- Data are intended to relate oxidative stress to maternal nutrition condition and reproduction.

## What the data are
- Measurements include:
  - Red blood cell concentrations of glutathione (GSH)
  - Blood plasma concentrations of malondialdehyde (MDA)
  - Blood plasma concentrations of protein carbonyls (PC)
  - Red blood cell activity of total superoxide dismutase (SOD)
  - Whole milk concentrations of malondialdehyde (MDA_milk)
- Data are organized into separate spreadsheets (datasets) with specific fields:
  - MDA_milk.csv
  - MDA_plasma.csv
  - PC.csv (protein carbonyls)
  - SOD.csv (SOD activity)
  - GSH.csv (glutathione)
- Each dataset includes identifiers for individuals, sampling events, and assay-specific metadata and quality control indicators.

## Where and when the data were collected
- Location: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E)
- Timeframe: 2017–2021

## How the data were collected
- Population sampling:
  - Individuals trapped every 3–6 months using box traps
  - Anesthesia with isoflurane prior to blood collection
  - Blood collected from the jugular vein (100–500 μL) into EDTA tubes
  - Plasma separated by centrifugation and stored at -80°C; plasma analyses conducted later
  - Red blood cells (RBC) snap-frozen in liquid nitrogen and stored at -80°C until analysis
- Sample handling and storage:
  - All samples snap-frozen within ~10 minutes of collection
  - Transport to UK laboratory in cryogenic shippers; analyses conducted within one year of collection
- Assays:
  - MDA (plasma and milk) quantified by HPLC with fluorescence detection; methodology adapted from Nussey et al. (2009)
  - Protein carbonyls quantified using DNPH-based assay with plate reader; adjustments made due to limited plasma and high protein content
  - SOD activity measured via xanthine oxidase–based assay; RBCs diluted and assayed per kit instructions
  - GSH quantified using a DTNB-based assay; RBCs deproteinated prior to assay
- Quality controls:
  - Plasma measurements include duplicates (MDA) and run in duplicates for QC
  - SOD and GSH assays include within-plate duplicates; repeated runs if >50% difference between duplicates
  - PC measurements include within-plate and between-plate repeats
  - Samples annotated with indicators (Bloody, Cloudy, number of thaws, etc.)

## Data structure and key fields (highlights)
- MDA_milk.csv: individual, capture.date, pack, MDA_milk_before_dilution, QUANTITY USED, MDA_milk_μM, DATE.processed
- MDA_plasma.csv: indiv, sex, pack, capture.date, plasma.sample.pl, MDA (uM), MDA REPEAT (uM), MDA Date processed, Bloody y/n, Cloudy y/n, no. thaws
- PC.csv: indiv, sex, pack, capture.date, plasma.sample.pl, Protein Conc. (mg/ml), Protein Carbonyl (nmol/ml), Carbonyl (nmol/mg), Within Plate Repeat, Between Plate Repeat, P.C Date processed, P.C repeat Date processed, Bloody y/n, Cloudy y/n, No freeze thaws for 1st run
- SOD.csv: indiv, sex, pack, capture.date, rbc processing no., SOD Activity (U/ml lysate), Dilution Factor, SOD Activity (U/ml RBC), SOD REPEAT (U/ml lysate), Dilution Factor REPEAT, SOD Activity (U/ml RBC) repeat, SOD Date processed
- GSH.csv: indiv, sex, pack, capture.date, rbc processing no., Glutathione (uM), Dilution factor, Glutathione repeat (μM), Repeat Dilution Factor, Glutathione Date processed, Glutathione repeat Date processed

## Data governance, provenance, and responsibility
- Principal Investigator: Jonathan D. Blount (University of Exeter)
- Co-Investigator: Michael A. Cant (University of Exeter)
- Postdoctoral contributors who collected/analyzed data: Magali Meniri, Faye J. Thompson, Harry H. Marshall
- Documentation includes detailed laboratory methods, quality control procedures, and data field definitions to support data reuse and reproducibility.

## Data quality, limitations, and completeness
- Variability in sample sizes across markers due to:
  - Insufficient blood volume for certain assays
  - Trapping success and frequency
- Data include multiple QC indicators (blood contamination, sample clarity, number of thaws, duplicates/repeats) to flag potential issues
- Some data fields indicate where abnormalities or limitations occurred (e.g., bloody/hemolyzed samples, cloudy plasma)

## Practical considerations for data discovery and reuse
- Datasets are organized by biomarker type and sample matrix (milk, plasma, RBC)
- Clear metadata and QC indicators support data discovery, filtering, and quality assessment
- Temporal coverage spans 2017–2021 with associated processing dates for traceability
- Related reference provided for methodological context: Nussey et al. 2009 (MDA methodology)
- No licensing or access restrictions are specified in the provided text; users should verify data sharing terms with the data holders

## Reference
- Nussey, D.H., Pemberton, J.M., Pilkington, J.G., Blount, J.D., 2009. Life history correlates of oxidative damage in a free-living mammal population. Functional Ecology 23, 809-817. https://doi.org/10.1111/j.1365-2435.2009.01555.x