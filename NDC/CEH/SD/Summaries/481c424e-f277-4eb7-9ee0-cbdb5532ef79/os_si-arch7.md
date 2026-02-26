# Oxidative stress markers in banded mongooses at Queen Elizabeth National Park, Uganda, 2017-2021

## What are the data?
- Dataset includes oxidative state markers for banded mongooses in Queen Elizabeth National Park, Uganda, from 2017 to 2021.
- Files:
  - GSH.csv: red blood cell concentrations of glutathione (GSH)
  - MDA_plasma.csv: blood plasma concentrations of malondialdehyde (MDA)
  - PC.csv: blood plasma concentrations of protein carbonyls (PC)
  - SOD.csv: red blood cell activity of total superoxide dismutase (SOD)
  - MDA_milk.csv: whole milk concentrations of malondialdehyde (MDA)
- MDA data include duplicates for quality control; other assays include repeats or duplicates as specified in their respective spreadsheets.

## Where and when were the data collected?
- Location: Queen Elizabeth National Park, Uganda (approx. 0°12'S, 29°54'E).
- Time period: 2017–2021.
- Sampling cadence: individuals trapped every 3–6 months.

## How were the data collected?
- Field procedures:
  - Trapping with box traps; anesthetized prior to blood collection.
  - Blood drawn from jugular vein; samples processed to plasma and red blood cells; snap-frozen and stored at -80°C until analysis.
- Measurements and assays:
  - MDA (plasma and milk): quantified by HPLC with fluorescence detection (MDA-TBA adducts).
  - Protein carbonyls: quantified via DNPH reaction and spectrophotometric readout; protein-normalized values provided.
  - SOD activity: determined by a plate assay using xanthine oxidase; units per mL lysate and per mL RBC reported.
  - Glutathione (GSH): quantified via DTNB reaction; values in μM with dilution factors noted.
- Data quality controls:
  - MDA plasma includes duplicates (MDA REPEAT).
  - Within-plate and between-plate repeats reported for PC and SOD and GSH as applicable.
  - Some samples excluded or limited due to hemolysis, cloudiness, low blood volume, or number of thawings.

## Data structure and key fields (per dataset)
- MDA_milk.csv (milk)
  - indv ID, capture.date, pack, MDA_milk_before_dilution, QUANTITY USED, MDA_milk_μM, DATE.processed
- MDA_plasma.csv (plasma)
  - indiv, sex, pack, capture.date, plasma.sample.pl, MDA (uM), MDA REPEAT (uM), MDA Date processed, Bloody y/n, Cloudy y/n, no. thaws
- PC.csv (protein carbonyls)
  - indiv, sex, pack, capture.date, plasma.sample.pl, Protein Conc. (mg/ml), Protein Carbonyl (nmol/ml), Carbonyl (nmol/mg), repeats and date processed, Bloody y/n, Cloudy y/n
- SOD.csv (SOD)
  - indiv, sex, pack, capture.date, rbc processing no., SOD Activity (U/ml lysate), Dilution Factor, SOD Activity (U/ml RBC), REPEAT fields, SOD Date processed
- GSH.csv (glutathione)
  - indiv, sex, pack, capture.date, rbc processing no., Glutathione (μM), Dilution factor, Glutathione repeat (μM), Repeat Dilution Factor, Date processed
- All datasets note sample-specific metadata such as hemolysis status, sample quality, and processing dates.

## Why were the data collected?
- To measure oxidative state in banded mongooses in relation to maternal nutrition condition and reproduction.

## Who was responsible for data collection and interpretation?
- Principal Investigator: Jonathan D. Blount (University of Exeter)
- Co-investigator: Michael A. Cant (University of Exeter)
- Postdoctoral researchers collecting/analyzing data: Magali Meniri, Faye J. Thompson, Harry H. Marshall

## Data quality and gaps
- Sample sizes vary by marker due to limited blood volume or capture feasibility.
- Some samples have missing or unusable data due to issues like hemolysis, cloudiness, or multiple freeze-thaws.

## GIS and data-use notes
- Spatial context: park-wide sampling within Queen Elizabeth National Park; precise site-level coordinates are not specified beyond the park location, but coordinates are given for the study location.
- Temporal context: multi-year (2017–2021) with regular sampling intervals, enabling time-series and space-time analyses.
- Potential map-based uses: visualize sampling effort by pack/location over time; correlate oxidative markers with spatial factors (e.g., pack ranges) and temporal factors (seasonality, reproductive cycles).
- Cautions: data may have missing values or varying sample sizes across markers; ensure QC flags (hemolysis, cloudy, repeats) are considered in GIS analyses.