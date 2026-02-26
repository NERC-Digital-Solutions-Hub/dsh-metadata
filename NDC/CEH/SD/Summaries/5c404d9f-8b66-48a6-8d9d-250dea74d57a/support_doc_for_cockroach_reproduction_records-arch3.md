# Description

## Overview
- Records of offspring production for 192 female cockroaches (Blaptica dubia); counted the number of nymphs produced in up to two clutches and entered into a spreadsheet.
- Purpose: part of the project "The evolution and plasticity of social networks traits" to determine fitness consequences of social network position at different humidities.
- Location and period: University of Aberdeen Zoology building insectary; 29/12/23 to 23/01/24.

## Experimental design and data collection
- Each female mated with two males over two weeks at 28°C and approximately 50% humidity.
- Two paper tags attached to each female for identification.
- Females transferred to an incubator at 28°C with either 50% or 30% humidity for two weeks (the experimental period), during which social associations were recorded in groups of 24.
- After the experimental period, all females returned to 28°C at 50% humidity in individual containers; the number of nymphs produced was checked twice weekly.
- This process continued for 10 weeks, by which point no female had produced offspring in the last 10 days.

## Data and sampling completeness
- All females have brood records; 40/192 produced a non-zero value for brood one and 1/192 produced a non-zero value for brood two.
- If zero nymphs were produced in a brood, there is no date recorded and an 'NA' fills the cell.

## Metadata and data structure
- Columns: unique_ID, humidity, label, group, nymphs, date1, nymphs2, date2, total_off.
- Field descriptions:
  - unique_ID: unique identifier for each female cockroach.
  - humidity: humidity level (50% or 30%) during the social association recording.
  - label: tag used for visual identification.
  - group: social group identifier.
  - nymphs: number of nymphs produced in the first brood (0 if none).
  - date1: date of the first brood (NA if none).
  - nymphs2: number of nymphs produced in the second brood (0 if none).
  - date2: date of the second brood (NA if none).
  - total_off: total offspring across broods.

## Responsibilities and interpretation
- Data collection and interpretation conducted by: Research associate Callum McLean, PhD student Georgia Cash, and Principal Investigator David Fisher (with McLean and Fisher responsible for interpretation).

## Data governance and practical considerations for monitoring frameworks
- Clear provenance and structured metadata support reproducibility and evaluation of how social environment and humidity influence fitness.
- Documented experimental conditions (temperature, humidity) and data collection schedule (twice weekly checks) aid ongoing monitoring and replication.
- Completeness and explicit handling of missing data (NA for absent dates) provide transparency for data quality assessment.