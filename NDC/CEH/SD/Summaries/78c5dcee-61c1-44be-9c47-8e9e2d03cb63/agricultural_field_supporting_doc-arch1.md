# Rural smallholder agricultural field surveys across Mozambique: supporting documentation

- A structured dataset comprising 259 smallholder field surveys from 26 villages across three districts in Mozambique (Mabalane in Gaza, Marrupa in Niassa, Gurue in Zambezia).
- Collected through the ESPA-funded ACES project to understand how land-use changes affect soil fertility, ecosystem services, and rural livelihoods.

## Study scope and timeline

- Villages: 26 total, selected to cover gradients of land-use intensity (charcoal production, subsistence agriculture/forest extraction, and smallholder commercial agriculture).
- Fields: 10 active fields per village (total 259 fields sampled), with owner consent and GPS-mapped perimeters.
- Survey periods:
  - Mabalane District: May–September 2014
  - Marrupa District: May–August 2015
  - Gurue District: September–December 2015
- Field selection aimed for active fields (no current fallows) with known ownership, varying field ages, and location within village boundaries.

## Data collection methods and instrumentation

- Interview format: Structured questionnaires administered in the local language; responses translated into Portuguese and then into English by the lead author.
- Field measurements:
  - Field locations and perimeters recorded with Garmin GPS devices.
  - Data collected on Android tablets using ODK software.
- Data collection team: Trained interviewers with local knowledge; data quality monitored by the lead author.
- Data linkage: Each field across all datasets uses a common field_id to link records.

## Data structure and contents (12 datasets)

- field_main_survey: Core interview responses per field (date, location, area, management practices, crops, yields, fallow cycles, floods, pests, and qualitative observations).
- crops_planted: Crops normally planted in each field; crops planted in last year and in the first year (district-dependent).
- crop_yield: Quantitative yields for the most recent harvest; older yield data omitted due to recall unreliability; some fields recorded yields as count units (individuals).
- yield_unit_conversion: Unit conversions for crops to weight (kg) with source notes and uncertainties; conversions often highly uncertain.
- fertiliser_use: Types of fertilisers used, frequency, and extent of application.
- pesticide_use: Pesticide use data (collected only in Gurue district) and frequency.
- field_tilling: Tilling methods and frequency (hoe, ox plow, tractor, etc.).
- insect_pest: Local names of insect pests and their observed frequency.
- animal_pest: Local names of animal pests and their observed frequency.
- trees_on_field: Live tree species observed on fields at interview time.
- trees_before_cleared: Tree species present before field creation (only in Mabalane).
- indicator_species: Trees/ grasses used as indicators of good soil; includes indicator type (grass or tree) and species names.

- Field_id structure: Field identifiers encode village and field number; alignment across datasets is ensured via the field_id key.
- Data quality flags: Blanks indicate not recorded, not relevant, or unknown; -999 indicates unknown quantities or years.
- Temporal and district nuance: Some questions and data elements varied by district; presence/absence columns indicate district-specific inclusion.

## Notable methodological details

- Soil data: Soil samples were collected but not included in this dataset; soil data are referenced as separate by ACES projects.
- Yields: Emphasis on most recent harvest due to recall unreliability for earlier years; multiple yield-related fields exist to document units, conversions, and comments.
- Field age and history: Data include years since ownership, fallow periods (start/end), and signs of field expansion or land-use change; historical woodland presence before field creation is recorded where applicable.
- Data quality and limitations:
  - All data were quality assured by the lead author; translation and standardization procedures were employed to minimize ambiguity.
  - Unit conversions for yields are uncertain and should be treated as rough estimates; cross-dataset consistency relies on careful linking via field_id.

## Context and references

- Data collected to understand how land-use changes impact soil carbon and nitrogen dynamics, ecosystem services, and rural livelihoods in Mozambique.
- References include works on charcoal production, soybean cultivation, national agricultural surveys, and related land-use impact studies.