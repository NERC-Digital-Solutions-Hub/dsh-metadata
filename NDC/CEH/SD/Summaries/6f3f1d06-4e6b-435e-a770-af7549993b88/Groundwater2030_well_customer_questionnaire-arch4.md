# Well customer questionnaire

## Overview
- Instrument used when groundwater from sampled wells is sold to others.
- Conducted with a randomly selected groundwater customer who normally buys well water.
- Includes surveyor details, date, area, Well ID, owner name, customer name.
- Participant consent is read and recorded; if consented, Parts 1 and 2 of the questionnaire are completed.
- Areas covered: Manyatta, Migosi, and Other (specified).

## Data structure and key variables
- Part 1: Groundwater Use
  - Q1: Amount of well/borehole water bought yesterday (number of jerrycans).
  - Q2–Q3: Water safety actions taken (yes/no/don’t know) and specific treatment methods (boil, bleach/chlorine, water filters, let settle, strain, solar disinfection, other).
  - Q4: Presence of alternative water sources beyond the well/borehole (multiple sources listed).
  - Q5: Source use by purpose (for each purpose: drinking, cooking, washing, etc., across all source types). Includes coded reasons for source choice (1–7) with the bottom row for other details.
  - Q5 also records storage method for the water at the greatest quantity (uncovered/covered containers, etc.).
- Groundwater2030 module (context section on why sources are used)
  - Codes for reasons to use a source (1-cost, 2-quality, 3-availability, 4-access ease, 5-quantity, 6-taste/odor/color, 7-other).
- Part 2: Household Living Conditions and Food Security
  - Q1: Type of toilet facility.
  - Q2: Household assets (clock, electricity, TV, non-mobile phone, fridge) with yes/no/don’t know options.
  - Q3: Main cooking fuel (multiple fuel types listed).
  - Q4–Q5: Cooking location and presence of a separate kitchen.
  - Q6: Car ownership.
  - Q7: Main material of walls (observed entry with many material options).
  - Q8: Days in the last seven days with meat, rice, and wheat in a main meal.
  - Q9: Days in the last seven days with cassava only.
  - Q10: Days in the last 30 days with not enough to eat.
  - Q11: Months in the last 12 months with at least one day without enough to eat.
  - Q12: Purchase frequency for staple foods (maize, maize meal, potatoes) with defined frequency options.
  - Q13: Weeks in the past 12 months with stock of maize, maize meal, or potatoes.
- Data collection format
  - Options include numerical responses, single/multiple choice, and “other (specify)” fields.
  - Some questions require observational data (e.g., wall material).

## Data collection and governance
- Consent documented as: participate, not participate, or not available for interview.
- Use of standardized codes (e.g., 1/0/9 for yes/no/don’t know; 1–7 for reason codes).
- Open-ended fields for “Other” responses to capture non-listed options.
- Built to capture both direct respondent answers and household-level observations.

## Data quality considerations
- Potential recall bias due to short-term (yesterday) and longer-term (30–12 months) questions.
- Complex multi-source and multi-purpose table (Q5) may introduce entry errors without careful validation.
- Requires consistent coding and training to ensure comparability across enumerators (especially for observed attributes like wall materials).
- Data gaps may arise from non-response or consent refusal; “not available” and “don’t know” codes help flag these.

## Uses and implications for data strategy
- Assess groundwater reliance versus alternative sources and safety practices.
- Analyze how water source choices relate to sanitation, housing conditions, and food security indicators.
- Identify geographic or demographic disparities across Manyatta, Migosi, and other areas.
- Support program planning for water quality interventions, access improvements, and community education.
- Inform data governance: develop a comprehensive data dictionary, standardize variable names, and implement quality checks and validation rules.

## Key considerations and challenges for implementation
- Harmonizing the groundwater use module with the household living conditions module for integrated analysis.
- Ensuring privacy and ethical handling of consent, especially with sensitive food security questions.
- Maintaining consistent interpretation of “Other” responses and free-text fields.
- Balancing respondent burden with data richness in a comprehensive field survey.