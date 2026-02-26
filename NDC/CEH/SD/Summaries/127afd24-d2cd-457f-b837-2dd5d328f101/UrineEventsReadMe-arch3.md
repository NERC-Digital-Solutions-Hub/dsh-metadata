# UrineEvents.csv

## Overview
- Dataset on urination behaviour (squatting duration, frequency, and estimated volume) of Welsh Mountain ewes on two contrasting upland pastures.
- Aims align with environmental health monitoring by informing nitrogen cycling, nitrate leaching, and potential N2O emissions from urine patches.

## Data collection and instrumentation
- Ewes fitted with Daily Diary (DD) tags (Wildbyte Technologies Ltd., UK) attached to the hind area.
- Four campaigns: Spring 2016, Autumn 2016 (semi-improved upland field, n=30 per campaign); Spring 2017, Autumn 2017 (unimproved montane grazing area, n=30 per campaign).
- Sites:
  - Semi-improved upland field at Henfaes Research Centre (11.5 ha, 240–340 m asl) with grassland communities U4 and MG6.
  - Common grazing land in Snowdonia National Park (495 ha, 322–943 m asl) with heath vegetation (H12) and patches of acid grassland.
- Sheep weights at deployment varied by site and season.
- Data collected via DD tags, with events detected by a Boolean algorithm.

## Variables and data structure
- Site: SemiImproved or Unimproved upland pastures.
- Season: Spring or Autumn.
- Sheep: ID R1–R30 per campaign (some missing values due to tag issues; different sheep sets between sites).
- Date, Time: Date and start time of urine events.
- DateTime: Combined timestamp.
- Duration: Squatting duration (seconds) from accelerometer data.
- Vol_Est: Estimated urine event volume (ml) derived from a linear relationship with squatting duration (established from a penned-study with tagged sheep).

## Data processing and quality control
- Urine events identified using a Boolean algorithm; duration and frequency extracted.
- Volume estimates based on a linear relation from PennedSheepWithTags.csv.
- Dataset represents final filtered and cleaned data.
- Data cleaning steps:
  - Removal of initially unsuccessful tags (e.g., tags falling off).
  - Filtering unreliable days where no urination events were detected for >2 consecutive days or irregularly interspersed events.
  - Filtering out urine events with duration < 1 second (noise); the minimum observed squatting duration in the study was 1.9 seconds.
- Some missing values occur ( Sheep IDs not present for all campaigns/sites ) due to tag issues.

## Data quality and limitations
- Gaps due to tag failures and detachments; missing data across campaigns and sites.
- Potential sensor attachment issues caused by wool growth or movement, affecting reliability.
- Differences between sites in sheep sets and environmental conditions may affect comparability.
- Volume estimation relies on a linear relationship from a separate Penned study; applicability to field conditions depends on context.

## Metadata and provenance
- Campaigns, sites, vegetation classifications, and sheep weights documented.
- Data headers and units described in the dataset.
- Linked data: PennedSheepWithTags.csv contains the data underpinning the volume estimation model; this is referenced for reproducibility.
- Clear instruction to cite the dataset if reused.

## Data sharing and governance considerations
- The dataset is described as final, cleaned, and ready for dissemination, with metadata and unit definitions included to aid reuse.
- Transparency achieved through explicit data cleaning criteria and event filtering rules.
- Public sharing of underlying data and metadata is acknowledged as a governance consideration in the monitoring-framework context.

## End use and applications for monitoring frameworks
- Supports evaluation of nitrogen cycling and potential N2O emissions from urine patches in grazed ecosystems.
- Provides measurable inputs (urination frequency, duration, and estimated volume) for environmental health monitoring, modeling, and policy evaluation.
- Demonstrates data governance practices: traceable data cleaning, documentation of methods, and linkage to supplementary datasets for model parameters.