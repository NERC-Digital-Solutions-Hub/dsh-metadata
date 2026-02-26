# Oxidative stress markers in banded mongooses at Queen Elizabeth National Park, Uganda, 2017-2021

## What are the data?
- Datasets measure oxidative state markers in banded mongooses: red blood cell glutathione (GSH), plasma malondialdehyde (MDA_plasma), protein carbonyls (PC), red blood cell superoxide dismutase activity (SOD), and milk malondialdehyde (MDA_milk).
- Specific files:
  - GSH.csv (RBC Glutathione)
  - MDA_plasma.csv (blood plasma MDA)
  - PC.csv (protein carbonyls)
  - SOD.csv (RBC SOD activity)
  - MDA_milk.csv (milk MDA)

## Where were the data collected?
- Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E)

## When were the data collected?
- 2017–2021

## How were the data collected?
- Field protocol:
  - Individuals trapped every 3–6 months using box traps.
  - Anesthesia with isoflurane prior to blood collection.
  - Blood drawn from jugular vein (100–500 μl) into EDTA tubes.
  - Plasma separated by centrifugation and frozen for MDA and PC analyses.
  - Red blood cells frozen for GSH and SOD analyses.
  - All samples snap-frozen in liquid nitrogen within 10 minutes of collection and shipped to a UK lab for storage at -80°C; analyses conducted within one year of collection.
- Assays:
  - MDA (plasma and milk): high-performance liquid chromatography (HPLC) with fluorescence detection; protocol adapted from Nussey et al. 2009.
  - MDA_milk: includes fields for pre-dilution, volume used, and μM concentration.
  - Protein carbonyls (PC): DNPH reaction; plate-reader measurement; standardization to protein concentration; specific sample processing steps and quality controls noted (e.g., within-plate or between-plate repeats, handling of haemolysis).
  - SOD: based on superoxide dismutation assay; RBCs diluted and assayed per kit instructions; duplicates used for QC.
  - GSH: DTNB-based assay; RBCs diluted, deproteinated, and assayed per kit instructions; duplicates used for QC.

## What measurements/datasets are included?
- GSH.csv: RBC glutathione levels with dilution factors and replicate data.
- MDA_plasma.csv: plasma MDA concentration with duplicates, hemolysis and cloudiness flags, number of thaws, and processing date.
- MDA_milk.csv: milk MDA concentration with pre-dilution details and sample processing data.
- PC.csv: protein carbonyl data (nmol/mg and nmol/ml) with repeat measurements and processing dates.
- SOD.csv: SOD activity (U/ml lysate and U/ml RBC) with dilution factors and repeats.
- SOD and GSH matrices include per-individual and per-sample fields (indiv, sex, pack, capture date, sample IDs, and processing dates).

## Why were the data collected?
- To measure oxidative state in banded mongooses in relation to maternal nutrition condition and reproduction.

## Who was responsible for the collection and interpretation of data?
- Principal Investigator: Jonathan D. Blount (University of Exeter)
- Co-investigator: Michael A. Cant (University of Exeter)
- Postdoctoral researchers collecting/analyzing data: Magali Meniri, Faye J. Thompson, Harry H. Marshall

## Data quality, handling, and missing data
- Sample sizes for markers vary due to blood volume limitations and capture feasibility.
- Duplicates are included for quality control; blocks where duplicates differ by more than 50% are re-run.
- Additional data quality fields tracked: hemolysis (Bloody), sample cloudiness, number of thaw events, and date processed.
- All analyses were conducted within a UK laboratory setting after field collection; some details depend on sample availability and storage constraints.

## Data gaps and limitations
- Some data are absent or incomplete for certain markers due to limited blood volume or unsuccessful captures, leading to variable sample sizes across markers.

## Reference
- Nussey, D.H., Pemberton, J.M., Pilkington, J.G., Blount, J.D., 2009. Life history correlates of oxidative damage in a free-living mammal population. Functional Ecology 23, 809-817.