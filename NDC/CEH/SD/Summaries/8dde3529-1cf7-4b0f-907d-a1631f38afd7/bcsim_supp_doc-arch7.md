# To identify loci that contribute to discrimination between males of related species

## Overview
- Study aims to identify genomic loci that differentiate male mating discrimination between Drosophila simulans and D. sechellia.
- Uses female progeny from a D. simulans backcross (F2 from an F1 backcross to D. simulans) in a two-choice mating assay.
- Genomic genotyping and subsequent data processing underpin locus-level analysis.

## Experimental design
- Adult flies sexed at eclosion and kept in same-sex groups of three per vial.
- Test subjects: three females and three males of either species, all eclosed the same day.
- Two-choice mate assay monitored for up to four hours or until copulation occurs.

## Data collection and sequencing
- When the first mating occurs, vial is frozen (-20°C) and the copulating male’s species is determined by inspecting male genitalia (distinct between species).
- Illumina sequencing libraries prepared using standard molecular biology methods (as described in Andolfatto et al., 2011).

## Data structure and fields
- ID: library ID followed by a unique barcode.
- pheno: 0 = females mated with D. simulans males; 1 = females mated with D. sechellia males.
- Remaining columns: specific genomic locations in the D. simulans genome (Hu et al., Genome Res. 2013; 23: 89-98).

## Genotypes and parental references
- Parental genomes: D. simulans A2A2B (from Tsimbazaza strain) and D. sechellia D1A1C (from D. sechellia 13 strain).

## Genotyping method and data processing
- Genotypes obtained by Multiplexed Shotgun Genotyping (Andolfatto et al., 2011).
- Data thinned using pull_thin (David Stern’s script).
- In cases of low DNA content leading to incomplete calls, individuals with more than 25% ambiguous calls (NA) removed.

## Data coding
- BB = sim/sim alleles
- BA = sech/sim
- NA = data not available

## References
- Andolfatto, P., et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping. Genome Res. 2011.
- Hu, T.T., Eisen, M.B., Thornton, K.R., Andolfatto, P. A second-generation assembly of the Drosophila simulans genome. Genome Res. 2013.