# Benthic particulate organic matter biomass

## Overview
- Data describe ash-free dry mass (AFDM) of three benthic organic matter size fractions, reported as means with standard deviations.
- Fractions: coarse woody debris (>1 cm), coarse particulate (>1 mm), and fine particulate (>0.250 mm).
- Data derived from up to 10 replicate Surber samples per site per occasion; results expressed as mean AFDM per square metre (mg m-2) with SD.

## Spatial and Temporal Coverage
- Location: three chalkstream sites in the Wessex chalk area — Nine Mile River, River Till, and River Wylye.
- Time period: collected between October 2012 and October 2013.
- Sampling frequency: Wyse and Nine Mile River – seven occasions; Till – five occasions.
- Sampling seasons: not conducted during salmonid breeding season (Dec–Mar) for the Till.

## Data Collection and Methods
- Field method: up to 10 Surber samples (0.25 x 0.25 m; mesh 0.025 mm) over a 100 m reach per site occasion.
- Lab processing: after sorting invertebrates, materials were separated into three fractions, dried, and ashed to determine AFDM.
- Drying: 80°C for at least 24 hours; final weighing with an Ohaus balance (to 0.0001 g).
- Ashing: 560°C for 8–12 hours; re-weighing.
- Output: AFDM mass per fraction, expressed as mg m-2 on the stream bed.

## Data Structure and Variables
- Spatial/identification fields: RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, NGR, EASTING, NORTHING.
- Temporal field: SAMPLE_DATE.
- Categorical field: POM_Fraction (coarse woody debris >1 cm; coarse particulate >1 mm; fine particulate >0.250 mm).
- Quantitative fields: Mean_AFDM_mgperm2, SD_AFDM_mgperm2, AFDM_n (number of samples per site).

## Data Provenance and Quality Assurance
- Collected and interpreted by Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.
- Quality practices: standard laboratory procedures followed; no formal QA such as replicate repeats within surber samples; final values screened for outliers (none detected).

## Completeness and Limitations
- Sampling completeness: Nine Mile River and Wylye collected on 7 occasions; Till on 5 occasions.
- Sampling gaps: no sampling during Dec–Mar for the Till to avoid disturbance to redds.
- Replicates: 10 replicates for Oct 2012, Feb 2013, Mar 2013, May 2013; 5 replicates for Jul 2013, Aug 2013, Oct 2013.

## Potential GIS Applications
- Map-based visualization of AFDM by river, site, and sampling date.
- Spatial comparison of detritus standing stocks across rivers with different land-use gradients.
- Temporal analysis of detritus dynamics across seasons and sites; integration with other environmental layers (e.g., land use, hydrology, habitat maps).