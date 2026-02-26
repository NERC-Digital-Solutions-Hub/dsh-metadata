# UrineEvents.csv

## Dataset overview
- Large dataset detailing urination behaviour (squatting duration, frequency, and estimated volume) of Welsh Mountain ewes on two contrasting upland pastures.
- Implications for nitrogen cycling in grazed pasture ecosystems, including nitrate leaching and N2O emissions from urine patches.
- Data collected from four campaigns (two sites, spring/autumn; 2016–2017).

## Study design and subjects
- Subjects: 30 ewes per campaign, across two sites; different sets of 30 sheep used at each site.
- Sites:
  - Semi-improved upland pasture (Henfaes Research Centre, 53°13′N, 4°0ʹW; 11.5 ha; 240–340 m a.s.l.; vegetation: NVC U4 and MG6).
  - Unimproved montane grazing area (Carneddau, Snowdonia National Park, 322–943 m a.s.l.; vegetation: NVC H12 heath with patches of acid grassland).
- Campaigns:
  - Campaign 1: Spring 2016, semi-improved site
  - Campaign 2: Autumn 2016, semi-improved site
  - Campaign 3: Spring 2017, unimproved site
  - Campaign 4: Autumn 2017, unimproved site
- Sheep characteristics: mean weights at start ~33.5 kg (spring) and ~39.7 kg (autumn) at semi-improved site; ~41.6 kg (spring) and ~38.0 kg (autumn) at unimproved site.

## Data collection and processing
- Data collection: Daily Diary (DD) tags (Wildbyte Technologies Ltd.) attached to a shorn hind area of each ewe.
- Measurements captured: urination start time, frequency, squatting duration; urine event volume estimated from squatting duration using a linear relationship derived from penned sheep.
- Processing:
  - Boolean algorithm used to detect start time, frequency, and duration of urination events.
  - Volume estimation (Vol_Est) derived from squatting duration via the established linear regression.
  - Final dataset is filtered/cleaned; some tags removed due to early failure (e.g., detachment from rubbing).
  - Urination data quality filters:
    - Days with zero urination events for more than two consecutive days or irregular patterns flagged as unreliable and removed.
    - Urine events shorter than 1 second removed as noise.
    - Shortest directly observed squatting duration in the study with penned sheep was 1.9 s.
- Related data: PennedSheepWithTags.csv contains the data underpinning the duration–volume regression used for Vol_Est.

## Data fields and units
- Site: SemiImproved or Unimproved (upland pastures).
- Season: Spring or Autumn.
- Sheep: ID R1–R30 for each campaign; missing values present due to tag/attendance issues.
- Date: dd/mm/yyyy (urination event date).
- Time: hh:mm:ss (start time of urination event).
- DateTime: dd/mm/yyyy hh:mm:ss (combined timestamp).
- Duration: squatting duration (seconds).
- Vol_Est: estimated urine event volume (ml) calculated from squatting duration.

## Data quality, limitations, and governance
- Data quality notes:
  - Some tags removed due to early detachment or sheep rubbing hind area.
  - Data gaps where different sheep sets were used between sites.
  - Potential sensor attachment issues from wool growth or tag stability.
- Limitations:
  - Different management and environmental conditions between sites; results may reflect site-specific factors.
  - Volume estimates rely on regression from penned sheep and may introduce uncertainty when applied to free-range conditions.
- Reuse and citation:
  - If data are reused, ensure full citation of the dataset.
  - Grant: NE/M015351/1; authors listed (Marsden, Lush, Holmberg, Harris, Whelan, Webb, King, Wilson, Jones, Charteris, Cardenas, Chadwick, etc.).
  - Related dataset PennedSheepWithTags.csv provides underlying regression data for Vol_Est.