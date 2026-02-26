# Introduction The National Plant Monitoring Scheme (NPMS) is a new habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC.

## Overview and Aims
- Purpose: collect data to indicate annual changes in plant abundance and diversity, monitor habitat quality, understand drivers of change, and contribute to UK Biodiversity indicators.
- Scope: volunteer-based plant recording across 28 NPMS habitats (grouped into 11 broad categories) in the UK, Isle of Man, and Channel Islands.
- Outputs: annually updated dataset held at CEH Wallingford; aims to support policy, research, and public communication about habitat condition.

## Data Files Provided (2015–2018)
- locations_2015to2018.csv (location_id, location_type) — unique sampling locations and plot types.
- sampleInfo_2015to2018.csv (id, survey_id, date_start, location_id, entered_sref, entered_sref_system, created_on, created_by_id) — sampling events per location.
- sampleAttributes_2015to2018.csv (sample_attribute_id, sample_id, caption, text_value) — additional attributes linked to samples.
- occurrences_2015to2018.csv (id, sample_id, taxonversionkey, preferred_taxon, domin, record_status, sensitivity_precision) — species occurrences with abundance and verification status.
- npmsHabitatLookup.csv (NPMS_broad_habitat, NPMS_fine-scale_habitat) — static habitat category mappings for convenience.

## Data Model and Linkages
- Location table links to sampleInfo via location_id.
- SampleInfo links to sampleAttributes and occurrences via sample_id/id.
- Occurrences include taxon keys, names, abundance (Domin scale), verification status (C/V/R), and sensitivity for blurred records.
- Habitat lookup provides mapping between fine and broad habitat categories.

## Field Protocols and Data Collection
- Habitats and plots:
  - 28 fine NPMS habitats (11 broad categories).
  - Plots: square 5x5 m (woodlands 10x10 m); linear plots 1x25 m.
  - Two main survey levels: Wildflower, Indicator, and Inventory (with increasing species lists and robustness).
- Plot selection and relocation:
  - Prefer plots within pre-selected locations, but self-selection (Protocol A) allowed to represent habitat; ensure plots are relocatable in future years.
  - Emphasis on recording a diverse set of habitats across a kilometre square when possible.
- Data entry and documentation:
  - Data entered online at npms.org.uk; or post forms if online entry is not possible.
  - Each plot requires a field sketch, compass direction, GPS coordinates (optional, supports relocation), and up to two photos per plot.
  - Spatial references use entered_sref and entered_sref_system (OSGB, Irish Grid, WGS84).
- Plot specifics:
  - Square plots: 5x5 m (10x10 m in woodlands); linear plots: 1x25 m.
  - Ponds/flushes treated as linear plots; where applicable, multiple plot types may be used to maximize habitat representation.
  - Recording intensity within plots follows a consistent search approach to capture all present species.
- Data recording details:
  - Abundance: percentage cover for each species using the Domin scale.
  - Additional optional data: vegetation height classes, woodedness, aspect, slope, and management signs.
  - For arable margins, road verges, hedgerows, standing waters, springs, and other habitats there are specific plotting guidelines (e.g., margins extend 1 m into cultivated area; rivers/streams surveyed from bank; etc.).
- Handling of missing or changed habitats:
  - If habitat changes over time, continue using the current habitat’s species list at the time of each survey; if plots leave NPMS habitats, continue surveying where possible to track changes.

## Evidence Quality Assurance (EQA)
- EQA basis: peer-reviewed articles and project reports underpinning NPMS design and data handling.
- Core QA elements:
  - Sample design and plot selection reviewed by statisticians; randomization with respect to landscape to avoid bias.
  - Habitat definitions and target species lists subjected to expert review; field recording uses three engagement levels to accommodate volunteer expertise.
  - Data input validation: online capture with a species dictionary, calendar dates, map-based locations, and controlled terms; automated geographic checks; iRecord verification for taxonomic reviews.
  - Uncertainty and biases addressed through robust statistical design; results checked by scientists before publication.
  - Documentation and version control: all design outputs tracked, with versioned reports archived and backed up off-site per a CEH Data Management Plan aligned with PRINCE2 standards.
- Governance:
  - Project overseen by a Steering Group; external peer review engaged where risk is higher (e.g., survey design).
  - Outputs (newsletters, reports) reviewed by scientists to ensure claims are evidence-based.

## Data Access, Sharing and Outputs
- Data publishing: data from NPMS will be made publicly available to enable independent review.
- Data use: supports researchers, volunteers, policy-makers, and the public; disseminated via NPMS newsletters and peer-reviewed publications.
- Support: user help available via NPMS support channels; non-online data can be mailed in.

## How Outputs Communicate Uncertainty and Limitations
- Outputs are reviewed to ensure claims are supported by evidence; uncertainty is addressed through statistical modelling and explicit methodology.
- Data users are encouraged to consult EQA publications alongside guidance documents for interpretation.

## Data Governance, Rights and Safety
- Access rights reflect UK country-specific guidelines (England/Wales, Scotland, Northern Ireland).
- Volunteers are advised to obtain permission for private land and to follow countryside/access codes; safety guidelines emphasize personal responsibility, buddy systems, weather checks, and risk mitigation.
- Data management emphasizes clear documentation, version control, and secure backups.

## Appendix: Habitat Classification (Brief)
- 28 fine NPMS habitats organized into 11 broad categories (e.g., Arable field margins; Bog and wet heath; Broadleaved woodland; Coastal habitats; Fresh water; Heathland; Lowland grassland; Marsh and Fen; Native pinewood and juniper scrub; Rock outcrops; Upland grassland).
- Domin Scale: 10-step percent-cover scale used to quantify abundance (and guidance for interpreting 1% increments in various plot sizes).
- Habitat descriptions provide guidance for selecting the appropriate fine habitat or broad category when recording.

## Contacts and Support
- Support and data entry assistance via NPMS channels; documented guidelines and sample forms available on the NPMS website.