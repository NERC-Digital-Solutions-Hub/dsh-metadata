# Paternity of Eschscholzia californica plants introduced to habitats comprising different floral cover

## Purpose and study context
- Details paternity of progeny from Eschscholzia californica plants introduced to habitats with contrasting floral cover.
- Part of a larger experiment examining how floral resources shape pollination services to isolated plants.
- Field site: Hillesden estate, Buckinghamshire, UK; study conducted in June 2015.

## Experimental design
- Four 100-ha replicate blocks; sixteen experimental arrays total.
- Each array contains three E. californica plants separated by 1 m, arranged in a triangle.
- Within each block, four arrays positioned along a 150 m transect across the boundary between florally rich habitat and florally poor habitat (bare/fallow ground or grazed grassland): two arrays in rich habitat and two in poor habitat.
- Plants genotyped prior to deployment; 48 plants with distinct genotypes deployed across the landscape.

## Methods

### Genotyping and plant preparation
- Plants grown from seed and genotyped at seven microsatellite loci.
- DNA extracted from leaf tissue; PCR amplified seven loci; fragment analysis performed; alleles scored.
- Ambiguous alleles validated by cloning and sequencing.
- Selection of 48 plants with distinct genotypes; triplets within arrays arranged so that, where possible, plants were homozygous at a locus but carried different alleles across arrays.

### Field deployment and data collection
- Open flowers removed; one bud per plant covered with muslin to simulate pollinator exclusion.
- Field exposure lasted 16 days to allow full anthesis and multiple pollination events.
- Fruits labeled to ensure only offspring from the field period were included.
- Seeds collected (~10 per plant) and stored until maturation under controlled glasshouse conditions.

### Progeny sampling and paternity analysis
- Genotyped approximately ten progeny per field-exposed plant (mean ~9.5).
- Selfing vs outcrossing determined by comparing progeny genotypes to maternal genotype across seven loci.
- Paternity assigned using Cervus 3.0.7, incorporating delta score (∆) and a 95% confidence threshold for trio matches.
- Paternity outcomes recorded with habitat of pollen movement and distance travelled.

## Data structure and contents
- Single CSV file: Paternity_analysis_of_introduced_Eschscholzia_californica_plants.csv
- Key columns:
  - Block (replicate block identifier)
  - Experimental_array (array identifier within a block)
  - Plant_identification_number (individual plant ID)
  - Fruit_number (offspring sample ID; 'Maternal' for maternal samples)
  - Habitat and Treatment (location context)
  - Sample_identification (sample IDs; progeny vs maternal)
  - Loci columns (lociX_AlleleY for seven loci; NA for failed amplification)
  - Parentage (manual paternal assessment)
  - Paternity_analysis (Cervus-derived paternal ID; '?' if confidence <95%)
  - Distance_of_pollen_movement (in meters)
  - Habitat_crossed (habitat type pollen crossed between)

## Measurements and outputs
- Selfing vs outcrossing rates per habitat.
- Paternity assignments and associated confidence levels.
- Distances moved by pollen between maternal and paternal plants.
- Context of pollen movement across florally rich vs poor habitats.

## Data quality, provenance, and access
- Dataset described as complete, with detailed collection and analytical protocols.
- Data collected and interpreted by T.M. Evans.
- Metadata includes block, array, habitat, and sample identifiers to support discoverability and reuse; NA entries denote missing amplification or undetermined paternity.