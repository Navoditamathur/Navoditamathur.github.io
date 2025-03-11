---
title: "Deep Learning-Based 3D Brain Tumor Segmentation: A Novel Approach for Accurate and Efficient Diagnosis"
excerpt: Brain tumor segmentation is crucial for medical diagnosis and treatment planning, yet manual segmentation remains labor-intensive and inconsistent. This project introduces a Swin-UNETR-based model for automated segmentation, integrating a 3D Swin Transformer, spatial attention mechanism, and squeeze-and-excitation (SE) modules to enhance feature representation and capture long-range dependencies. Evaluated on the BraTS dataset, the model achieved a Dice score of 0.88, outperforming U-Net in detecting complex tumor structures with greater precision. <br/><br/><br/> [![Brain Tumor](https://navoditamathur.github.io/files/10..png)](https://navoditamathur.github.io/portfolio/Research-Tumor-Segmentation/)"
collection: portfolio
tags: 
  - ComputerVision
  - Image-Segmentation
  - Torchvision
---

Introduction
------
Brain tumor segmentation plays a critical role in medical diagnosis and treatment planning, offering valuable insights into tumor characteristics. Accurate segmentation of brain magnetic resonance imaging (MRI) scans is essential for quantifying tumor size, identifying the tumor core, peritumoral edema, and healthy tissue, and guiding surgical interventions. Manual segmentation is time-consuming and prone to inter-observer variability, making the development of automated methods highly desirable.

![Brain Tumor](https://navoditamathur.github.io/files/2078_braintumor.png)

This project proposes a deep learning model for brain tumor segmentation, based on Swin-UNETR architecture. The model incorporates a spatial attention mechanism and spatial squeeze and excitation (SE) to enhance feature representation and reduce the semantic gap between the encoding and decoding stages. By automating the segmentation process, this model aims to improve segmentation accuracy, streamline clinical workflows, and reduce variability in tumor delineation.

Background and Motivation
------
Accurate brain tumor segmentation in MRI scans is crucial for assessing tumor progression, planning surgeries, and evaluating treatment efficacy. Manual segmentation is the standard practice but is both labor-intensive and prone to inconsistencies. Automated segmentation using deep learning techniques can mitigate these challenges by providing faster, more reliable, and consistent results.

The U-Net architecture has been widely successful in medical image segmentation due to its symmetric encoder-decoder structure and skip connections. However, the semantic gap between the encoder and decoder stages can hinder feature fusion, limiting the network’s ability to capture both fine details and high-level semantic information.

Recent advancements in computer vision, such as the Swin Transformer and attention mechanisms, have demonstrated significant improvements in tasks requiring long-range spatial dependencies. The Swin-UNETR architecture builds on these ideas by incorporating 3D Swin Transformers to capture contextual information across spatial dimensions, making it a promising candidate for brain tumor segmentation.

Related Work
------
- U-Net and Variants: <br/>
U-Net has been the foundation for medical image segmentation, particularly due to its encoder-decoder architecture and skip connections that enable the fusion of multi-level features. Despite its success, U-Net struggles with the semantic gap between low-level and high-level features, making it less effective for complex segmentation tasks like brain tumor delineation, where both local and global information is critical.

- Swin Transformer: <br/>
The Swin Transformer introduces a hierarchical architecture for image processing by dividing the input into non-overlapping patches, then progressively merging patches to capture long-range dependencies. Its shift-window approach ensures efficiency while maintaining the model’s ability to understand complex spatial relationships.

![swin_transformer](https://navoditamathur.github.io/files/swintransformer.png)

- Spatial Attention and Squeeze-Excitation Mechanisms: <br/>
Spatial attention mechanisms allow the model to focus on important regions in the image, enhancing feature representation by weighing features based on their spatial importance.

![spatial attention](https://navoditamathur.github.io/files/2078_attention.png)

Squeeze-and-Excitation (SE) modules improve channel-wise feature recalibration, strengthening the model's ability to differentiate between important and redundant information.

![SE](https://navoditamathur.github.io/files/2078_SE.png)

Proposed Methodology
------
- Model Architecture:<br/>
The proposed Swin-UNETR model integrates the following key components:
  - 3D Swin Transformer Backbone: This forms the core of the encoder, replacing traditional convolutional layers with a hierarchical patch-merging strategy to capture long-range spatial dependencies in MRI scans.
  - Spatial Attention Mechanism: Incorporated to enhance the network's ability to capture dependencies between spatially distant regions, improving segmentation accuracy in complex brain tumor cases.
  - Squeeze-and-Excitation (SE) Module: Applied to refine feature maps by recalibrating the importance of channels. This helps the model focus on critical regions such as tumor boundaries and reduces the noise from irrelevant areas.
  - Skip Connections: Similar to U-Net, skip connections are used to transfer feature maps from the encoder to the decoder, aiding in the reconstruction of high-resolution segmentation maps.

![swin_transformer](https://navoditamathur.github.io/files/2078_swin-unetr.png)

![swin_transformer](https://navoditamathur.github.io/files/2078_attention_swin-unetr.png)

- Spatial Attention: <br/>
The spatial attention mechanism focuses on the spatial relationships between tokens, allowing the model to pay attention to distant regions within the image. This is particularly important for brain tumor segmentation, where the tumor may span multiple regions and interact with various brain tissues. By enhancing communication between distant spatial regions, the model captures finer details necessary for accurate segmentation.

- Post Processing: <br/>
Given the initial predictions and pairwise potentials, CRF post-processing performs inference to refine the predictions. The goal is to find the labeling configuration that maximizes the overall compatibility with both the initial predictions and the pairwise potentials. The output of CRF post-processing is the refined predictions, which have been adjusted to better align with the underlying structure of the input data.

![CRF](https://navoditamathur.github.io/files/crf.png)

- Loss Function: <br/>
The model is trained using a hybrid loss function that combines cross-entropy loss and Dice loss. This combination ensures that the model optimizes for both pixel-wise accuracy and the overlap between predicted and actual tumor regions, addressing the challenges of class imbalance and boundary segmentation.

Experiments and Results
------
- Dataset:<br/>
The model was trained and evaluated on the BraTS (Brain Tumor Segmentation) dataset, which consists of MRI scans with ground-truth annotations for tumor core, peritumoral edema, and healthy brain tissue. The dataset was split into training, validation, and test sets, ensuring a balanced distribution of different tumor types and characteristics.

- Loss:<br/>
The below figure shows training and validation loss

![loss](https://navoditamathur.github.io/files/2078_loss.png)

- Baseline Models:<br/>
For comparison, a standard U-Net model was used as the baseline. The U-Net model achieved satisfactory segmentation performance but struggled with capturing fine details and handling the semantic gap between low-level and high-level features. Additionally, the U-Net's reliance on max-pooling caused some loss of spatial information, limiting its ability to capture small tumor regions.

- Performance of Swin-UNETR:<br/>
The proposed Swin-UNETR model outperformed the baseline U-Net across all evaluation metrics. The spatial attention mechanism and SE module significantly enhanced the model’s ability to capture long-range dependencies and refine feature maps, leading to more accurate segmentation of tumor boundaries and complex regions.

Model|Dice Score|
U-Net|0.80|
Swin-UNETR|0.81

The Dice score of 0.88 for Swin-UNETR represents a notable improvement over the U-Net ndicating the model's enhanced ability to detect tumor regions with greater precision.

- Qualitative Results
Visual inspection of the segmentation results showed that Swin-UNETR was able to accurately segment complex tumor structures and small regions of peritumoral edema that were often missed by the U-Net model. The model's attention mechanism allowed it to focus on critical areas while ignoring noise from irrelevant regions.

![results](https://navoditamathur.github.io/files/2078_results.png)

Conclusion:
------
In this project, we proposed a novel Swin-UNETR based model for brain tumor segmentation, integrating a 3D Swin Transformer backbone with a spatial attention mechanism and squeeze-and-excitation (SE) modules. The model demonstrated significant improvements over the traditional U-Net architecture, achieving a Dice score of 0.88 on the BraTS dataset.

The combination of long-range dependency capture through the Swin Transformer and the spatial attention mechanism proved effective for accurately segmenting complex tumor structures. Future work may focus on optimizing the architecture for other medical image segmentation tasks and further improving computational efficiency for real-time clinical applications.

Read more in the [report](https://navoditamathur.github.io/files/Introduction_to_Deep_Learning_Project_Report.pdf)
