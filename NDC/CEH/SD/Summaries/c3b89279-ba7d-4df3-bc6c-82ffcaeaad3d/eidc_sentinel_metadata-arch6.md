# Sentinel project bat and bird survey data, 20202023

## Overview
- Data collected under the Sentinel project (Social and Environmental Trade-Offs in African Agriculture) to assess ecological impacts of agricultural expansion in Ghana and Zambia.
- Aimed to understand community structure and species composition across land-use gradients, and to investigate dietary habits and potential shifts in ecosystem service delivery.

## Survey scope and design
- Timeframe: December 2020 to March 2023.
- Study countries and localities: Ghana (3 localities) and Zambia (5 localities).
  - Ghana: Upper Guinean wet evergreen forests, bordered by cacao and rubber plantations.
  - Zambia: Subtropical climate with dry miombo woodlands and evergreen Cryptocephalum forests, surrounded by maize and cassava cultivation.
- Site selection: mix of landscapes with recent agricultural expansion and baseline reference sites with more intact vegetation.
- Sampling framework: two-tier stratified random design using a 1 km × 1 km grid per locality.
  - Land-use classifications: Not Applicable (NA), Agriculture Only, Forest edge, Forest.
  - Subset sampling within Agriculture, Forest edge, and Forest categories; some sites later became inaccessible requiring plan adjustments.
- Within sites: survey points chosen randomly along transects, at least 200 m apart.

## Survey methods
- Birds
  - Point counts conducted at dawn, totaling about 3 hours per location.
  - 10-minute counts within a 50 m radius; record birds seen or heard to species level, estimate group size, note perched vs flying, and separate observations beyond 50 m.
  - Additional weather and vegetation data collected at each point.
  - Some sites used mist nets to sample understory birds.
- Mist nets (birds)
  - At least 180 m of net lanes per site, using four 30 mm mesh nets (6–18 m lengths).
  - Netting conducted from 5:30 to 10:00, avoiding dawn and dusk extremes to minimize bat capture.
  - Birds netted, identified to species, weighed, sexed and aged where possible; released within about 30 minutes.
  - Callback techniques used to attract birds.
- Bats
  - Conducted at the same locations as bird mist netting; sampling on separate nights.
  - Equipment: 1–2 harp traps and multiple mist nets; minimum 4 hours per night with checks every 15–30 minutes.
  - Netting performed under suitable weather; bats identified using regional reference guides.
- Data handling
  - Multiple data inputters digitized field sheets.
  - Datasets were compiled, error-checked and validated.

## Data description
- Data package: Sentinel_survey_data.zip containing two dataframes.
- Bird point counts dataframe (Sentinel_Pointcount_data.csv)
  - Key variables: Country, Locality, Grid, Transect, Point, Site, Latitude, Longitude, Collection.date, Observer.Initials, Time.Started, Common.name, Species.name, Perch.Under.50m, Flyover.Under.50m, Total.Under.50m, Over.50m, Total, Observation.Type, Temp, Cloud.Cover, Wind, Rain, Land.Grid, Land.Point, Land.Site, MaxCan, MinCan, MeanCan, MaxVis, MeanVis, TreeS, TreeM, TreeL, TreeTotal.
- Bat and bird mistnetting dataframe (Sentinel_Mistnetting_data.csv)
  - Key variables: Country, Locality, Site, Site.type, Latitude, Longitude, Collection.date, Specimen.number, Class, Scientific.name, Common.name.
- Data quality notes:
  - Missing data designated as 'NA'.
  - Data fields provide spatial (lat/long), temporal (date/time), observational (counts, observation type), and environmental (weather/vegetation) context.

## Data access and quality notes
- Data were consolidated from multiple inputters and undergo error checking and validation to ensure consistency.
- Some sampling sites were modified due to accessibility and permission issues, reflecting real-world field constraints.

## References
- Bird census and survey techniques; mammals of Africa guides; regional bat phylogenies and identification references used for species verification.