# The purpose of the data is to compare the amount of a key pheromone between two sibling species of Drosophila.

## Overview
- Objective: Compare levels of the pheromone 7,11-HD between two sibling Drosophila species.
- Sample size: 15 female individuals per species.
- Species/strains: D. simulans (inbred line a2a2b from Tsimbazaza) and D. sechellia (line 13 from Cousin Island, Seychelles).
- Female preparation: Virgins isolated, kept with other females for five days before extraction.

## Sample collection and preparation
- Anesthesia: Females anesthetised on ice for 10 minutes.
- Extraction solvent: 150 μL of >99% pure hexane in a 200 μL glass vial with insert.
- Extraction procedure: Vortex at lowest speed for 2 minutes; nitrogen flow used to evaporate hexane after removal of the female.
- Storage: Vials stored at -20°C until shipping.
- Internal standard: 50 μL of solution containing 10 ng/mL octadecane (C18) and 10 ng/mL hexacosane (C26) in hexane.

## Analytical methodology
- Instrumentation: Agilent 7890 GC with flame ionization detector (FID).
- Column: DB-1, 0.180 mm diameter, film 0.18 μm.
- Injector: Splitless, 250 °C; carrier gas: helium.
- GC program: 50 °C (1.5 min) → 150 °C at 10 °C/min → 280 °C at 4 °C/min, hold 5 min.
- Data processing: ChemStation; peaks integrated relative to internal standard C26; method based on Krupp et al. (2008).
- Compound identification: 7,11-HD identified by retention time relative to C26.
- Quantification: relative quantity in ng based on peak area of 7,11-HD compared to area of the known quantity of C26.
- Data quality note: samples that produced no traces were excluded from analysis.

## Data structure and datasets
- Datasets: 711HDsech.csv (D. sechellia) and 711HDsim.csv (D. simulans).
- Organization: information arranged by ng (column 2) per sample (column 1).
- Output: quantified 7,11-HD in ng; samples with no traces removed from dataset.

## Provenance and data handling
- Rearing and extractions: Stephen Goodwin's lab, University of Oxford; performed by Deniz Erezyilmaz.
- Shipping and analysis: Samples shipped to University of Groningen for GC analysis in J.C. Billeter's lab; analysis conducted by Nicolas Dubovetsky.
- Data integration: Quantification anchored to internal standard (C26); cross-referenced with retention time relative to C26.

## Quality considerations and limitations
- Data completeness: some samples excluded due to missing traces.
- Data organization: results stored in separate species-specific CSV files with ng-based quantification.
- Reproducibility: method aligns with Krupp et al. (2008) and uses a standardized internal standard approach to enable comparison across samples.