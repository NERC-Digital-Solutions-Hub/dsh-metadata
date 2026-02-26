# The purpose of the data is to compare the amount of a key pheromone between two sibling species of Drosophila.

## Objective
- Compare the amount of the pheromone 7,11-heptacosadiene (7,11-HD) between two Drosophila species: D. simulans and D. sechellia.

## Experimental design and samples
- Species and strains:
  - D. simulans (strain a2a2b; inbred line from Tsimbazaza)
  - D. sechellia (from Cousin Island, Seychelles)
- Sample size: 15 virgin females per species, kept with other females for 5 days before extraction.
- Handling: females anaesthetised on ice for 10 minutes prior to extraction.

## Extraction and preparation
- Extraction solvent: >99% pure hexane (150 μL) in a 200 μL glass vial with insert.
- Procedure: vortex for 2 minutes; evaporate hexane under a gentle nitrogen flow; store vials at -20°C until shipping.
- Internal standards: resuspend extracts in 50 μL of standard solution containing 10 ng/mL octadecane (C18) and 10 ng/mL hexacosane (C26) in hexane.

## Analytical methods
- Instrumentation: Agilent 7890 GC with flame ionization detector.
- Column and conditions: DB-1 column (diameter 0.180 mm, film 0.18 μm); splitless injector at 250°C; helium carrier gas (flow 37.2 cm/s).
- Temperature program: 50°C (1.5 min) → 150°C at 10°C/min → 280°C at 4°C/min; hold at 280°C for 5 min.
- Data processing: ChemStation software; identify 7,11-HD by retention time relative to C26; quantify by comparing peak area of 7,11-HD to the internal standard C26.
- Datasets: 711HDsech.csv (D. sechellia) and 711HDsim.csv (D. simulans); data organized with column 1 as ng per sample and column 2 as sample name.

## Data quality and notes
- Some samples failed to produce any traces and were excluded from analysis.
- Relative quantities reflect peak area comparisons to the internal standard (C26).

## Data provenance and collaboration
- Rearing and extractions conducted in Stephen Goodwin's lab (University of Oxford) by Deniz Erezyilmaz.
- Samples shipped to University of Groningen for GC analysis in J.C. Billeter's lab; analysis performed by Nicolas Dubovetsky.