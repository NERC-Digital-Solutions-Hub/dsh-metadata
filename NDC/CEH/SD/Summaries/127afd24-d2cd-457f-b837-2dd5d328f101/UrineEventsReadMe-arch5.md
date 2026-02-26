# UrineEvents.csv

## Dataset overview
- Large dataset describing urination behavior of Welsh Mountain ewes across two contrasting upland pastures in Wales, UK.
- Relevant to nitrogen cycling in grazed ecosystems (nitrate leaching and N2O emissions) due to urine patches.
- Data collected from four campaigns (spring/autumn 2016 and 2017) with 30 sheep per campaign.
- Data are the final filtered and cleaned records; some DD tags were removed due to deployment issues.

## Data collection context
- Monitoring device: Daily Diary (DD) tags attached to a shorn area on the hind of each ewe.
- Sites:
  - Semi-improved upland pasture (Henfaes Research Centre, 11.5 ha, 240–340 m asl)
  - Unimproved montane grazing area (Carneddau, Snowdonia National Park, 322–943 m asl)
- Vegetation classifications:
  - Site 1: U4 and MG6 NVC communities
  - Site 2: H12 heath with patches of acid grassland
- Sheep weights at deployment start:
  - Semi-improved site: spring 33.5 ± 1.2 kg; autumn 39.7 ± 1.1 kg
  - Unimproved site: spring 41.6 ± 0.9 kg; autumn 38.0 ± 0.7 kg
- Data processed with a Boolean algorithm to detect start time, frequency, and squatting duration; urine event volume estimated from squatting duration using a linear relationship derived from pens with tagged sheep.

## Data processing and quality control
- Final dataset after filtering and cleaning.
- Quality control filters:
  - Excluded DD tags that failed (e.g., detached early).
  - Removed urination days with zero events for two consecutive days or irregular gaps (likely due to sensor attachment issues).
  - Filtered out urine events with duration under 1 second as noise (shortest observed 1.9 s in penned study).
- Handling of missing data:
  - Missing values present due to tagging issues and campaign variation; different sets of sheep used per site.
- Data dependencies:
  - Volume estimates (Vol_Est) derived from squatting duration using a regression model linked to PennedSheepWithTags.csv.

## Data fields and definitions
- Site: SemiImproved or Unimproved upland pasture.
- Season: Spring or Autumn at each site.
- Sheep: ID R1–R30 per campaign (note missing values due to tagging issues).
- Date: Date of urine event (dd/mm/yyyy).
- Time: Start time of urine event (hh:mm:ss).
- DateTime: Combined date and time (dd/mm/yyyy hh:mm:ss).
- Duration: Urination squatting duration (seconds) as recorded by DD tags.
- Vol_Est: Estimated urine event volume (ml) derived from duration via regression model.
- Reference note: PennedSheepWithTags.csv contains data used to establish the duration–volume relationship.

## Provenance and versioning
- Four campaigns documented with specific date ranges per campaign.
- Tags and sheep allocation varied by site; some data loss due to tag detachment.
- Documented criteria for data cleaning and filtering to ensure reliability.

## Data storage, sharing, and reuse
- Data is provided as UrineEvents.csv with explicit data cleaning steps and quality criteria.
- Data usage note: If reused, dataset must be fully cited.
- Related dataset: PennedSheepWithTags.csv contains the regression data used to estimate urine volume.

## Governance considerations for Data Stewards
- Metadata completeness:
  - Ensure clear definitions for each field, units, and data processing steps.
  - Record site characteristics, campaign periods, and sheep cohorts for reproducibility.
- Data quality management:
  - Maintain filtering criteria (e.g., thresholds for reliability of daily events, minimum duration).
  - Document tag performance issues and reasons for data exclusion.
- Interoperability and standards:
  - Maintain consistent field naming, date/time formats, and units across datasets.
  - Link to calibration data (PennedSheepWithTags.csv) and provide provenance traces for the duration–volume model.
- Access and licensing:
  - Ensure reuse citations are provided; clarify any embargoes or access restrictions.
  - Consider depositing in a data portal with metadata and DOI for discoverability.
- Updates and version control:
  - Track any reprocessing or corrections; maintain a changelog.
  - Plan for future updates if additional campaigns or improved tagging methods are introduced.
- User needs alignment:
  - Preserve metadata that explains assumptions (e.g., linear volume estimation) to support appropriate reuse in nitrogen cycling studies.