# Oxidative stress markers in banded mongooses at Queen Elizabeth National Park, Uganda, 2017-2021

## Overview
- Dataset of oxidative state markers in banded mongooses from Queen Elizabeth National Park, Uganda, collected 2017–2021.
- Markers include: red blood cell glutathione (GSH), plasma malondialdehyde (MDA_plasma), plasma protein carbonyls (PC), red blood cell superoxide dismutase activity (SOD), and milk malondialdehyde (MDA_milk).
- Aimed at understanding oxidative stress in relation to maternal nutrition and reproduction.

## Study site and period
- Location: Queen Elizabeth National Park, Uganda (0°12'S, 29°54'E).
- Timeframe: 2017–2021.

## Data collection methods
- Subjects: banded mongooses trapped every 3–6 months.
- Procedure: box traps used; animals anesthetized with isoflurane prior to blood collection.
- Sample collection: 100–500 μl blood drawn from jugular vein; plasma separated by centrifugation and frozen; red blood cells frozen for RBC analyses.
- Storage and transport: snap-frozen in liquid nitrogen within 10 minutes; shipped to UK lab and stored at -80°C until analysis; analyses conducted within one year of collection.

## Measurements and assays
- MDA (plasma and milk): quantified by HPLC with fluorescence detection; milk and plasma samples processed with thiobarbituric acid reaction and subsequent extraction.
- Protein carbonyls (PC): quantified via DNPH reaction; absorbance read at 370 nm; results normalized to protein concentration.
- SOD (RBC): determined by inhibition of superoxide radicals using a xanthine oxidase system; results given as U/ml lysate and U/ml RBC.
- Glutathione (GSH): measured via DTNB (Ellman) reaction; RBCs deproteinated before assay; results in μM.
- Data capture: multiple spreadsheets with detailed metadata per marker (e.g., sample IDs, sex, pack, processing dates, duplicates, QC notes).

## Data structure and files
- MDA_milk.csv: milk MDA concentrations with sample metadata.
- MDA_plasma.csv: plasma MDA concentrations with sample metadata (including duplicate measurements and quality flags).
- PC.csv: protein carbonyl measurements with detailed within/between plate repeat data and sample processing notes.
- SOD.csv: SOD activity measurements with lysate and RBC values and repeats.
- GSH.csv: glutathione concentrations with duplicate measurements and processing dates.
- Additional data quality fields present across datasets (e.g., bloody/cloudy flags, number of thaws).

## Rationale and scope
- Purpose: quantify oxidative state to relate maternal nutrition and reproductive biology to oxidative stress in a wild mammal population.
- Reference framework: methods align with Nussey et al. 2009 for oxidative damage metrics.

## Data quality, QA, and completeness
- Quality control: duplicates included for several markers (e.g., MDA_plasma, SOD, GSH); within-plate and between-plate repeats documented.
- Sample limitations: occasional missing data due to insufficient blood volume or capture variability; sample sizes for markers vary accordingly.
- Documentation: extensive procedural detail provided to enable replication and verification.

## Roles and data stewardship
- Principal investigator: Jonathan D. Blount (University of Exeter); co-investigator: Michael A. Cant (University of Exeter).
- Postdoctoral researchers involved in collection and analysis: Magali Meniri, Faye J. Thompson, Harry H. Marshall.
- Data handling: samples stored and analyzed per lab protocols; outputs intended for repository posting and portal-upload to ensure accessibility.

## Data accessibility and references
- Data are described with explicit sample and processing metadata; the primary reference for the MDA methodology is Nussey et al. (2009).