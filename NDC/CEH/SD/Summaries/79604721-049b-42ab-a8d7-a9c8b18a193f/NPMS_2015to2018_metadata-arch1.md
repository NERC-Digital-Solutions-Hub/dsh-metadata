# National Plant Monitoring Scheme survey data (2015-2018)

- Purpose and scope
  - A habitat-based plant monitoring scheme designed by BSBI, CEH, Plantlife and JNCC.
  - Aims to provide annual indications of changes in plant abundance and diversity, detect changes in priority habitats, understand drivers of change, and contribute to UK biodiversity indicators (e.g., C7).
  - Volunteers collect plant community data and habitat attributes across small plots in 28 fine NPMS habitats (11 broad categories) throughout the UK, Isle of Man and Channel Islands.
  - Data are managed in a central CEH database and intended for public release and independent review.

- Key datasets and how they relate
  - locations_2015to2018.csv: Unique location identifiers and plot type (square or linear); links to sampling events.
  - sampleInfo_2015to2018.csv: Sampling events linked to location_id; includes survey_id, date_start, entered_sref and system, created_on, and creator_id.
  - sampleAttributes_2015to2018.csv: Additional attributes linked to samples (sample_id), with category (caption) and text_value.
  - occurrences_2015to2018.csv: Species occurrences per sample, with taxon information, dominant cover (domin), verification status (C/V/R), and sensitivity (for blurred records).
  - npmsHabitatLookup.csv: Static mapping between NPMS broad habitats and fine-scale habitats.
  - Links among files are through location_id (locations file) and sample_id (sampleInfo and sampleAttributes), with occurrences referencing sampleInfo.

- Data collection design and habitats
  - Habitat-based design using 28 fine NPMS habitats, aggregatable into 11 broad NPMS categories.
  - Plot types and sizes:
    - Square plots: 5x5 m (10x10 m in woodlands).
    - Linear plots: 1x25 m (for standing/water bodies, hedgerows, margins, etc.).
  - Plot selection and layout
    - Pre-selected plot locations within each kilometre square; aim to place plots in a representative mix of habitats.
    - Protocol A allows self-selected plots when pre-selected options are unavailable; plots should be relocatable and representative.
  - Survey levels
    - Wildflower Level: fewer target species.
    - Indicator Level: full target species set for habitat indicators; most robust.
    - Inventory Level: Indicator Level plus recording all other vascular plants present.
  - Plot types by habitat (examples)
    - Arable field margins; road verges; hedgerows; standing waters, rivers, ponds; springs/flushes; ponds and wetlands; coastal habitats; upland and montane habitats; rock outcrops; woodlands.

- Data recording and measurement
  - For every plotted hectare, record species present using the relevant NPMS species list.
  - Abundance is recorded as percent cover using the Domin scale (with defined category ranges).
  - Additional optional data include vegetation height, woodedness, aspect, slope, and management indicators (e.g., grazing intensity, mowing, herbicide use).
  - Support materials include a field species guide, NPMS Species Lists, and monitoring forms (photographs and sketches recommended to aid relocation).
  - Data input
    - Online data entry via npms.org.uk with species dictionary, date and location validation, and iRecord-based expert verification for notable records.
    - If online entry is not possible, paper forms can be mailed.

- Evidence Quality Assurance (EQA)
  - NPMS EQA process described with multiple publications and a project-wide framework.
  - QA elements include:
    - Peer-reviewed design and methods; methodological testing and field trials.
    - Clear habitat definitions and unbiased indicator species selection; expert review of core components.
    - Data input controls: standardized spatial dating, controlled terms, and geographic range checks.
    - Verification through the iRecord system for higher-level botanical records.
    - Model-based uncertainty estimation and robust statistical design to minimize bias.
    - Documentation and version control (Data Management Plan; PRINCE2 standards); archival of design documents.
  - Q&A framing (Q1–Q5) covers design review, risk management, uncertainty communication, bias avoidance, and document/version control.

- Using and sharing the data
  - Data are intended to be publicly available to enable independent review and reuse.
  - Outputs (newsletters, reports) are checked by scientists to ensure claims are evidence-based.
  - Researchers and monitoring scientists can access dataset documentation and guidance; data are designed to be discoverable with metadata.

- Access rights, responsibilities, and safety
  - Survey participants should respect land access rights, other users, and the environment.
  - Safety guidelines emphasize preparedness, risk assessment, working with a buddy when possible, reporting whereabouts, carrying a mobile phone and first-aid, and wearing appropriate gear.
  - Access rules vary by UK country; guidance outlines permissions and responsible conduct for England, Wales, Scotland, and Northern Ireland.

- How to implement and relocate plots over time
  - PLOTS SHOULD REMAIN FIXED FOR long-term monitoring to detect changes.
  - If habitat changes, use the appropriate habitat list at the time of the survey for consistency.
  - If plots fall outside NPMS habitats, continue surveying where possible to maximize data on habitat change.
  - If survey is interrupted or a participant withdraws, plots should be made available to others; multiple squares may be allocated with varying minimum frequencies (up to five-year intervals for some plots).

- Appendix 1: Habitat types (overview)
  - 28 fine NPMS habitats grouped into 11 broad categories (examples include Arable field margins, Bog and wet heath, Broadleaved woodland, Coast, Fresh water, Heathland, Lowland grassland, Marsh and Fen, Native pinewood and juniper scrub, Rock outcrops, upland grassland).
  - Each habitat has characteristic species lists and management considerations to guide field recording and habitat assignment.

- Domin Scale and measurement guidance
  - Domin scale details provided for percent cover (e.g., 1-10 scale with defined intervals) and for individual counts.
  - For 10x10 m plots, 1% cover corresponds to 1 m2; for 5x5 m plots, 1% coverage equates to 50x50 cm area.
  - Guidance clarifies how to interpret scattered versus clumped distributions and how to tally multiple individuals within plot units.