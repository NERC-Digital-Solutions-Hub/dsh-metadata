# Soil protozoan diversity data from Sourhope field experiment site, Scotland, 1999-2000 [NERC Soil Biodiversity Programme]

- Context and aims
  - Data derive from the NERC Soil Biodiversity Thematic Programme (1999) focused on soil biodiversity and key ecological processes.
  - Site: Sourhope field experiment, Macaulay Land Use Research Institute (now James Hutton Institute) farm, Southern Scotland.
  - Primary aim: understand soil protozoan diversity and its functional roles in carbon and nitrogen turnover.
  - Scope: 24 projects within the programme; this dataset describes protozoan abundance and diversity.

- Site and sampling overview
  - Location characteristics: upland temperate grassland, base-poor damp soils, shallow brown soils, pH 4.54–4.81, mean soil carbon ~7.61%, nitrogen ~0.56%.
  - Vegetation aligned with National Vegetation Classification; Agrostis capillaris dominant.
  - Experimental design: 5 replicate blocks with 6 main plots each (30 main plots total), across downslope environmental gradients (slope 4–7°).
  - Stock exclusion since April 1998.
  - Sampling timeline: March 2, May 4, July 7, September 7, 1999 and July 17, 2000 (six occasions total).

- Protozoa sampling and lab methods
  - Core sampling: three 4.8 cm diameter, 5 cm depth cores per plot per occasion; samples processed to create air-dried soil for incubation.
  - Testate amoebae and naked amoebae/flagellates, ciliates/flagellates enumerations performed through incubation and staining/enumeration in controlled conditions at 15 °C.
  - Abundance expressions: quantities per gram oven-dried soil (or per gram dry weight for certain fractions); multiple enumeration approaches (direct, indirect, averages) used for flagellates.
  - Laboratory setting: Centre for Ecology & Hydrology, Windermere, Cumbria.

- Data structure and datasets
  - Dataset 1050: All Protozoa Abundance July 2000
    - 25 plots (sub-plot S of plot 4D) on 17 July 2000.
    - Variables include BLOCK, MAIN_PLOT, TREATMENT, SUID, sampling date, and protozoan counts (naked amoeba, flagellates direct/indirect, average, testate amoeba live/empty, ciliates, etc.).
    - Units: thousands per gram dry weight or per gram dry weight, depending on variable.
  - Dataset 1051: All Protozoa Abundance (P2130_PROTOZOA_ABUNDANCE.csv)
    - Six sampling occasions (Mar 1999–Feb 2000) across 25 plots.
    - Similar variables as 1050 but across multiple dates; includes NAKED_AMOEBA, FLAGELLATES_DIRECT/INDIRECT/AVERAGE, TESTATE_AMOEBA_LIVE/EMPTY, CILIATES.
  - Dataset 1052: Protozoa Species Size Distribution (P2130_PROTOZOA_SPECIES_SIZE.csv)
    - Average numbers by protozoan size class (12 size classes) for naked amoebae, flagellates, testate amoebae, and ciliates; includes species counts where applicable.
  - Dataset 1053: Protozoa Size Distribution (P2130_PROTOZOA_SIZE_DIST.csv)
    - Enumeration by size class for naked amoebae, flagellates, testate amoebae, and ciliates; six sampling occasions across 25 plots.
  - Dataset 1054: Protozoan species diversity by plot (130_PROTOZOAN_SPEC_DIVERSITY.csv)
    - Presence/absence and diversity indicators by plot:
      - PROTOZOAN_GROUP, GENUS, SPECIES, SPECIES_OCCURRENCE (present/not), NUMBER_OF_PLOTS (where detected).
    - Includes block and main plot metadata.

- Data quality and provenance
  - Quality control: numeric range checks, formatting checks, and logical integrity checks applied.
  - Note: NERC provides the data without warranty of accuracy or fitness for a specific use; no liability for misuse or outcomes.

- Practical notes for data use
  - The datasets are structured for cross-dataset joins using keys such as BLOCK, MAIN_PLOT, TREATMENT, sampling date, and SUID identifiers.
  - Suitable for data products enabling self-service exploration of protozoan abundance, size distribution, and species diversity across plots and over time.
  - Potential analyses include comparing protozoan groups across treatments, assessing temporal dynamics, and exploring size-structure vs. plot-level diversity.

- Reference and further reading
  - Related publications and data handbook entries are listed (e.g., Finlay et al. 2000; Sourhope Field Data Handbook 2003; Usher et al. 2006) for methodological context and data interpretation.