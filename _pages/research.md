---
layout: archive
title: "Research Experience (Non-profit)"
permalink: /research/
author_profile: true
redirect_from:
  - /research
---

{% include base_path %}


---

# Marine Debris Detection

This document contains:
- Description of the best performing model from the Omdena Project _Detecting Plastic Debris through Satellite Imagery in the Italian and Mediterranean Seas_.
- A short summary of the evaluation methodologies used in papers [1], [2] which we might want to replicate if we decide to pursue publication.
- A paragraph comparing our model with the Map-Mapper models
- A going-forward paragraph, highlighting the possible next steps
Aim of the document :
- It should serve as both a recap and a starting point for the analysis to determine whether we want to pursue publication

## Model Description
- Our model is based on the **ResAttUNet** architecture. In the original paper the model is trained on MARIDA and solves a multi-class problem. The metrics are inferior to Map-Mapper. We improve over it, but we transform the task to a **binary** task.
- Our Model is trained on a **combined dataset** composed of MARIDA and the imagery from the Litter Windrows Catalog that we collected and preprocessed ourselves.
- **Our Model merges MARIDA classes 1, 2, 3, 4, 9 (1. Marine Debris, 2. Dense Sargassum, 3. Sparse Sargassum, 4. Natural Organic Material, 9. Foam) to a unique plastic debris proxy- class, following the paper [1]**.
- A distinctive feature of the training pipeline is the random selection of non-debris pixels from an annular neighborhood surrounding the annotated debris pixels in the Litter Windrows Catalog Dataset. This strategy helps mitigate the inherent imbalance between debris and background pixels. Both the proportion of non-debris pixels sampled from the annular region and the radius of that region are treated as hyperparameters.
- The metrics, following literature, are computed on the annotated pixels of the MARIDA test set (no random choice happens for the MARIDA dataset).
- 
## Model Performance
#### Our Model : Binary Segmentation Task


|                | Iou   | Prec. | F1    | Rec. |
| -------------- | ----- | ----- | ----- | ---- |
| Our best model | 0.817 | 0.889 | 0.899 | 0.90 |


#### Map-Mapper Model (Multi-Class Segmentation)

|                    | MD&SP IoU | MD&SP Prec. | F1       |
| ------------------ | --------- | ----------- | -------- |
| MAP-Mapper-Opt 0pt | **0.78**  | 0.87        | **0.88** |
| MAP-Mapper-HP      | 0.60      | **0.95**    | 0.75     |


#### References
1. Large-scale detection of marine debris in coastal areas with Sentinel-2 , [https://doi.org/10.1016/j.isci.2023.108402](https://doi.org/10.1016/j.isci.2023.108402 "Persistent link using digital object identifier")
2.  High-precision density mapping of marine debris and floating plastics via satellite imagery,  H.Booth, W. Ma, O. Karakus, [https://doi.org/10.1038/s41598-023-33612-2](https://doi.org/10.1038/s41598-023-33612-2)



# Flood Risk Assessment Using CHIRPS and Landsat Data in Sub-Basins

## 1. Introduction

Flooding poses a significant threat to many regions worldwide, including the Congo Basin. Effective flood risk management and mitigation require a comprehensive understanding of the factors contributing to flooding within specific sub-basins. This project utilizes a combination of CHIRPS (Climate Hazards Group InfraRed Precipitation with Station data) and Landsat data to analyze rainfall patterns and land cover changes to assess flood risk in various sub-basins.

By leveraging high-resolution precipitation data from CHIRPS and detailed land cover information from Landsat, the project aims to identify sub-basins most susceptible to flooding. This understanding is crucial for developing targeted strategies for flood risk reduction, including enhanced flood defenses, improved drainage infrastructure, and sustainable land management practices.

## 2. Background and Motivation

Flooding is a recurrent and devastating natural disaster that affects millions of people globally. Accurate flood risk assessment involves analyzing both climatic and land cover factors. CHIRPS provides high-resolution rainfall estimates, which are essential for identifying regions with significant precipitation. Landsat data offers detailed information on land use and land cover, which can be used to understand how these factors interact to influence flood risk.

In areas like the Congo Basin, where rainfall patterns and land cover changes significantly impact flood dynamics, integrating these datasets can provide valuable insights. For example, deforestation can increase runoff and reduce soil absorption, exacerbating flood risks. Therefore, understanding the relationship between rainfall and land cover is crucial for effective flood risk management.

## 3. Methodology

### 3.1 Data Collection

**CHIRPS Data:**
- CHIRPS provides high-resolution precipitation data, offering detailed insights into rainfall patterns over time.
- This dataset is used to identify regions within each sub-basin that experience significant precipitation, which is a key factor in flood risk.

**Landsat Data:**
- Landsat satellites offer detailed land cover and land use information.
- Key indices derived from Landsat data, such as the Normalized Difference Vegetation Index (NDVI) and soil moisture content, are used to assess vegetation cover and soil conditions.
- Changes in land cover, such as deforestation, are analyzed to understand their impact on flood risk.

### 3.2 Data Integration and Analysis

**Flood Risk Assessment:**
- Combining CHIRPS precipitation data with Landsat indices allows for a comprehensive analysis of flood risk.
- NDVI is used to assess vegetation health and cover, which influences soil absorption and runoff. Lower NDVI values indicate reduced vegetation cover, potentially increasing flood risk.
- Soil moisture content helps in understanding the soil's ability to absorb precipitation, with higher moisture levels indicating reduced capacity to handle additional rainfall.

**Sub-Basin Analysis:**
- The mean indices from Landsat data and CHIRPS precipitation data are used to evaluate flood risk across different sub-basins.
- Sub-basins with high precipitation and low vegetation cover are identified as more vulnerable to flooding.

### 3.3 Application of Findings

**Flood Mitigation Strategies:**
- The insights gained from the analysis are used to develop targeted flood mitigation strategies.
- Recommendations may include reinforcing flood defenses, improving drainage systems, and implementing sustainable land management practices to reduce flood risk.

**Resource Allocation:**
- Understanding the contribution of each sub-basin to overall flood risk enables more precise and effective allocation of resources for disaster preparedness and response.

## 4. Results and Discussion

The integration of CHIRPS and Landsat data provides a detailed understanding of flood risk within various sub-basins of the Congo Basin. By analyzing precipitation patterns and land cover changes, the project identifies sub-basins with the highest vulnerability to flooding. Key findings include:

- Sub-basins with significant precipitation and reduced vegetation cover are more susceptible to flooding.
- Changes in land cover, particularly deforestation, contribute to increased runoff and reduced soil absorption, exacerbating flood risks.

These findings highlight the importance of incorporating both climatic and land cover factors in flood risk assessments. The information gained is crucial for developing effective flood mitigation strategies and improving disaster preparedness.

## 5. Conclusion

This project successfully utilizes CHIRPS and Landsat data to assess flood risk in the Congo Basin. By analyzing rainfall patterns and land cover changes, the project identifies sub-basins most vulnerable to flooding and provides valuable insights for targeted flood risk management. The integration of high-resolution precipitation data with detailed land cover information enhances the accuracy of flood risk assessments, leading to more effective mitigation strategies and resource allocation.

Future work may focus on expanding the analysis to include additional factors such as topography and land use changes, as well as applying the methodology to other regions affected by flooding.

---

# Detection of Deforestation Due to Roads, Logging, Industrial Agriculture, and Slash & Burn in the Congo Basin

## 1. Introduction

The Congo Basin, often described as the "lungs of Africa," is home to the second-largest tropical rainforest in the world. This crucial ecosystem plays a significant role in global climate regulation, carbon sequestration, and biodiversity support. However, it faces severe threats from deforestation driven by various factors including roads, logging, industrial agriculture, and slash-and-burn practices. Effective detection of deforestation due to these specific activities is essential for targeted conservation and management efforts.

This project employs Sentinel-2 satellite imagery to detect deforestation associated with roads, logging, industrial agriculture, and slash-and-burn practices. By analyzing multiple vegetation and land cover indices, including **NDVI**, **EVI**, **MSAVI**, **NDMI**, **NBR**, **NDBI**, and **NDWI**, we aim to identify and map areas affected by these activities.

## 2. Background and Motivation

The Congo Basin’s rainforest is vital for regulating the global climate and maintaining biodiversity. Deforestation caused by roads, logging, industrial agriculture, and slash-and-burn methods threatens these functions and contributes to climate change. Detecting and understanding the impact of these activities is crucial for effective conservation and sustainable management.

**Remote Sensing Techniques:**
- **Sentinel-2 Satellite Imagery:** Provides high-resolution images with various spectral bands, enabling detailed land cover analysis.
- **Vegetation and Land Cover Indices:** These indices help assess vegetation health, moisture content, burn severity, urban expansion, and water bodies.

## 3. Methodology

### 3.1 Data Collection

**Sentinel-2 Data:**
- High-resolution imagery with 13 spectral bands.
- Multi-temporal images used to derive various indices and detect deforestation.

### 3.2 Indices Calculation

**Vegetation and Land Cover Indices:**
- **NDVI:** \[(NIR - Red) / (NIR + Red)\]
  - Indicates vegetation health; decreases suggest deforestation.
  
- **EVI:** \[2.5 \times (NIR - Red) / (NIR + 6 \times Red - 7.5 \times Blue + 1)\]
  - Provides enhanced vegetation information in dense areas; lower values may indicate deforestation.
  
- **MSAVI:** \[(2 \times NIR + 1 - \sqrt{(2 \times NIR + 1)^2 - 8 \times (NIR - Red)}) / 2\]
  - Reduces soil background effects; useful in areas with sparse vegetation.
  
- **NDMI:** \[(NIR - SWIR) / (NIR + SWIR)\]
  - Assesses moisture content; changes can indicate land cover alterations.

- **NBR:** \[(NIR - SWIR) / (NIR + SWIR)\]
  - Evaluates burn severity and changes in vegetation cover due to fires.

- **NDBI:** \[(SWIR - NIR) / (SWIR + NIR)\]
  - Highlights built-up areas and urban expansion; relevant for detecting infrastructure.

- **NDWI:** \[(Green - NIR) / (Green + NIR)\]
  - Identifies water bodies and assesses moisture; useful for detecting changes related to slash-and-burn practices.

### 3.3 Detection of Deforestation

**Target Activities:**
- **Roads:** Identified by increased NDBI and changes in NDVI and EVI values.
- **Logging:** Detectable through significant decreases in NDVI, EVI, and MSAVI values.
- **Industrial Agriculture:** Revealed by changes in NDVI, MSAVI, and NDMI values, indicating land conversion.
- **Slash and Burn:** Identified by variations in NDWI and NBR, indicating recent burning and vegetation removal.

**Analysis:**
- Temporal changes in vegetation and land cover indices are analyzed to detect and map deforestation due to the target activities.
- Significant changes in indices provide insight into the impact of roads, logging, industrial agriculture, and slash-and-burn practices.

### 3.4 Application of Findings

**Conservation and Management:**
- Identified deforestation hotspots are mapped and analyzed to inform targeted conservation strategies.
- Recommendations may include enforcing anti-logging measures, controlling agricultural expansion, and addressing slash-and-burn practices.

**Policy and Resource Allocation:**
- Detection results support policy decisions and resource allocation for conservation and management.
- Monitoring outcomes guide interventions to mitigate deforestation and promote sustainable practices.

## 4. Results and Discussion

The analysis of Sentinel-2 imagery and various indices successfully detected and mapped deforestation associated with roads, logging, industrial agriculture, and slash-and-burn practices. Key findings include:

- **Roads:** Increased NDBI values and changes in NDVI and EVI identified regions impacted by road construction.
- **Logging:** Significant decreases in NDVI, EVI, and MSAVI highlighted areas affected by logging activities.
- **Industrial Agriculture:** Changes in NDVI, MSAVI, and NDMI indicated land conversion for agriculture.
- **Slash and Burn:** Variations in NDWI and NBR revealed areas affected by burning practices.

These insights emphasize the need for targeted conservation measures and timely policy interventions to address the impact of these activities on the Congo Basin’s rainforest.

## 5. Conclusion

This project effectively utilized Sentinel-2 data and multiple vegetation and land cover indices to detect deforestation due to roads, logging, industrial agriculture, and slash-and-burn practices in the Congo Basin. The comprehensive analysis provided valuable information for conservation and management efforts, highlighting the importance of continued monitoring and targeted interventions.

Future work may involve integrating additional datasets and refining analysis techniques to enhance detection capabilities and support broader conservation initiatives.

