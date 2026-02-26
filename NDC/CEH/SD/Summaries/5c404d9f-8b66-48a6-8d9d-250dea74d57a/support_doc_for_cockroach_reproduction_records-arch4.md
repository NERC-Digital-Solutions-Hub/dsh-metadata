# Description

## What was recorded
- Records of offspring production for 192 female cockroaches (Blaptica dubia); counted nymphs produced in up to two clutches and entered into a spreadsheet.

## Where and when
- Location: University of Aberdeen Zoology building insectary (ground floor).
- Dates: 29/12/23 to 23/01/24.

## How data were collected
- Each female stored in an individual box with food, hydration, and shelter; checked twice a week to count offspring and remove them.

## Experimental design and purpose
- Part of the project "The evolution and plasticity of social networks traits" to determine fitness consequences of social network position at different humidities.
- 192 females mated with two males over two weeks at 28C and ~50% humidity.
- Two humidity treatments during a two-week experimental period: 50% (n=96) or 30% (n=96).
- Social associations recorded in groups of 24 (refer to cockroach_aggregation_records).
- After experimental period, all returned to 28C 50% humidity in individual containers; number of nymphs produced checked twice a week for 10 weeks; by then no female had produced offspring in 10 days.

## Data structure and completeness
- All females have a brood record.
- Brood 1 non-zero for 40/192; brood 2 non-zero for 1/192.
- If zero nymphs were produced in a brood, there is no date and an 'NA' fills the cell.

## Metadata fields
- unique_ID: unique identifier for each female.
- humidity: humidity level (50% or 30%), during the experimental period.
- label: tag used for visual identification.
- group: social group identifier.
- nymphs: number of nymphs produced in the first brood (0 if none).
- date1: date of the first brood (NA if none).
- nymphs2: number of nymphs produced in the second brood (0 if none).
- date2: date of the second brood (NA if none).
- total_off: total offspring (sum of nymphs and nymphs2).

## Roles and interpretation
- Data collection: Callum McLean (research associate), Georgia Cash (PhD student), and David Fisher (principal investigator).
- Interpretation: McLean and Fisher.

## Notes and related data
- Related dataset referenced: cockroach_aggregation_records (social associations).