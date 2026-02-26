# Well owner questionnaire

## Overview
- A household- and well-level survey instrument designed to capture groundwater use, water safety practices, alternative water sources, sanitation, housing characteristics, assets, and nutrition/food security data.
- Aims to support GIS-enabled analysis and mapping of groundwater access, water safety behaviors, and related infrastructure decisions.
- Collects both quantitative (numbers, frequencies) and qualitative (descriptions, reasons) data, with coded response options to enable integration with other datasets.

## Key spatial and identifying data
- Area (choices: Manyatta / Migosi / Other)
- Well ID
- Well owner name
- Consent to participate (must confirm before proceeding)

## Groundwater use and access (Main data section)
- Q1: Daily water collection from well (in 20 L jerrycans) the previous day (includes all users)
- Q2: Whether the household sells well water (Yes/No/Don't know)
  - If No, Q3 asks for approximate amount sold yesterday
- Q3 (in practice): Identification of neighboring households that buy water; select one buyer at random for follow-up
- Q4: Land ownership status of the well site (owner/landlord, etc.)
- Q5: Any measures to make water safer to drink? (Yes/No/Don't know)
- Q6: If yes, list all stated water-safety practices (e.g., boil, chlorine, filtration, solar disinfection, settling, other)
- Storage method: choose the storage method used to store the greatest amount of water after collection
- Q7: Availability of other water sources beyond the well (e.g., piped water, borehole, rainwater, vendor, surface water, bottled water, etc.)
- Q8: For each water source, indicate its use for multiple household purposes (drinking, cooking, washing, etc.) and capture the reason for source choice using codes (1–7), including “Sell to others” as a use for each source
- Note: The questionnaire includes a comprehensive matrix listing sources (Piped Kiwasco, Borehole, Dug well, Water from spring, Rainwater, Tanker truck, Water from vendor, Surface water, Bottled water) and numerous household purposes (drinking, cooking, washing, flushing toilet, irrigation, animals, etc.)

## Sanitation, housing, and assets (household profile)
- Toilet facility type used by the household (e.g., flush, pit latrine, bucket, etc.)
- Ownership of household items (clock/watch, electricity, television, non-mobile phone, refrigerator) with Yes/No/Don't know responses
- Primary cooking fuel type (electricity, LPG/natural gas, biogas, kerosene, coal, charcoal, wood, agricultural waste, dung, etc.)
- Cooking location (in-house, separate building, outdoors); whether a separate kitchen room exists
- Car ownership (Yes/No/Don't know)
- Main wall material (various options including dirt, cane, adobe, wood, bricks, cement, etc.)
- Date-related nutrition/diet questions: number of days in the last week the main meals included meat, rice, and wheat products
- Food security indicators:
  - Number of days in the last 30 days with not enough to eat
  - Number of months in the last 12 months with at least one day without enough to eat
- Food stock and purchase patterns:
  - Frequency of purchasing staples (maize, maize meal, potatoes)
  - Number of weeks in the past 12 months with a stock of certain staples at home

## Data coding and response formats
- Binary/ordinal coding: Yes = 1, No = 0, Don’t know = 9
- Frequency scales for staples: Daily, Twice a week, Weekly, Fortnightly, Monthly, Less frequent than once per month
- Quantitative fields: numeric entries for counts (e.g., number of jerrycans, days, weeks, months)
- Consistent use of 20 L units and explicit consent verification

## GIS and data integration considerations
- Spatial linkage via Well ID and Area enables point-based mapping of wells and associated attributes
- Ability to join well-level data with external datasets on land ownership, housing materials, and water infrastructure
- Rich multi-source water-use data supports thematic mapping of source dependence by purpose
- Data quality considerations include handling missing, unknown, or ambiguous responses and standardizing codes across datasets

## Practical implications for GIS specialists
- Build point feature classes for wells with attributes for groundwater use, water safety practices, storage, and source repertoire
- Create layers or heatmaps of water sources and use patterns to identify gaps in access or reliability
- Develop dashboards showing relationships between water sources, sanitation facilities, and food security indicators at the community or village level
- Use standardized coding to facilitate cross-w Survey integration, quality control, and longitudinal analyses (e.g., monitoring changes over time)

## Endnotes and notes
- The instrument includes a Groundwater2030 section with codes for why sources are chosen, indicating an emphasis on understanding drivers behind source selection
- Consent and random sampling procedures are embedded in fieldwork instructions to ensure ethical and unbiased data collection