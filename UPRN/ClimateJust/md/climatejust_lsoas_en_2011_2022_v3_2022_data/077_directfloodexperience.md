### Number of properties within historical flood boundary (Z-Score)

**Description:**
This field (identified internally as `DirectFloodExperience` or standardized as a Z-score under `Z_DirectFloodExperience` in the spatial dataset) represents the proportion of properties within a given Lower Super Output Area (LSOA) that fall within a historical flood boundary. It serves as a proxy metric for "Direct flood experience" to evaluate the level of existing local knowledge within a neighbourhood.

**Vulnerability Rationale:**
Unlike the vast majority of indicators in the Climate Just dataset, higher raw values for this indicator represent **lower** social vulnerability. This metric is utilized across several dimensions, including "Community Support," "(In)ability to Prepare," and "(In)ability to Respond". 

The rationale for this reversed relationship is based on the "prisoner of experience" phenomenon. A community with a history of flooding is generally better equipped to handle future events for several reasons:
*   **Local Knowledge and Preparedness:** Those with direct experience of flooding have more knowledge about what to do and how to respond during an emergency. They are significantly more likely to take preventative actions, such as installing property-level flood defences, and are more likely to respond seriously to official flood warnings.
*   **Community and Institutional Support:** Areas with historical flooding are more likely to benefit from a higher level of targeted activity, awareness campaigns, and support from both government and non-government organizations. 
*   Conversely, populations without direct flood experience are generally less able to cope and may remain more vulnerable until they unfortunately experience an event firsthand.

**Interpretation:**
Because past experience provides a protective function, the raw data for this indicator is **reversed** (or negatively weighted) when calculating the final vulnerability indices so that it aligns with the standard format where higher scores equal higher vulnerability. 
When looking at the standardized Z-scores (`Z_DirectFloodExperience`):
*   **Positive Z-scores (Reversed)** denote a *lack* of historical flood experience compared to the national average, indicating less local knowledge and thus a **higher** level of relative vulnerability.
*   **Values around 0** indicate average levels of historical flood experience.
*   **Negative Z-scores (Reversed)** signify *more* historical flood experience than the national average, indicating greater community awareness and **lower** relative vulnerability.

**Data Source:**
For the 2022 England LSOA dataset, the underlying data relies on queries of residential property datasets against historical flood outlines (limited to the past 50 years where date information is available) provided by the Environment Agency (EA) and other national rivers agencies. This data was compiled by Sayers et al. (2017). When used to calculate specific indices like the "Inability to Prepare" or "Inability to Respond" indices, this reversed indicator carries a weight of 0.333 alongside other factors like population transience and lack of flood warning coverage.