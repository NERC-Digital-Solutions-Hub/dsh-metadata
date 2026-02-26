# Long-term multisite Scots pine trial, Scotland: temperatures and temperature variances for tree nurseries, 2007-2012

## Overview
- Multisite common garden trial of Scots pine seedlings to assess how temperature regimes influence growth and development.
- Seeds from 21 native Scottish populations (210 families; 5,040 individuals) were used to create replicated progeny across three nurseries.
- Temperature data are the primary environmental variable recorded to compare conditions across sites and over time.

## Experimental design and nurseries
- Three nurseries used: NW (outdoors, western Scotland), NE (outdoors in a fruit cage at James Hutton Institute, Aberdeen), NG (unheated glasshouse at James Hutton Institute, Aberdeen).
- In 2010, NG plants moved outdoors to Glensaugh, Aberdeenshire.
- Each nursery housed 8 seedlings per family, arranged in 40 randomised blocks (trays); each block contained two trees per population (total 42 trees).
- Seedlings were repotted in 2010 into 3 L pots with Ericaceous compost and slow-release fertiliser; no artificial light was used.

## Temperature data collection and variables
- Hourly temperatures recorded from Sep 2007 (NG and NE) or Nov 2007 (NW) to Mar 2012 using data loggers placed 50 cm above ground.
- Derived daily metrics for each nursery: DailyMaximum, DailyMinimum, DailyAverage, DailyVariance.
- DailyVariance further partitioned into DaytimeVariance (sunrise–sunset) and NighttimeVariance (sunset–sunrise).
- Sunset/sunrise times obtained from timeanddate.com using site coordinates.

## Data file structure
- File: NurseryTemperature.txt
- Key fields: Nursery (NE, NG, NW), Year (2007–2010), Month (1–12), Day (1–31), Date (DD/MM/YYYY), DailyMaximum (°C), DailyMinimum (°C), DailyAverage (°C), DailyVariance (°C²), DaytimeVariance (°C²), NighttimeVariance (°C²).
- Measurements are in degrees Celsius; data are recorded daily where all hourly readings for the day are present.

## Temporal coverage and site coordinates
- NG and NE: data from Sep 2007 onward; NW starts Nov 2007 onward; coverage through Mar 2012.
- Site coordinates referenced for precise sunset/sunrise calculations, with NW at approximately 57.775714, -5.597181; NE and NG at Aberdeen facilities; NG moved to Glensaugh in 2010 for outdoor exposure.

## Data quality, processing notes, and limitations
- If a day has more than one missing hourly record, that day's statistics are not calculated (omitted).
- The dataset focuses on temperature metrics; other environmental factors (e.g., light, moisture) are not included here.
- Experimental management changes (e.g., 2010 repotting and the NG outdoor move) may influence microclimate and should be considered in analyses.

## Potential analyses and uses
- Compare temperature regimes across nurseries to understand environmental differences affecting seedling growth.
- Analyze diurnal (day vs night) temperature variance and its association with growth or phenology.
- Develop or calibrate climate-growth models for Scots pine using the daily temperature and variance data.
- Integrate with growth or phenotypic data from the same trial to assess genotype-by-environment interactions across sites.