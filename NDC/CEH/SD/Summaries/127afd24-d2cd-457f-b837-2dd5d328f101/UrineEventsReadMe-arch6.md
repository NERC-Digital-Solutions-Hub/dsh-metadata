# UrineEvents.csv

## Overview
- Large dataset detailing urination behaviour (squatting duration, frequency, estimated volume) of Welsh Mountain ewes on two contrasting upland pastures in Wales, UK.
- Relevant to nitrogen cycling in grazed pasture ecosystems (nitrate leaching and N2O emissions) due to urine patches.
- Collected across four campaigns: Spring 2016 (semi-improved site), Autumn 2016 (semi-improved), Spring 2017 (unimproved montane), Autumn 2017 (unimproved montane).
- Each campaign involved 30 ewes.

## Study Sites and Subjects
- Site 1: Semi-improved upland field, Henfaes Research Centre, 11.5 ha, 240–340 m asl; vegetation: NVC U4 and MG6.
  - Mean starting weights: Spring 33.5 ± 1.2 kg; Autumn 39.7 ± 1.1 kg.
- Site 2: Unimproved montane grazing area, Carneddau (Snowdonia National Park), 495 ha, 322–943 m asl; vegetation: NVC H12 heath with patches of acid grassland.
  - Mean starting weights: Spring 41.6 ± 0.9 kg; Autumn 38.0 ± 0.7 kg.

## Data Collection and Processing
- Data collected with Daily Diary (DD) tags glued to the hind of ewes.
- Measurements detected by a Boolean algorithm: start time, frequency, and squatting duration of urination.
- Urine event volume (Vol_Est) estimated from squatting duration using a linear relationship established from penned sheep with DD tags (reference to PennedSheepWithTags.csv for underlying regression).

## Campaigns and Data Coverage
- Campaign 1 (Spring 2016): Ewes n = 30 at semi-improved site (May 12, 2016 – June 16, 2016).
- Campaign 2 (Autumn 2016): Ewes n = 30 at semi-improved site (Sept 2016 – Nov 3, 2016).
- Campaign 3 (Spring 2017): Ewes n = 30 at unimproved montane site (May 31, 2017 – July 5, 2017).
- Campaign 4 (Autumn 2017): Ewes n = 30 at unimproved montane site (Sept 18, 2017 – Oct 28, 2017).

## Data Cleaning and Quality
- Final filtered and cleaned dataset; some DD tags removed due to early detachment (e.g., sheep rubbing hind on trees/posts).
- Urination data filtering:
  - If zero urination events occurred on several consecutive days (more than two days in a row) or irregularly, data considered unreliable and removed.
  - Urine events with duration < 1 second removed as noise (shortest observed in pen study was 1.9 s).
- Note: Different sets of sheep were used between the two sites; missing values present.

## Data Schema and Units
- Headers and meaning:
  - Site: SemiImproved or Unimproved upland pastures.
  - Season: Spring or Autumn.
  - Sheep: ID (R1–R30 per campaign); some missing values due to removals.
  - Date: Date of urine event (dd/mm/yyyy).
  - Time: Start time of urination (hh:mm:ss).
  - DateTime: Combined date and time (dd/mm/yyyy hh:mm:ss).
  - Duration: Squatting duration (seconds) as recorded by accelerometers and analyzed by the Boolean algorithm.
  - Vol_Est: Estimated urine event volume (ml) derived from squatting duration (linear relationship from PennedTag data).

## Use and Citation
- Data intended to support understanding of urine patches’ role in nitrogen cycling and related emissions in grazing systems.
- For reuse, ensure full citation of the dataset.
- Underlying regression used to estimate Vol_Est is documented in PennedSheepWithTags.csv within the same deposited dataset.