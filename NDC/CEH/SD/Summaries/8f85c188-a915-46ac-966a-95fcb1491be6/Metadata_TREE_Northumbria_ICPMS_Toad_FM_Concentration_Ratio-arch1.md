# TREE_Northumbria_ICPMS_Toad_FM_Concentration_Ratio

## Purpose and scope
- Dataset describing concentration ratios of multiple elements in toads, comparing fresh mass toad tissue (whole body) with dry mass soil from a co-located soil sample.
- Enables analysis of trace element uptake by toads and potential correlations with surrounding soil at sampling sites.
- Includes metadata to support traceability, sample preparation notes, and linkage to the associated soil sample.

## Dataset structure
- Tabular schema with a mix of metadata fields and concentration ratio measurements.
- Key metadata fields capture species information, sampling site, collection date, and sample identifiers.
- Concentration ratio fields cover a wide range of elements and are defined as the ratio of Fresh Mass Toad (whole body) to Dry Mass Soil.

## Metadata fields
- Latin_Species_Name: Latin name of the species.
- Common_Species_Name: Common name of the species.
- Site: Sampling site.
- Date_Sample_Collected: Date the sample was collected.
- CEH_Sample_Code: CEH sample code.
- CEH_Sample_Description: Description of the CEH sample.
- Notes: Notes about preparation of toads.
- Co_Located_Soil_Sample_Used_To_Calculate_Concentration_Ratio: Description of the soil sample used for calculating the concentration ratio.

## Concentration ratio fields
- I_Concentration_Ratio
- Li_Concentration_Ratio
- Be_Concentration_Ratio
- Na_Concentration_Ratio
- Mg_Concentration_Ratio
- Al_Concentration_Ratio
- P_Concentration_Ratio
- K_Concentration_Ratio
- Ca_Concentration_Ratio
- Ti_Concentration_Ratio
- V_Concentration_Ratio
- Cr_Concentration_Ratio
- Mn_Concentration_Ratio
- Fe_Concentration_Ratio
- Co_Concentration_Ratio
- Ni_Concentration_Ratio
- Cu_Concentration_Ratio
- Zn_Concentration_Ratio
- As_Concentration_Ratio
- Se_Concentration_Ratio
- Rb_Concentration_Ratio
- Sr_Concentration_Ratio
- Mo_Concentration_Ratio
- Ag_Concentration_Ratio
- Cd_Concentration_Ratio
- Cs_Concentration_Ratio
- Ba_Concentration_Ratio
- Tl_Concentration_Ratio
- Pb_Concentration_Ratio
- U_Concentration_Ratio

Note: Each Concen-tration_Ratio field is described as the Concentration Ratio (Fresh Mass Toad (wholebody) divided By Dry Mass Soil). The units are not applicable (unitless).

## How the data can be used
- Analyze correlations between soil metal concentrations and toad tissue uptake across sites.
- Develop predictive models of bioaccumulation for multiple elements.
- Compare element-specific uptake patterns and identify elements with notable soil-to-toad transfer.
- Support environmental decision-making by linking toads’ exposure to soil contaminants with sampling context (site, date, preparation notes).

## Data provenance and quality considerations
- Metadata enables traceability to specimen details and sampling context.
- Co-located soil sample linkage supports site-level interpretation of concentration ratios.
- The dataset emphasizes clear preparation notes to aid reproducibility and interpretation of tissue-to-soil ratios.