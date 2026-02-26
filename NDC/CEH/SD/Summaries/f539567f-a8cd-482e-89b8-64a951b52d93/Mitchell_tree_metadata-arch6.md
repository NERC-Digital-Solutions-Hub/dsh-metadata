# Functional and epiphytic biodiversity differences between nine tree species in the UK

- Purpose and context
  - Addresses global concern about pests and pathogens affecting trees and the potential ecosystem function changes if species shift.
  - Compares functional and epiphytic biodiversity (bryophytes and lichens) across nine tree species, including three UK-threatened oaks and potential ecological replacements.
  - Key variables: nitrogen mineralization and decomposition rate; total soil carbon and nitrogen; loss on ignition; soil pH; soil temperature; bark water holding capacity; bark pH and conductivity; and bark characteristics.

- Species and sites
  - Tree species: Acer pseudoplatanus, Castanea sativa, Fagus sylvatica, Fraxinus excelsior, Quercus cerris, Quercus petraea, Quercus robur, Quercus rubra, Tilia x europaea.
  - Sites (six across the UK): Knightshayes Court (England), Bodnant (Wales), Dinefwr (Wales), Westonbirt (England), Crathes (Scotland), Mount Stuart (Scotland).
  - Sampling: 230 trees total (roughly 35–40 per site); site climate data from nearby meteorological data; site descriptions include habitat type around each tree.

- Field and lab data collected per tree
  - Tree measurements and context
    - Girth/DBH, height; site habitat classification (semi-natural woodland, grassland/parkland, garden); four cardinal habitat sectors around the tree; distance to nearest tree; GPS/easting/northing coordinates; slope and aspect; canopy and litter notes.
    - Bark sampling indicators (whether a bark sample was taken).
  - Decomposition experiments
    - Litter decomposition using four Whatman filter papers inside a nylon mesh bag, buried 3 m south of each tree; litter-bag time points and recovery data; associated sticks and notes.
    - Soil temperature measured hourly near each tree (iButton loggers) for decomposition context.
  - Soil sampling and analyses
    - Eight soil samples per tree around the trunk; lab analyses include:
      - Loss on ignition (LOI) at 450°C.
      - pH in water and in CaCl2.
      - Total carbon (C) and nitrogen (N).
      - Mineralizable N and forms of inorganic N (TON-N, NH4-N) before and after incubation.
      - N-mineralization rate.
  - FTIR and bark chemistry
    - Fourier-transform infrared (FTIR) spectral data on processed soil; pre-processing details and spectra range.
    - Bark chemistry: water holding capacity, bark pH, conductivity; bark samples processed and analyzed.
  - Bark physical characteristics
    - On four cardinal heights per tree, bark pattern (smooth, fissured, flaky, rugose, patterned, plus other features), fissure shapes, ridge and furrow measurements, ridge alignment, bark hardness (durometer), and plot-level measurements (eight measurements per quadrat).
  - Bark plot and canopy metrics
    - Plot-level variables include eight measurements related to fissures, width/depth of furrows and ridges, and various bark features per quadrant.
  - Lichen and bryophyte data
    - All lichen and bryophyte species recorded on trunk (ground level to 1.75 m); branches and twigs recorded where accessible.
    - Taxa names and authorities stored in separate reference files; presence/absence data captured for trunk, branches, twigs.

- Data structure and access
  - Relational database design with a central Trees table (ANS_Tree_code) linking to multiple other tables.
  - Tables and data files include: Trees, Habitat_structure, Decomposition, Temperature, Soil, FTIR, Bark_chemistry, Bark_plot, Bryophytes, Lichens, plus taxonomy reference tables (Bryophyte_names, Lichen_names).
  - Metadata and descriptions provided for each table and field to enable data self-service and integration across datasets.

- Outputs, provenance, and credits
  - Acknowledgments: funded by Defra via the PuRpOsE project (BBSRC) and the Scottish Government’s Rural and Environment Research and Analysis Directorate.
  - References for methods and related ecological context are provided, supporting reproducibility and methodological transparency.