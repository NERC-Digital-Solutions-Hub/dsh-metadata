# UrineEvents.csv

## Overview
- Large dataset documenting urination behavior (squatting duration, frequency, and estimated volume) of Welsh Mountain ewes on two contrasting upland pastures.
- Relevant for nitrogen cycling in grazed pastures, including nitrate leaching and N2O emissions from urine patches.
- Data collected across four campaigns (Spring 2016, Autumn 2016, Spring 2017, Autumn 2017) with 30 ewes per campaign.

## Study sites and context
- Site 1: Semi-improved upland field (11.5 ha, 240–340 m asl) at Henfaes Research Centre; vegetation U4/MG6 (NVC).
- Site 2: Common grazing land on Carneddau mountains (495 ha, 322–943 m asl) in Snowdonia; vegetation H12 heath with patches of acid grassland.
- Ewes weighed 33.5–41.6 kg at deployments depending on site and season.
- Data linked to a linear relationship between squatting duration and urine volume established from penned sheep (PennedSheepWithTags.csv).

## Data collection and processing
- Equipment: Daily Diary (DD) tags attached to shorn hind area of ewes.
- Measurements: start time, frequency, and squatting duration detected via a Boolean algorithm.
- Urine event volume (Vol_Est) estimated from squatting duration using the referenced linear relationship.
- Data screening and filtering:
  - Excluded data from DD tags that failed (e.g., tag detachment).
  - Removed periods with no urination events for >2 consecutive days or irregularly spaced events (likely due to sensor attachment issues).
  - Filtered out urine events shorter than 1 second; minimum observed squatting duration was 1.9 s.

## Data structure and variables
- Site: SemiImproved or Unimproved upland pastures.
- Season: Spring or Autumn.
- Sheep: ID R1–R30 per campaign (some missing values; different sheep sets per site).
- Date, Time, DateTime: timestamp fields for each urination event.
- Duration: squatting duration in seconds (from accelerometers and Boolean analysis).
- Vol_Est: estimated urine event volume in milliliters (ml).

## Campaigns
- Campaign 1: Spring 2016, semi-improved upland field.
- Campaign 2: Autumn 2016, semi-improved upland field.
- Campaign 3: Spring 2017, unimproved montane grazing area.
- Campaign 4: Autumn 2017, unimproved montane grazing area.

## Quality, usage, and applications
- Final filtered and cleaned dataset; notes on data quality include missing values and differences in sheep sets between sites.
- Data are suitable for assessing environmental health and nitrogen cycling impacts of urination in grazing systems.
- Useful for monitoring environmental policies and ecosystem nutrient dynamics over time.
- For data reuse, full citation is required; references to PennedSheepWithTags.csv provide the basis for volume estimation. Data should be stored and shared through appropriate portals.