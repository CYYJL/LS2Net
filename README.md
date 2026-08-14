# LS2Net: A Lightweight Segmentation Network for Ultrasound Imaging via Synergy of Large and Small Receptive Fields
Code will be made available upon paper acceptance

## Deleted Content from Introduction

The following figures were removed from the Introduction section of the manuscript solely to comply with the IEEE Regular Paper page limit. They are preserved here for editorial reference.

### Figure 1 — Effective Receptive Field (ERF) Visualization

<div align="center">

<img src="Figure/ERF.jpg" width="92%" alt="Effective Receptive Field (ERF) Visualization"/>

<br/>

<sub>
<i>
<b>Figure 1.</b> Visualization of the Effective Receptive Fields (ERF) across different methods reveals distinct characteristics. U-Net (CNN-based) exhibits a blurred and highly localized receptive field, whereas MobileUViT (Transformer-based) shows a dispersed and weak response. LS$^2$Net (baseline) achieves a more concentrated yet limited receptive field. In contrast, the full LS$^2$Net model produces a clearer and more balanced ERF distribution, effectively capturing both local details and global context, thereby demonstrating superior feature modeling capability. We take the central response of the output feature map as the target and compute its gradient distribution with respect to the input pixels via backpropagation to characterize the contribution of different regions. The results are then averaged across multiple samples and normalized using logarithmic scaling to obtain a stable estimation of the effective receptive field (ERF). Furthermore, by measuring the minimal high-contribution coverage ratios under different thresholds (20%, 30%, 50%, and 99%), we quantitatively compare the spatial modeling capability of different models.</i>
</sub>

<br/>

<sub>
<i>Removed from the main manuscript to comply with the IEEE Regular Paper page limit.</i>
</sub>

</div>

<br/>

---

### Figure 2 — Challenges in Ultrasound Image Segmentation

<div align="center">

<img src="Figure/challenge.jpg" width="92%" alt="Challenges in Ultrasound Image Segmentation"/>

<br/>

<sub>
<i>
<b>Figure 2.</b> Challenges in ultrasound image segmentation and the targeted design of LS$^2$Net for balancing accuracy and computational efficiency.
</i>
</sub>

<br/>

<sub>
<i>Removed from the main manuscript to comply with the IEEE Regular Paper page limit.</i>
</sub>

</div>

<br/>

---
## Related Work

The following materials were removed from the Related Work section of the manuscript solely to comply with the IEEE Regular Paper page limit. The deleted content is preserved here for editorial reference.

### 1. Deleted Discussion: Limitations of Local Receptive Fields

**Original location:**
Section II, **Related Work** → Subsection **Methods with Local Receptive Fields**, at the **end of the subsection**, immediately after the paragraph discussing **ConvNeXt and LKSNeXt**.

**Text immediately preceding the deleted content:**

> Models such as ConvNeXt \cite{han2022convunext} and LKSNeXt \cite{zhao2025lksnext} employ large-kernel convolutions to expand the receptive field, enhancing global information modeling and capturing long-range dependencies in medical images.

**Deleted text:**

> However, conventional convolution operations are inherently limited in receptive field, and large-kernel convolutions often saturate in performance before achieving a truly global receptive field, frequently requiring deep network stacking to further expand the receptive field and achieve high performance.

**Reason for deletion:**
This discussion was removed solely to reduce the manuscript page count. The related discussion of local receptive field-based methods remains in the main manuscript.

---

### 2. Deleted Discussion: Limitations of Global Receptive Fields

**Original location:**
Section II, **Related Work** → Subsection **Methods with Global Receptive Fields**, at the **end of the subsection**, immediately after the paragraph discussing **BRAUNet++ and MCBTNet**.

**Text immediately preceding the deleted content:**

> Similarly, MCBTNet incorporates CNN and Transformer within a U-shaped encoder–decoder framework, and leverages the dynamic sparsity of dual-layer routing attention Transformers to effectively capture global contextual information, thereby maximizing multi-scale feature utilization and improving both segmentation accuracy and efficiency.

**Deleted text:**

> However, despite their excellent global modeling abilities, both Transformers and Mamba have limitations. The self-attention mechanism in Transformers incurs quadratic computational complexity, resulting in substantial overhead, while structural characteristics of Mamba lead to slower inference speed. These constraints make both architectures challenging to deploy in clinical environments with limited computational resources \cite{tang2025mobile}.

**Reason for deletion:**
This discussion was removed solely to reduce the manuscript page count. The main manuscript retains the discussion of global receptive field-based methods.

---

### 3. Deleted Table: Comparison of the Advantages of Different Methods

**Original location:**
Section II, **Related Work** → Subsection **Methods with Hybrid Receptive Fields**, **after the paragraph discussing MSCWNet and before the subsection `Ultrasound Image Segmentation`**.

**Deleted content:**

<div align="center">

<table>
<tr>
<th>Model</th>
<th>MSRFS</th>
<th>NS</th>
<th>LCFE</th>
<th>BR</th>
<th>LW</th>
</tr>
<tr>
<td>UNet</td><td></td><td></td><td></td><td></td><td></td>
</tr>
<tr>
<td>ATT-UNet</td><td></td><td></td><td></td><td></td><td></td>
</tr>
<tr>
<td>AAU-Net</td><td>✓</td><td></td><td></td><td></td><td></td>
</tr>
<tr>
<td>Swin-UMamba</td><td>✓</td><td></td><td></td><td></td><td></td>
</tr>
<tr>
<td>Dilated Transformer</td><td>✓</td><td>✓</td><td>✓</td><td></td><td></td>
</tr>
<tr>
<td>TransFSM</td><td></td><td></td><td></td><td>✓</td><td></td>
</tr>
<tr>
<td>ANNet</td><td>✓</td><td>✓</td><td></td><td></td><td></td>
</tr>
<tr>
<td>BRAUNet++</td><td>✓</td><td></td><td></td><td></td><td></td>
</tr>
<tr>
<td>MCBTNet</td><td>✓</td><td></td><td></td><td></td><td></td>
</tr>
<tr>
<td>APFormer</td><td>✓</td><td>✓</td><td></td><td></td><td>✓</td>
</tr>
<tr>
<td>MobileUViT</td><td>✓</td><td></td><td></td><td></td><td>✓</td>
</tr>
<tr>
<td>BLENet</td><td>✓</td><td>✓</td><td></td><td></td><td>✓</td>
</tr>
<tr>
<td>PMFSNet</td><td>✓</td><td></td><td></td><td></td><td>✓</td>
</tr>
<tr>
<td><b>LS²Net</b></td><td>✓</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td>
</tr>
</table>

<br/>

<sub>
<i>
<b>Table.</b> Comparison of the advantages of different methods.
MSRFS: Multi-scale Receptive Field Synergy;
NS: Noise Suppression;
LCFE: Low-contrast Feature Extraction;
BR: Boundary Refinement;
LW: Lightweight design.
</i>
</sub>

</div>

**Reason for deletion:**
This comparison table was removed solely to reduce the manuscript page count.

---

### 4. Deleted Discussion: Challenges of Existing Ultrasound Segmentation Methods and LS²Net Motivation

**Original location:**
Section II, **Related Work** → Subsection **Ultrasound Image Segmentation**, immediately after the paragraph ending with the discussion of **BLENet** and before the discussion of clinical generalization.

**Text immediately preceding the deleted content:**

> In contrast, BLENet [23] draws inspiration from efficient human visual processing, proposing an antagonistic bio-inspired module and integrating frequency-domain transformation to expand the receptive field and enhance feature extraction.

**Deleted text:**

> However, these methods primarily rely on enlarging the receptive field to process ultrasound images, with the core objective of enhancing feature extraction. They do not explicitly address the fundamental challenges of ultrasound imaging, including speckle noise, low contrast, and blurry boundaries. Simply improving feature extraction is insufficient to balance segmentation performance and computational efficiency. More importantly, such approaches struggle to generalize effectively in real-world clinical environments characterized by multi-center data, heterogeneous devices, and diverse imaging conditions. To this end, LS²Net conducts a systematic analysis of the key challenges in ultrasound imaging and introduces targeted design strategies within the network architecture. Specifically, it enables effective noise suppression, discriminative feature extraction under low-contrast conditions, and refined boundary delineation. By doing so, LS²Net achieves a favorable trade-off between segmentation accuracy, computational efficiency, and model lightweightness. As shown in Table III, LS²Net demonstrates more comprehensive advantages and superior overall performance compared with existing methods.

**Reason for deletion:**
This discussion was removed solely to reduce the manuscript page count and avoid redundancy with the motivation presented in the Introduction, and the core motivation and contributions of LS²Net remain in the main manuscript

---

## Deleted Content from Experiment and Results

The following materials were removed from the Experiment and Results section of the manuscript solely to comply with the IEEE Regular Paper page limit. They are preserved here for editorial reference.

### 1. Deleted Figure: Bland–Altman and Linear Regression Analysis

**Original location:**
Section IV, **Experiment and Results** → Subsection **Comprehensive Analysis of LS²Net** → **4) Analysis of Binary Segmentation**.

The deleted figure was originally placed immediately after the discussion of the cross-scenario segmentation performance and before the **“5) Deployment Analysis”** subsection.

**Figure file:**
`Figure/BAB_Analysis.jpg`

**LaTeX label:**
`fig:bab`

**Deleted figure:**

<div align="center">

<img src="Figure/BAB_Analysis.jpg" width="92%" alt="Bland–Altman and Linear Regression Analysis"/>

<br/>

<sub>
<i>
<b>Figure.</b> Bland–Altman analysis and linear regression analysis of binary segmentation datasets between LS$^2$Net predictions and ground truth (GT). (a) Bland–Altman analysis evaluates the agreement between LS$^2$Net predictions and GT by quantifying the mean bias and limits of agreement (±1.96 SD). A smaller bias and narrower limits indicate better consistency and less systematic deviation across datasets. (b) Linear regression analysis assesses the correlation between LS$^2$Net and GT through Pearson’s correlation coefficient (R) and corresponding P-value. Higher R values and statistically significant P values (typically P $<$ 0.05) demonstrate a strong linear relationship and reliable predictive performance of LS$^2$Net across different binary segmentation datasets.
</i>
</sub>

<br/>

<sub>
<i>Removed from the main manuscript to comply with the IEEE Regular Paper page limit.</i>
</sub>

</div>

<br/>

---

### 2. Deleted Discussion: Analysis of Binary Segmentation

**Original location:**
Section IV, **Experiment and Results** → Subsection **Comprehensive Analysis of LS²Net** → **4) Analysis of Binary Segmentation**.

**Text immediately preceding the deleted content:**

> When combined with other modules, the Dice score further increases from 76.74\% to 80.20\%, demonstrating the effectiveness of MRCFM, as shown in Fig. \ref{fig:mrcfm}.

**Deleted text:**

> **4) Analysis of Binary Segmentation:** For other binary segmentation datasets, model performance was analyzed using Bland-Altman and linear regression analyses. The number of foreground pixels in both the predicted and manually annotated masks was summed, with the foreground pixel count representing the area of the target segmentation region. The areas of the predicted masks were then compared with those of the ground truth to evaluate LS²Net’s segmentation performance.
>
> **Bland-Altman Analysis:** Bland-Altman analysis reflects the agreement between predicted and ground-truth pixel counts. As shown in Fig. \ref{fig:bab}(a), overall performance is stable, with predictions closely matching the ground truth. Specifically, LS²Net achieved excellent segmentation results on BUS\_BRA (bias = -196.98, SD = 1735.35), BUSI (bias = -423.47, SD = 3462.79), KidneyUS (bias = 118.36, SD = 1380.32), Kvasir-SEG (bias = -650.65, SD = 4619.4), CVC-ClinicDB (bias = -425.89, SD = 1480.23), EchoNet-ED (bias = 35.98, SD = 835.67), and EchoNet-ES (bias = -59.41, SD = 632.75). Most pixel differences are concentrated near the zero line, indicating minimal bias between predictions and ground truth, and demonstrating strong consistency of LS²Net across different datasets.
>
> **Linear Regression Analysis:** Linear regression analysis further validates the correlation between predicted and ground-truth values. As shown in Fig. \ref{fig:bab}(b), LS²Net exhibits a strong positive correlation across multiple datasets. Specifically, BUS\_BRA (R = 0.943, P = 9.43×10$^{-90}$), BUSI (R = 0.847, P = 1.548×10$^{-22}$), KidneyUS (R = 0.924, P = 6.11×10$^{-23}$), Kvasir-SEG (R = 0.854, P = 1.682×10$^{-29}$), CVC-ClinicDB (R = 0.963, P = 8.76×10$^{-36}$), EchoNet-ED (R = 0.951, P = 0), and EchoNet-ES (R = 0.947, P = 0) all show high correlation levels. The predicted values are closely distributed around the regression line, indicating that LS²Net demonstrates strong fitting capability and reliable correlation across different datasets.

**Reason for deletion:**

This analysis and its corresponding figure were removed solely to reduce the manuscript page count. The quantitative segmentation results and the main conclusions regarding the performance and generalization capability of LS²Net remain in the main manuscript.

---

### 3. Deleted Figure and Discussion: Failure Case Analysis

**Original location:**
Section IV, **Experiment and Results** → Subsection **Cross Datasets Evaluation**, after the discussion of the generalization results on the colorectal datasets.

**Deleted content:**
The complete **“Failure Case Analysis”** subsection and its corresponding figure.

**Figure file:**
`Figure/faile_case.jpg`

**LaTeX label:**
`fig:fail`

**Deleted figure:**

<div align="center">

<img src="Figure/faile_case.jpg" width="92%" alt="Failure Cases of Segmentation Caused by Frequency Aliasing"/>

<br/>

<sub>
<i>
<b>Figure.</b> Failure Cases of Segmentation Caused by Frequency Aliasing.
</i>
</sub>

<br/>

<sub>
<i>Removed from the main manuscript to comply with the IEEE Regular Paper page limit.</i>
</sub>

</div>

<br/>

**Deleted subsection:**

> ### Failure Case Analysis
>
> Although LS²Net achieves promising segmentation performance, certain limitations still lead to suboptimal results on some images. As illustrated in Fig. \ref{fig:fail}, we present failure cases of LS²Net on the BUSI dataset. During the spatial–frequency interaction process in LS²Net, operations such as convolution, downsampling, and frequency-domain transformation may introduce frequency-domain aliasing when the input signal contains high-frequency components beyond the Nyquist frequency. This aliasing effect, when transformed back into the spatial domain, may manifest as structural artifacts or abnormal textures, resulting in distortions or repetitions in the image. Consequently, these artifacts can interfere with feature extraction, mislead the model in identifying true anatomical structures, and lead to structural inconsistencies, inaccurate boundary localization, and mis-segmentation in local regions.
>
> In future work, the frequency-domain processing can be further improved. Specifically, frequency band selection or adaptive frequency weighting mechanisms can be introduced in the frequency branch to reduce the influence of unreliable high-frequency components on feature representation. In addition, incorporating frequency-domain consistency constraints—such as frequency-domain regularization or consistency loss during training—can help maintain more stable structural representations between the spatial and frequency domains, thereby improving robustness against artifacts.

**Reason for deletion:**

This failure-case analysis and its corresponding figure were removed solely to reduce the manuscript page count. The main methodological contributions and experimental validation of LS²Net remain unchanged.

---
## Deleted Content from Discussion and Conclusion

The following materials were removed from the Discussion and Conclusion section of the manuscript solely to comply with the IEEE Regular Paper page limit. They are preserved here for editorial reference.

### 1. Deleted Discussion and Conclusion: Overall Summary of LS²Net

**Original location:**
Section V, **Discussion and Conclusion**, at the **beginning of the section**.

**Deleted text:**

> Ultrasound imaging, as a widely used medical imaging modality, is applied for the diagnosis of multiple organs and systems throughout the body. To meet the growing clinical demands for accuracy, efficiency, and versatility, modern ultrasound systems are increasingly integrating multiple AI-assisted functions (lesion segmentation). However, deploying these segmentation models directly within ultrasound machines (on-device) for real-time inference is challenging due to the constraints of computational resources, memory capacity, and power consumption. Therefore, developing lightweight and efficient network architectures is essential. To address this need, we propose LS$^2$Net, a lightweight medical image segmentation framework that achieves a balance between segmentation accuracy and computational efficiency. The encoder combines global and local receptive fields to capture multi-scale contextual information, while the decoder employs a multi-receptive field fusion strategy to reconstruct fine-grained features at different levels. The LACS module further refines skip connections to preserve boundary details. Benefiting from these architectural designs, LS$^2$Net achieves a favorable trade-off between accuracy and efficiency, delivering state-of-the-art segmentation performance across five medical scenarios and seven datasets, and demonstrating strong generalization ability on four cross-dataset tests, while significantly reducing computational cost without sacrificing segmentation quality.

**Reason for deletion:**
This introductory summary of the proposed framework and its overall performance was removed solely to reduce the manuscript page count. The key methodology, experimental results, and contributions of LS$^2$Net remain fully presented in the main manuscript.

---

### 2. Deleted Discussion: On-Device Deployment and Real-Time Clinical Applications

**Original location:**
Section V, **Discussion and Conclusion**, immediately after the paragraph summarizing the overall performance of LS$^2$Net.

**Deleted text:**

> LS$^2$Net contains only 0.21M parameters and achieves an inference speed of 96 FPS, making it easily embeddable into ultrasound consoles or portable devices for real-time, on-device segmentation. This capability enables efficient operation directly on the ultrasound platform, allowing real-time segmentation of target regions during image acquisition and substantially enhancing the efficiency and intelligence of ultrasound examinations. Clinically, real-time lesion localization and quantitative visualization during scanning facilitate faster and more accurate diagnosis, which is particularly valuable in emergency, bedside, and primary healthcare settings where computational resources are limited.

**Reason for deletion:**
This discussion was removed solely to reduce the manuscript page count. The lightweight nature and real-time inference capability of LS$^2$Net remain reflected by the reported parameter count and inference speed in the main manuscript.

---

### 3. Deleted Discussion: Cross-Modality Generalization of the Collaborative Receptive Field Paradigm

**Original location:**
Section V, **Discussion and Conclusion**, after the discussion of the real-time on-device deployment capability of LS$^2$Net.

**Deleted text:**

> The collaborative receptive field paradigm integrates multi-scale receptive fields via a multi-branch architecture to jointly model structural and texture information. As it is inherently modality-agnostic, it demonstrates strong cross-modality generalization. In MRI and CT, large receptive fields capture global anatomical structures, while small receptive fields refine local details, enabling effective segmentation across different scales. In histopathology, large receptive fields model tissue-level context, whereas small receptive fields focus on cellular morphology, aligning well with cell-level analysis tasks. Overall, this paradigm provides a unified and flexible framework for multi-scale feature modeling, which can be readily extended to various medical imaging modalities and tasks.

**Reason for deletion:**
This broader discussion of the potential applicability of the collaborative receptive field paradigm to other medical imaging modalities was removed solely to reduce the manuscript page count. The main manuscript retains the core design and validation of the collaborative receptive field paradigm in ultrasound segmentation.

---

### 4. Deleted Discussion: Clinical Deployment and Future Work

**Original location:**
Section V, **Discussion and Conclusion**, after the discussion of the cross-modality generalization potential of LS$^2$Net.

**Deleted text:**

> In real-world clinical settings, imaging devices and computational resources vary significantly across institutions and regions, and the applicability of our model in such diverse environments remains to be further explored. In the future, we plan to deploy LS$^2$Net on edge computing devices and collaborate with clinicians for professional validation to further assess its feasibility and practicality in real-world clinical workflows. Through joint evaluation with medical experts, we aim to investigate the model’s consistency across different disease types, imaging parameters, and operator conditions, thereby confirming its clinical robustness and reliability. Moreover, the generalization capability of LS$^2$Net across various imaging devices and modalities warrants further investigation. We intend to conduct systematic multi-center and multi-device experiments to evaluate its stability and adaptability, enhancing its reliability in diverse clinical scenarios. LS$^2$Net is expected to promote the standardization and generalization of intelligent ultrasound-assisted diagnosis, providing a stable, efficient, and scalable intelligent diagnostic support system for remote areas and primary healthcare institutions.

**Reason for deletion:**
This discussion of clinical deployment, multi-center validation, multi-device generalization, and future research directions was removed solely to reduce the manuscript page count. The removal does not affect the reported experimental findings or the main conclusions of the study.

---

### 5. Deleted Discussion: Fine-Grained Feature Processing and Lightweight Decoder Design

**Original location:**
Section V, **Discussion and Conclusion**, at the **end of the section**.

**Deleted text:**

> LS$^2$Net implements fine-grained processing for different types of features, establishing a coarse-to-fine feature handling strategy that enables diversified feature representations. Meanwhile, the RRSC module optimizes skip connections, effectively reducing the computational burden on the decoder and accelerating feature reconstruction. LS$^2$Net provides a novel approach for lightweight segmentation models that balance performance and speed, offering a practical solution to meet the demands of clinical applications.

**Reason for deletion:**
This concluding discussion was removed solely to reduce the manuscript page count and avoid redundancy with the detailed descriptions of the network architecture and modules provided in the main manuscript. The corresponding methodological contributions and efficiency advantages remain documented elsewhere in the manuscript.

---



