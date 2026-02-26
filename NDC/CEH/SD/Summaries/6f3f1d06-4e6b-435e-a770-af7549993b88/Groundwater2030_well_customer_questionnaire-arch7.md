# Well customer questionnaire

- Purpose and scope
  - Field questionnaire used when water from sampled wells is sold to others.
  - Administered to a randomly selected groundwater customer who typically buys well/borehole water.
  - Includes informed consent process; collects consent status and proceeds with Parts 1 and 2 if consented (Part 2 not shown here).

- Survey process and structure
  - Surveyor records: name, date, area (Manyatta / Migosi / Other), Well ID, well owner, and groundwater customer name.
  - Verifies that the approached person buys water from the relevant well/borehole.
  - Consent is documented; if consented, Part 1 (Groundwater Use) is completed (Part 2 details not provided in the text).

- PART 1: GROUNDWATER USE (key data elements)
  - Q1: Quantity purchased yesterday (number of jerrycans).
  - Q2: Water safety measures before drinking (Yes/No/Don't know).
  - Q3: What is done to make water safer (multiple options: boil, bleach/chlorine, water filters, let it stand to settle, strain through cloth, solar disinfection, other).
  - Storage method after collection (uncovered small container, covered small container, covered large container/tank, other; circle the method used for the greatest amount stored).
  - Q4: Other water sources available for household use (e.g., piped water, borehole, rainwater, vendors, surface water, etc.).
  - Q5: Source use by purpose (for each source type: dug well, piped Kiwasco water, borehole, water from spring, rainwater, tanker truck, water from vendor, surface water) and for each purpose (drinking, cooking, washing, etc.). For each combination, record why the household uses that source using the provided codes (1–7: cost, safety, reliability, access, quantity, taste/color, other).
  - Groundwater2030: Codes for why a source is used (1 cost/price; 2 water quality/safety; 3 always available; 4 ease of access; 5 quantity; 6 taste/odor/color; 7 other).

  - Q1 (toilet facilities): Type of toilet used by household (options include flush/ pour-flush, pit latrine, composting, bucket, hanging toilet, no facility, other).
  - Q2: Household ownership of selected items (clock, electricity, television, non-mobile phone, refrigerator) with Yes/No/Don't know.
  - Q3: Main cooking fuel (electricity, LPG/natural gas, biogas, kerosene, coal/lignite, charcoal, wood, straw/shrubs/grass, agricultural/animal dung, no cooking, other).
  - Q4: Cooking location (in house, separate building, outdoors); if separate/outdoors, proceed to Q6.
  - Q5: Separate kitchen room present (Yes/No/Don't know).
  - Q6: Car or truck ownership (Yes/No/Don't know).

- PART 1 (socioeconomic and housing characteristics continued)
  - Q7: Main building material for walls (multiple material options; select observed main material).
  - Q8: Last 7 days main meals – days with meat, rice, and wheat products consumed.
  - Q9: Last 7 days – number of days cassava was the main meal.
  - Q10: In the last 30 days, how many days households did not have enough to eat.
  - Q11: In the last 12 months, how many months with at least one day without enough to eat.
  - Q12: Purchase frequency for staple foods (maize, maize meal, potatoes): Daily, Twice a week, Weekly, Fortnightly, Monthly, Less frequently than once a month.
  - Q13: How many weeks in the past 12 months the household stockpiled maize, maize meal, or potatoes.

- GIS relevance: key variables for spatial analysis
  - Location identifiers (area, Well ID) enable geocoding and map layers showing groundwater source usage and water safety practices.
  - Source-type and purpose data support layers on water-source dependence and potential contamination risk based on source mix.
  - Storage practices, toilet facilities, housing materials, and asset ownership provide socio-economic context for vulnerability mapping and service delivery planning.
  - Food security indicators (days without enough to eat, months of insecurity) can be linked to water access and reliability analyses.
  - Temporal aspects (yesterday purchase, last 7 days, last 30 days, last 12 months) allow trend mapping when combined with repeat surveys.

- Data quality considerations
  - Self-reported responses subject to recall bias and misreporting.
  - Use of multiple-choice and “don’t know” options (coded 9) requires careful handling in GIS datasets.
  - Complex matrix (Q5) and multi-source for multiple purposes may yield incomplete or inconsistent responses; consider data cleaning and validation protocols.
  - Consent status and linkage to Well ID are critical for data traceability and ethical use.

- Integration and use in map-based products
  - Create layers for: water source types by household, safety practices, and storage methods.
  - Link Well ID to spatial coordinates to map groundwater use patterns around wells.
  - Overlay sanitation facilities, cooking fuel, and housing materials to assess environmental and health risk profiles.
  - Combine with micro-level socio-economic indicators and service-availability data for policy and program targeting.