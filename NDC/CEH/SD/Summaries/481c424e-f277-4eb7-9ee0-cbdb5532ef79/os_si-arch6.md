# Oxidative stress markers in banded mongooses at Queen Elizabeth National Park, Uganda, 2017-2021

## Data overview
- Dataset collecting markers of oxidative state in banded mongooses at Queen Elizabeth National Park, Uganda, from 2017 to 2021.
- Data files and targets:
  - GSH.csv: red blood cell concentrations of glutathione (GSH)
  - MDA_plasma.csv: blood plasma concentrations of malondialdehyde (MDA)
  - PC.csv: blood plasma concentrations of protein carbonyls (PC)
  - SOD.csv: red blood cell activity of total superoxide dismutase (SOD)
  - MDA_milk.csv: whole milk concentrations of malondialdehyde (MDA in milk)
- Example measured metrics (where provided):
  - GSH: Glutathione (μM)
  - MDA_plasma: MDA (μM)
  - PC: Protein Carbonyl (nmol/ml) and related units
  - SOD: SOD Activity (U/ml lysate) and SOD Activity (U/ml RBC)
  - MDA_milk: MDA (μM)
- Data include duplicate measurements for quality control (e.g., MDA_plasma duplicates; SOD duplicates; PC within/between plate repeats; GSH repeats).

## Study location and period
- Location: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E)
- Sampling period: 2017–2021
- Sampling method: Individual mongooses trapped every 3–6 months using box traps; anaesthetized prior to blood collection; blood drawn from jugular vein.

## Data collection and laboratory methods
- Sample processing:
  - Blood (100–500 μl) collected into EDTA tubes; plasma separated by centrifugation and stored at -80°C; RBCs stored for GSH and SOD analyses.
  - All samples snap-frozen in liquid nitrogen within 10 minutes of collection; transported on dry ice to UK lab; analyses completed within one year of collection.
- Assays:
  - MDA: Quantified by HPLC with fluorescence detection after TBARs method; detailed reagents and protocol provided (including external calibration with TEP).
  - MDA in milk: Measured with pre-dilution and sample-specific adjustments captured in MDA_milk_before_dilution, QUANTITY USED, and MDA_milk_μM.
  - Protein carbonyls (PC): Measured via DNPH reaction forming hydrazone; absorbance read at 370 nm; protein concentration used for normalization; multiple plate repeats recorded (within-plate and between-plate).
  - SOD: Activity determined by xanthine oxidase-generated superoxide radicals; One unit defined as dismutation of 50% of superoxide; RBCs diluted and assayed per kit instructions; duplicates used for QC.
  - Glutathione (GSH): Measured via reaction with DTNB (5,5'-dithiobis(2-nitrobenzoic)) to form TNB; RBCs diluted, deproteinized, and assayed per kit instructions; duplicates used for QC.
- Data quality controls:
  - Duplicates for key measurements (MDA_plasma, PC, SOD, GSH) and criteria to re-run if duplicates differ by more than 50%.
  - Documentation includes sample processing details, hemolysis/clarity flags, number of thaws, and date processed.

## Data structure and key fields
- MDA_milk.csv
  - Fields: individual, capture.date, pack, MDA_milk_before_dilution, QUANTITY USED, MDA_milk_μM, DATE.processed
- MDA_plasma.csv
  - Fields: indiv, sex, pack, capture.date, plasma.sample.pl, MDA (uM), MDA REPEAT (uM), MDA Date processed, Bloody y/n, Cloudy y/n, no. thaws
- PC.csv
  - Fields: indiv, sex, pack, capture.date, plasma.sample.pl, Protein Conc. (mg/ml), Protein Carbonyl (nmol/ml), Carbonyl (nmol/mg), within-plate repeat metrics, between-plate repeat metrics, P.C Date processed, P.C repeat Date processed, Bloody y/n, Cloudy y/n, No freeze thaws for 1st run
- SOD.csv
  - Fields: indiv, sex, pack, capture.date, rbc processing no., SOD Activity (U/ml lysate), Dilution Factor, SOD Activity (U/ml RBC), SOD REPEAT (U/ml lysate), Dilution Factor REPEAT, SOD Date processed
- GSH.csv
  - Fields: indiv, sex, pack, capture.date, rbc processing no., Glutathione (uM), Dilution factor, Glutathione repeat (μM), Repeat Dilution Factor, Glutathione Date processed, Glutathione repeat Date processed

## Purpose and intended use
- Primary aim: Measure oxidative state in banded mongooses with respect to maternal nutrition condition and reproduction.
- Data are intended to support analyses of relationships between maternal condition, reproduction, and oxidative stress markers across multiple biological matrices (blood and milk).

## Responsibilities and provenance
- Principal Investigator: Jonathan D. Blount (University of Exeter)
- Co-investigator: Michael A. Cant (University of Exeter)
- Postdoctoral Researchers collecting/analyzing data: Magali Meniri, Faye J. Thompson, Harry H. Marshall

## Data completeness and limitations
- Sample sizes for markers vary due to:
  - Insufficient blood volume for some assays
  - Inability to capture individuals at times
- Data include multiple quality-control notes (e.g., duplicates, hemolysis/clarity flags, no. of thaws) but may have missing values in certain fields or samples.

## Reference
- Nussey, D.H., Pemberton, J.M., Pilkington, J.G., Blount, J.D. (2009). Life history correlates of oxidative damage in a free-living mammal population. Functional Ecology, 23, 809-817. https://doi.org/10.1111/j.1365-2435.2009.01555.x