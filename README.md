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




