# LS²Net: A Lightweight Segmentation Network for Ultrasound Imaging via Synergy of Large and Small Receptive Fields

**Code will be made available upon paper acceptance.**

## Supplementary Analyses and Additional Materials from the Main Manuscript

This repository provides additional supplementary analyses and discussions related to the main manuscript. For each supplementary content item, specific location information is provided to facilitate easy reference. The supplementary content is indicated in the format: 

The following supplementary analysis provides additional discussion and analysis:
> Supplementary Material.

---

## I. Supplementary Materials from Related Work

### 1. Supplementary Discussion of the Limitations of Local Receptive Fields

**Location:**
Section II, **Related Work** → **Methods with Local Receptive Fields**, at the end of the subsection, following the discussion of ConvNeXt and LKSNeXt.

The following supplementary analysis provides additional discussion and analysis:

> However, conventional convolution operations are inherently limited in receptive field, and large-kernel convolutions often saturate in performance before achieving a truly global receptive field, frequently requiring deep network stacking to further expand the receptive field and achieve high performance.

---

### 2. Supplementary Discussion of the Limitations of Global Receptive Fields

**Location:**
Section II, **Related Work** → **Methods with Global Receptive Fields**, at the end of the subsection, following the discussion of BRAUNet++ and MCBTNet.

The following supplementary analysis provides additional discussion and analysis:

> However, despite their excellent global modeling abilities, both Transformers and Mamba have limitations. The self-attention mechanism in Transformers incurs quadratic computational complexity, resulting in substantial overhead, while structural characteristics of Mamba lead to slower inference speed. These constraints make both architectures challenging to deploy in clinical environments with limited computational resources [18].

---

### 3. Supplementary Discussion of Existing Ultrasound Segmentation Methods and LS²Net Motivation

**Location:**
Section II, **Related Work** → **Ultrasound Image Segmentation**, immediately after the discussion of BLENet and before the discussion of clinical generalization.

The following supplementary analysis provides additional discussion and analysis:

> However, these methods primarily rely on enlarging the receptive field to process ultrasound images, with the core objective of enhancing feature extraction. They do not explicitly address the fundamental challenges of ultrasound imaging, including speckle noise, low contrast, and blurry boundaries. Simply improving feature extraction is insufficient to balance segmentation performance and computational efficiency. More importantly, such approaches struggle to generalize effectively in real-world clinical environments characterized by multi-center data, heterogeneous devices, and diverse imaging conditions. To this end, LS²Net conducts a systematic analysis of the key challenges in ultrasound imaging and introduces targeted design strategies within the network architecture. Specifically, it enables effective noise suppression, discriminative feature extraction under low-contrast conditions, and refined boundary delineation. By doing so, LS²Net achieves a favorable trade-off between segmentation accuracy, computational efficiency, and model lightweightness. As shown in Table I, LS²Net demonstrates more comprehensive advantages and superior overall performance compared with existing methods.

---

## II. Supplementary Materials from Experiments and Results

### 4. Supplementary Discussion of Comparison with State-of-the-Art Models

**Location:**
Section IV, **Experiment and Results** → **D. Comparison with State-of-the-Art Models** .

The following supplementary analysis provides additional discussion and analysis:
> In the **breast ultrasound segmentation** task, LS²Net achieved outstanding results. On the BUSI dataset, it reached Dice scores of 80.06%, establishing the current state-of-the-art performance in lightweight and general models. On the BUS_BRA dataset, the Dice score was 89.80%. As shown in Fig.6, the model’s ability to simultaneously process multi-scale and multi-granularity feature maps enables accurate segmentation of lesions of varying sizes in both datasets. Furthermore, by leveraging RRSC to optimize feature information in skip connections, LS²Net achieves more precise boundary delineation. The segmentation results in Fig.6 demonstrate noticeably superior boundary adherence compared to other methods.
>
> In the **kidney ultrasound segmentation** task, LS²Net achieved SOTA results, attaining a Dice score of 89.70% and an mIoU of 81.35%, demonstrating a clear performance advantage. As shown in Fig.6, even in cases with complex backgrounds and blurred organ boundaries, LS²Net maintains strong regional consistency and boundary continuity, effectively preventing mis-segmentation.
>
> In the **cardiac ultrasound segmentation** task, the end-systole (ES) and end-diastole (ED) phases were annotated as EchoNet-ES and EchoNet-ED, respectively. LS²Net achieved state-of-the-art segmentation performance in both phases, with Dice scores of 91.68% and 93.61%, respectively. As shown in Fig.6, LS²Net accurately captures the contours of the target regions. Even in the structurally more complex EchoNet-ES phase, which contains more curved boundaries, the model precisely segments the curved regions with fewer erroneous predictions.



### 5. Supplementary Discussion of Comprehensive Analysis of LS²Net

**Location:**
Section IV, **Experiment and Results** → **E. Comprehensive Analysis of LS²Net** .

The following supplementary analysis provides additional discussion and analysis:

> **1) Cross-scenario applicability analysis**: ... In the colorectal polyp segmentation task, LS²Net achieved Dice scores of 85.03% and 91.97% on the Kvasir-SEG and CVC-ClinicDB datasets, respectively, demonstrating superior performance even under challenging conditions such as uneven illumination and strong reflections, where it maintains accurate boundary delineation with high robustness. Furthermore, in the multi-structure cardiac segmentation task, LS²Net achieved a Dice score of 88.90% and an HD95 of 5.36, outperforming most existing methods. ...
>
> **2) Parameter Efficiency Analysis**: ... the horizontal axis represents the magnitude of the L2 norm, reflecting feature intensity, while the vertical axis represents the distribution density of L2 norm values. The overall plot illustrates the distribution patterns of feature strengths across models. Compared with other methods, LS²Net exhibits higher and more concentrated L2 norm values, indicating stronger activation and richer feature responses. ... 
>
> **3) Analysis of Multi-Class Segmentation**: ... It achieves both clear inter-class separation and tight intra-class clustering, with background features well-separated from other tissue features, indicating superior feature discriminability. In contrast, EMCADNet and APFormer exhibit blurred background boundaries and partial overlap with other classes, reflecting weaker feature discrimination.
> 
> **4) Analysis of Binary Segmentation**: ...
> **Bland–Altman Analysis:**
> Bland-Altman analysis reflects the agreement between predicted and ground-truth pixel counts. As shown in Fig.11(a), overall performance is stable, with predictions closely matching the ground truth. Specifically, LS²Net achieved excellent segmentation results on BUS_BRA (bias = -196.98, SD = 1735.35), BUSI (bias = -423.47, SD = 3462.79), KidneyUS (bias = 118.36, SD = 1380.32), Kvasir-SEG (bias = -650.65, SD = 4619.4), CVC-ClinicDB (bias = -425.89, SD = 1480.23), EchoNet-ED (bias = 35.98, SD = 835.67), and EchoNet-ES (bias = -59.41, SD = 632.75). Most pixel differences are concentrated near the zero line, indicating minimal bias between predictions and ground truth, and demonstrating strong consistency of LS²Net across different datasets.
>
> **Linear Regression Analysis:**
> Linear regression analysis further validates the correlation between predicted and ground-truth values. As shown in Fig.11(b), LS²Net exhibits a strong positive correlation across multiple datasets. Specifically, BUS_BRA (R = 0.943, P = $9.43 \times 10^{-90}$), BUSI (R = 0.847, P = $1.548 \times 10^{-22}$), KidneyUS (R = 0.924, P = $6.11 \times 10^{-23}$), Kvasir-SEG (R = 0.854, P = $1.682 \times 10^{-29}$), CVC-ClinicDB (R = 0.963, P =$8.76 \times 10^{-36}$), EchoNet-ED (R = 0.951, P = 0), and EchoNet-ES (R = 0.947, P = 0) all show high correlation levels. The predicted values are closely distributed around the regression line, indicating that LS²Net demonstrates strong fitting capability and reliable correlation across different datasets.
>
> **4) Analysis of Binary Segmentation**: ... While general segmentation models can be deployed, their low inference speed (2–12 FPS) limits real-time applicability. In contrast, lightweight models achieve higher efficiency with lower complexity. ... Although MK-UNet achieves the lowest memory consumption and fastest inference speed, LS²Net maintains comparable computational efficiency while delivering consistently excellent segmentation performance across all datasets. This demonstrates that LS²Net effectively balances efficiency and segmentation accuracy by specifically addressing ultrasound imaging challenges such as noise interference, blurred boundaries, and low contrast.

---

### 6. Supplementary Discussion of Ablation Experiment

**Location:**
Section IV, **Experiment and Results** → **F. Ablation Experiment** .

The following supplementary analysis provides additional discussion and analysis:

> ... 
> The visualization results of APDCB emphasize the capture of texture details, showing higher sensitivity to local features and fine boundaries. However, it is also more susceptible to noise and background textures, which can lead to discontinuities in the overall target region. In contrast, DWTCB excels in parsing global structures. Through the multi-scale and global receptive field provided by wavelet convolution, the model can integrate information across a broader context, resulting in more robust performance in maintaining target contours and semantic consistency. Additionally, DWTCB demonstrates advantages in suppressing redundant background features, reducing false-positive regions and producing predictions that are morphologically closer to the ground truth. This contrast indicates that APDCB is more suitable for capturing local texture patterns, while DWTCB is superior in global structural modeling and target differentiation. Their complementary strengths further validate our theoretical hypothesis.
> ... 
> **Single large-kernel pathway**: larger receptive fields (e.g., 13×13) focus more on structural information and pay greater attention to the contour regions of the target. **Large-to-Small pathways**: Large receptive fields (e.g., 13×13, 9×9) first extract global structural information, emphasizing the overall contours and morphology of the target. Subsequently, small receptive fields (e.g., 3×3) refine local regions, further enhancing texture details and edge information, thereby ensuring both completeness and fine-grained accuracy of the segmentation results. **Small-to-Large pathways**: Small receptive fields (e.g., 1×1) initially focus on local features and details, but due to the lack of structural guidance, they may produce incomplete region segmentation. Larger receptive fields (e.g., 11×11) subsequently integrate these details into the global representation, gradually completing the overall structure. **similar size kernels pathways**: similar receptive fields (e.g., 5×5, 7×7) act as a balance between texture and structure, primarily capturing local patterns and regional consistency, thereby compensating for information that may be overlooked by overly large or small receptive fields.
> ... This mechanism compensates for key information lost during the downsampling–upsampling process, effectively enhancing the feature representation of skip connections. Consequently, the decoder can focus more on reconstructing fine-grained features, improving segmentation precision and accuracy. ... 

---

### 7. Supplementary Discussion of Cross Datasets Evaluation

**Location:**
Section IV, **Experiment and Results** → **G. Cross Datasets Evaluation** .
 
The following supplementary analysis provides additional discussion and analysis:

> ... When trained on the EchoNet-ED dataset and tested on Camus-ED, LS²Net demonstrated outstanding performance, achieving a Dice score of 92.80% and MIoU of 86.57%, ranking first. Compared with the other model, our model achieves superior segmentation performance, while using only 0.21M parameters. Similarly, when trained on EchoNet-ES and tested on EchoNet-ED, LS²Net achieved a Dice score of 92.45%. ...
> ... When trained on Kvasir-SEG and transferred to CVC-ClinicDB for testing, LS²Net achieved a Dice score of 77.11% and MIoU of 62.77%. In the reverse setting, trained on CVC-ClinicDB and tested on Kvasir-SEG, our model demonstrated strong competitiveness, achieving a Dice score of 57.76%.

---

### 8. Supplementary Discussion of Failure Case Analysis

**Location:**
Section IV, **Experiment and Results** → **H. Failure Case Analysis** .
 
The following supplementary analysis provides additional discussion and analysis:

> ...
> 
> In future work, the frequency-domain processing can be further improved. Specifically, frequency band selection or adaptive frequency weighting mechanisms can be introduced in the frequency branch to reduce the influence of unreliable high-frequency components on feature representation. In addition, incorporating frequency-domain consistency constraints—such as frequency-domain regularization or consistency loss during training—can help maintain more stable structural representations between the spatial and frequency domains, thereby improving robustness against artifacts.

---


## III. Supplementary Materials from Discussion and Conclusion

### 9. Supplementary Analysis of Discussion and Conclusion

**Location:**
Section V, **Discussion and Conclusion**.

The following supplementary analysis provides additional discussion and analysis:


>
> ... The encoder combines global and local receptive fields to capture multi-scale contextual information, while the decoder employs a multi-receptive field fusion strategy to reconstruct fine-grained features at different levels. The LACS module further refines skip connections to preserve boundary details. Benefiting from these architectural designs, LS²Net achieves a favorable trade-off between accuracy and efficiency, delivering state-of-the-art segmentation performance across five medical scenarios and seven datasets, and demonstrating strong generalization ability on four cross-dataset tests, while significantly reducing computational cost without sacrificing segmentation quality.
>
> LS²Net contains only 0.21M parameters and achieves an inference speed of 96 FPS, making it easily embeddable into ultrasound consoles or portable devices for real-time, on-device segmentation. 
% This capability enables efficient operation directly on the ultrasound platform, allowing real-time segmentation of target regions during image acquisition and substantially enhancing the efficiency and intelligence of ultrasound examinations. Clinically, real-time lesion localization and quantitative visualization during scanning facilitate faster and more accurate diagnosis, which is particularly valuable in emergency, bedside, and primary healthcare settings where computational resources are limited.
> 
> The collaborative receptive field paradigm integrates multi-scale receptive fields via a multi-branch architecture to jointly model structural and texture information. As it is inherently modality-agnostic, it demonstrates strong cross-modality generalization. In MRI and CT, large receptive fields capture global anatomical structures, while small receptive fields refine local details, enabling effective segmentation across different scales. In histopathology, large receptive fields model tissue-level context, whereas small receptive fields focus on cellular morphology, aligning well with cell-level analysis tasks. Overall, this paradigm provides a unified and flexible framework for multi-scale feature modeling, which can be readily extended to various medical imaging modalities and tasks.
>
> In real-world clinical settings, imaging devices and computational resources vary significantly across institutions and regions, and the applicability of our model in such diverse environments remains to be further explored. In the future, we plan to deploy LS²Net on edge computing devices and collaborate with clinicians for professional validation to further assess its feasibility and practicality in real-world clinical workflows. Through joint evaluation with medical experts, we aim to investigate the model’s consistency across different disease types, imaging parameters, and operator conditions, thereby confirming its clinical robustness and reliability. Moreover, the generalization capability of LS²Net across various imaging devices and modalities warrants further investigation. We intend to conduct systematic multi-center and multi-device experiments to evaluate its stability and adaptability, enhancing its reliability in diverse clinical scenarios. LS²Net is expected to promote the standardization and generalization of intelligent ultrasound-assisted diagnosis, providing a stable, efficient, and scalable intelligent diagnostic support system for remote areas and primary healthcare institutions.

---

