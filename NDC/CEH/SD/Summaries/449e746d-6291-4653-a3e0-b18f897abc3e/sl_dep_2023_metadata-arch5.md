# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2023)

## Purpose and scope
- Study of high atmospheric ammonia (NH3) effects on forest vegetation, bryophytes, lichens, and soil using a wind-controlled NH3 enhancement experiment.
- Location: Queensberry Estate, central Sri Lanka; coordinates 6.9693° and 80.5911°, altitude 1645 m.
- Time frame: NH3 concentrations measured January 2023 to December 2024; data extend a 2022 dataset from the same site.

## Data collection and content
- NH3 enhancement system activated by wind direction and threshold speeds (0.3–10 m s⁻¹) to monitor upwind quadrats.
- NH3 concentrations measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers.
- Measurements produced as a CSV with 816 rows across 13 parameters.
- Key data fields:
  - Distance (m) from NH3 source; sign indicates direction (negative southwest, positive northeast)
  - Month (year-month)
  - NH3_conc (µg m⁻³): monthly average NH3 concentration at 1.5 m
  - Deposition flux components: Fg (soil), Fs_us (understory stomatal), Ftt (tree trunks), Fs_tc (canopy stomatal), and various cuticular deposition terms (Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones, Fd_us; Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc)
  - Flux signs: negative indicates emission

## Modelling and data context
- Deposition/emission estimates derived from a four-layer canopy bi-directional resistance model.
- Components modeled: soil surface, understory vegetation, tree trunks, tree canopy; includes stomatal and cuticular pathways and a capacitance term for cuticular deposition.
- Deposition flux to soil uses quasi-laminar boundary layer resistance; to trunks uses a boundary layer resistance model; stomatal and cuticular resistances include LAI and environmental dependencies.
- Major methodological improvement over prior versions: the current model simulates NH3 concentration peaks during release periods to estimate deposition, rather than using mean monthly concentrations for all intervals.

## Data structure and documentation
- Data file: CSV with 816 measurements across 13 parameters.
- Columns include Distance, Month, NH3_conc, and deposition flux terms for soil (Fg, etc.), understory (Fs_us, Fw_us_*), tree canopy/trunk (Fs_tc, Fw_tc_*, Fd_tc), and related emissions terms (negative values indicate emission).

## Quality control and data integrity
- Visual quality checks conducted; obviously erroneous data removed (instrument faults, datalogger issues, power cuts).
- Regular gaps due to scheduled power cuts; additional gaps from sensor replacements.
- Dataset described as an extension/improvement of the 2022 dataset from the same site.

## Data governance, availability, and provenance
- Dataset described as CSV with explicit units and descriptions; files include detailed parameter definitions and directional distance interpretation.
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- Related datasets and references:
  - 2022 dataset from Queensberry site
  - Associated meteorological and NH3 concentration/deposition data (Deshpande et al., 2024a, 2024b)
  - Methodological references for deposition resistances and deposition parameterizations (e.g., Massad et al. 2010; Jones et al. 2007; Sutton et al. 1998; Nemitz et al. 2000; DEPAC module van Zanten et al. 2010)
- For data stewardship:
  - Consider providing a dataset-level metadata record with creators, affiliations, contact, collection period, location, instruments, sampling protocol, QA/QC procedures, and licensing.
  - Include cross-references to the underlying modelling code or parameterizations where possible to enable reproducibility.
  - Indicate any data access restrictions, embargoes, or expected update/maintenance plans and versioning (this extension indicates ongoing updates from 2022 onward).

## Practical implications for reuse
- Suitable for researchers studying bi-directional NH3 exchange, deposition to forest ecosystems, and modelling atmospheric-vegetation NH3 interactions.
- Interoperability considerations: Units are SI; distance indexing and direction convention should be preserved for correct spatial interpretation.
- Users should consult the cited methodological papers and the 2022/2024 Deshpande et al. works for full model specifications and parameterizations.