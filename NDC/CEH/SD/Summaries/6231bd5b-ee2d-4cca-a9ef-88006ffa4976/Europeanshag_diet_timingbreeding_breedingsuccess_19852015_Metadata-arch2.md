# JAE_Keogan_Europeanshag_phenologymismatch_shagdataset

## Overview
- A data-focused document detailing datasets used to study phenology mismatch between European shag and its prey.
- Presents variables and data structure across three interconnected datasets: shag dataset, diet dataset, and bivariate dataset.
- Aimed at standardised monitoring outputs (reports, maps, charts) and proper data storage.

## Datasets and Key Variables

### shagdataset
- year
- laydate: day first egg in nest was laid (day of year from Jan 1)
- chicks.fledged.first: number of chicks fledged in the first clutch
- failedeggsfirst: number of failed eggs in the first clutch
- Mean.Lay: average lay date in each year
- relative.lay: nest lay date relative to annual mean lay date (in days)
- SST.past: average February/March SST in year -1
- SST.present: average February/March SST in current year
- pop.size: population size in breeding pairs
- yearcentre: year centred around the study’s average year
- chicks.fledged.all: number of chicks fledged from all clutches
- failedeggsall: number of failed eggs from all clutches

### dietdataset
- Year
- Date: day of sample collection (since Jan 1)
- Age: whether sample was from a chick or an adult
- SST: average February/March SST in current year
- yearcentre: year centred around the study’s average year
- meandate: average date of sample collection in each year
- datediff: sample collection date centred around the annual average
- SE1:SE0_proportion: proportion of 1+ sandeels relative to all sandeels in sample
- logitSE1:SE0: logit-transformed proportion above

### bivariatedataset
- Year
- Species: shag or sandeel
- chicks.fledged: number of chicks fledged
- failedeggs: number of potential failed eggs
- sandeelproportion: proportion of 1+ sandeels relative to all sandeels in sample
- dayofyear: day of laying (shags) or day of sample collection (sandeels)
- Mean.Lay: average lay date in each year
- Relative: day of year (lay date or sample collection) centred around the average lay date

## Data handling and outputs
- Data verification, quality assurance, cleaning, and transformation processes
- Analyses use standardised methods to categorise environmental health against standards
- Outputs presented as reports, maps, and charts
- Datasets stored and uploaded to appropriate data portals

## Cross-cutting challenges for Analysts Monitoring the Environment
- Increasing the value of datasets by combining them with other relevant data (avoiding “single use”)
- Enabling access to the underlying data used to create final outputs

## Additional context
- The document integrates multiple datasets to support monitoring of phenology mismatch in European shag systems and their prey dynamics, aligning with standardised environmental monitoring practices and data governance.