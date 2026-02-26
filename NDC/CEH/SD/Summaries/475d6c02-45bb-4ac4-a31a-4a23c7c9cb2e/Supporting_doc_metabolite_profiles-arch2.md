# Supporting Documentation for Untargeted metabolomic profiles of paired cultures of four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA.

- This dataset comprises untargeted metabolomic profiles from paired cultures of four interacting Streptomyces strains isolated from a Minnesota nature reserve.
- Daily samples were collected from day 2 to day 6 in triplicate, with quadruplicate pairings to enable metabolite and RNA sampling.
- Metabolites were extracted using cold methanol and analyzed by LC-MS in both positive and negative ionisation modes.
- The deposited data are raw LC-MS files converted to open-source mzML format, including mass-to-charge (m/z), elution time, and ion counts, to study how metabolism changes in response to neighboring strains.

## Data formats and file naming

- File format: .mzML (open-source raw LC-MS data).
- Contents: mass spectral data (m/z, ion counts, elution times) and metadata (instrument, mode).
- Naming convention: [n/p] - [2/3/4/5/6] - [A/B/C/D/agar] - [1/2/3]
  - n/p indicates negative or positive ionisation mode.
  - 2–6 indicates days post inoculation.
  - A/B/C/D/agar denotes the sampled strain and the neighbouring cultured strain; "agar" indicates background controls with no microbes.
  - 1/2/3 is the replicate number.
- Related outputs: analyzed peak datasets are available in a separate deposit.

## Organism Culturing and experimental design

- Bacterial spores standardized to 1 x 10^9 CFU/mL in 20% glycerol; diluted to 1 x 10^8 CFU/mL in ISP2 broth.
- 4 μL inoculated 1 cm apart in pairs on ISP2 agar; each pairing prepared in quadruplicate per timepoint (n=20 per pairing).
- Timepoints: days 2–6, with daily sampling for metabolomics and RNA.
- ISP2 medium composition: yeast extract, malt extract, glucose, agar (optional), pH 7.2.

## Metabolite extraction and LC-MS analysis

- Metabolite extraction: rectangular agar plugs including mycelia and surrounding agar; methanol extraction with three freeze-thaw cycles; supernatant dried and reconstituted for analysis.
- LC-MS instrumentation: Q Exactive Plus Hybrid Quadrupole-Orbitrap MS coupled to Ultimate 3000 UHPLC.
- Chromatography: Hypersil GOLD C18 column; gradient from 95% A to 95% B and back; flow rate 0.4 mL/min; 5 μL injection volume; 40 °C column temperature; autosampler at 4 °C; blanks and pooled QC samples included.
- Data acquisition: full MS mode; scan range 90–1350 m/z; resolution 70,000; positive and negative modes acquired in separate runs; instrument settings include AGC target and maximum injection time.

## Data analysis and processing

- Raw data converted to mzML format using ProteoWizard; mzML files used for deposit; peak-picking results available in a separate dataset.
- Data processing tools referenced: UmetaFlow as an untargeted metabolomics workflow, highlighting open-source processing compatibility.

## Quality control and reproducibility

- Analytical QC: blank injections at batch start and end to assess carryover; pooled QC samples analyzed every 6 injections to monitor drift.
- Randomized sample sequence; analysis performed in biological triplicate for each condition/replicate.
- Detailed instrumentation and method parameters provided to ensure reproducibility and comparability.

## Data accessibility and provenance

- The deposit provides raw mzML data, enabling re-processing with standard metabolomics pipelines.
- Analyzed peak datasets are available separately, facilitating downstream statistical analyses and metabolite identification.
- Funding sources: NERC (NE/T010959/1) and National Science Foundation (USA, 1935458).