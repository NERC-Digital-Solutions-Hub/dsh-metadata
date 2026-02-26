# Sampling design

- Scope and timing
  - Soils were sampled in CS in 1978, 1998 and 2007.
  - 1978 and 1998 sampled the same 256 squares; 2007 sampled all 591 CS squares.
  - Power analyses were conducted to determine the number of samples needed to detect significant change (Emmett et al. 2008).

- Spatial design and sampling units
  - Soils are sampled from CS x-plots; there are 5 x-plots randomly spaced within each CS square.
  - X-plots within a square are not replicates; they may differ in land use and soil type.
  - X-plots can be relocated over years due to plot destruction, access denial, or relocation uncertainty.
  - Each sampling location has a unique repeat identifier (e.g., 2RPT1): square 2, repeat plot 1.
  - Within permanently marked 2m x 2m plots, sampling locations are typically 2–3 m apart at the corners.

- Sampling method and data collection
  - Depths: top 15 cm (8 cm for invertebrates) sampled in 1998 and 2007; 1978 used a soil pit and sampled the top 15 cm from the pit side.
  - Core vs pit: 1998/2007 used soil cores hammered into the soil; 1978 used a soil pit.
  - Practical constraints: full cores may be unavailable due to stones or shallow soils.
  - In 2007, lab staff photographed cores and measured core dimensions on 2 of the 4 cores (black cores and N mineralization cores).

- Measurements and data structure
  - 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
  - 1998/2007: multiple cores per x-plot with different measurements; Table 1 lists measurements by core.
  - Measurements include: pH (in water and CaCl2), LOI, %C, %N, bulk density (not ISO-standard method), core dimensions, photographs, depth of organic layer, hand texture, soil moisture, Olsen P, metals, mineralisable N, and more.
  - Coverage: some measurements were made for all 591 squares; others only for subsets (e.g., original 256 squares).
  - Data release notes: some measurements "data only released after the Soils Report published in November 2009."

- Data analysis and GIS considerations
  - Analyses should account for land class structure; neglecting it biases results toward stock/change rather than national estimates.
  - Bootstrapping is not consistently applied; preferred approach is a mixed model with square as a random factor to reflect multiple x-plots per CS square.
  - Design-based approaches (dispersed observations) can improve regional precision and coverage when spatial structure is not the primary interest.
  - Users are advised to consult CEH before analysis and to review published CS data using resources listed on the CS website.

- Practical notes for GIS users
  - Distinguish between original 256 squares and all 591 squares when mapping temporal changes.
  - Use repeat identifiers (e.g., 2RPT1) to link successive samples from the same location while acknowledging a 2–3 m offset in exact sampling points.
  - Be aware of year- and core-specific measurement availability; consult data release notes (Soils Report 2009) for restricted measurements. 

- Reference
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. CEH Project No. C03042/ DEFRA Contact No. CR0334.