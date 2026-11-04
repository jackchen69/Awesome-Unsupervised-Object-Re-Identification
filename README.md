<a id="top"></a>
<div align="center">

<img src="fig/banner.png" width="100%" alt="Awesome Unsupervised Object Re-Identification"/>

<p>
  <a href="#"><img src="https://img.shields.io/badge/📄_Paper-arXiv-b31b1b?style=for-the-badge" alt="Paper"/></a>
  <a href="#-demo-what-is-unsupervised-object-re-id"><img src="https://img.shields.io/badge/🎬_Demo-Video-7c3aed?style=for-the-badge" alt="Demo"/></a>
  <a href="https://awesome.re"><img src="https://img.shields.io/badge/Awesome-List-fc60a8?style=for-the-badge&logo=awesomelists&logoColor=white" alt="Awesome"/></a>
  <a href="#-contributing"><img src="https://img.shields.io/badge/PRs-Welcome-22c55e?style=for-the-badge" alt="PRs"/></a>
</p>
<p>
  <img src="https://img.shields.io/github/stars/YOUR_ORG/Awesome-Unsupervised-ReID?style=flat-square&logo=github&color=f59e0b" alt="Stars"/>
  <img src="https://img.shields.io/github/forks/YOUR_ORG/Awesome-Unsupervised-ReID?style=flat-square&logo=github&color=3b82f6" alt="Forks"/>
  <img src="https://img.shields.io/github/last-commit/YOUR_ORG/Awesome-Unsupervised-ReID?style=flat-square&color=10b981" alt="Last commit"/>
  <img src="https://img.shields.io/badge/Research_Areas-5-8b5cf6?style=flat-square" alt="Areas"/>
  <img src="https://img.shields.io/badge/Objects-Person·Vehicle·Animal·Vessel-ec4899?style=flat-square" alt="Objects"/>
</p>

**[🎬 Demo](#-demo-what-is-unsupervised-object-re-id)** ·
**[📖 Introduction](#-introduction)** ·
**[🗺️ Taxonomy](#️-taxonomy)** ·
**[📚 Papers](#-paper-list)** ·
**[🗃️ Datasets](#️-datasets)** ·
**[🔭 Future](#-future-directions)** ·
**[📝 Citation](#-citation)**

</div>

> [!NOTE]
> This repository accompanies our survey **"Unsupervised Object Re-Identification: Recent Advances, Challenges, and Future Directions"** — to our knowledge, the **first dedicated survey** of unsupervised Re-ID across **persons, vehicles, animals, and vessels**. ⭐ **Star** the repo to follow updates, and PRs are always welcome!

---

## 🔥 News

- **`2026-11`** 🎬 A 1-minute **animated demo** explaining unsupervised Re-ID is released ([MP4](fig/demo.mp4)).
- **`2026-11`** 🎉 The awesome list is released, covering **5 research areas** and **VLM-based** unsupervised Re-ID.
- **`2026-xx`** 📄 Our survey is available on [arXiv](#).

---

## 🎬 Demo: What is Unsupervised Object Re-ID?

<div align="center">

<a href="fig/demo.mp4"><img src="fig/demo.gif" width="88%" alt="Demo: what is unsupervised object re-identification"/></a>

<sub>▶️ <b>Click the animation to download the full-resolution 1080p video</b> (<a href="fig/demo.mp4"><code>fig/demo.mp4</code></a>, 55 s)</sub>

</div>

<table>
<tr>
<td align="center" width="14%"><b>①</b><br/><sub>What is Re-ID?</sub></td>
<td align="center" width="14%"><b>②</b><br/><sub>Matching across cameras</sub></td>
<td align="center" width="14%"><b>③</b><br/><sub>The annotation bottleneck</sub></td>
<td align="center" width="16%"><b>④</b><br/><sub>Cluster → pseudo-label → train</sub></td>
<td align="center" width="14%"><b>⑤</b><br/><sub>Why it is hard</sub></td>
<td align="center" width="14%"><b>⑥</b><br/><sub>VLM guidance</sub></td>
<td align="center" width="14%"><b>⑦</b><br/><sub>Survey scope</sub></td>
</tr>
</table>

---

## 📖 Introduction

**Object Re-Identification (Re-ID)** retrieves all images of the same identity — a person, vehicle, animal, or vessel — across **non-overlapping cameras**. **Unsupervised Re-ID** learns this ability **without target-domain identity annotations**, which makes Re-ID systems scalable to new environments and privacy-sensitive deployments.

<p align="center">
  <img src="fig/reid_process.png" width="96%" alt="Generic object Re-ID process"/>
  <br/><sub><b>Fig. 1.</b> The generic object Re-ID process: a query is encoded and used to rank a cross-camera gallery.</sub>
</p>

<p align="center">
  <img src="fig/settings.png" width="96%" alt="Supervised, UDA and USL settings"/>
  <br/><sub><b>Fig. 2.</b> Learning settings. <b>UDA</b> uses a labeled source domain; <b>USL</b> uses no labeled Re-ID data at all.</sub>
</p>

### ✨ Highlights of this survey

<table>
<tr>
<td width="25%" align="center">🗂️<br/><b>5 Research Areas</b><br/><sub>image · video · cross-modal · scenario-specific · emerging</sub></td>
<td width="25%" align="center">🔍<br/><b>Mechanism-centric</b><br/><sub>how supervision & identity associations are built — and where they fail</sub></td>
<td width="25%" align="center">🧠<br/><b>VLM Analysis</b><br/><sub>text augmentation, prompt learning, dual-centroid experiment</sub></td>
<td width="25%" align="center">🚀<br/><b>Future Directions</b><br/><sub>VLM · multi-modality · federated · lifelong · lightweight</sub></td>
</tr>
</table>

<details>
<summary><b>📊 Comparison with existing Re-ID surveys</b> (click to expand)</summary>
<br/>

| Survey | Venue | 👤 Person | 🚗 Vehicle | 🐯 Animal | 🚢 Vessel | Focus |
|:--|:--:|:--:|:--:|:--:|:--:|:--|
| Deep Learning for Person Re-ID: A Survey and Outlook | ![](https://img.shields.io/badge/TPAMI-2021-1f6feb?style=flat-square) | ✅ | | | | General person Re-ID |
| Deep Learning for Visible-Infrared Cross-Modality Person Re-ID: A Comprehensive Review | ![](https://img.shields.io/badge/IF-2022-0891b2?style=flat-square) | ✅ | | | | Visible-infrared |
| Person Re-ID: A Retrospective on Domain Specific Open Challenges and Future Trends | ![](https://img.shields.io/badge/PR-2023-0891b2?style=flat-square) | ✅ | | | | Application challenges |
| Transformer for Object Re-Identification: A Survey | ![](https://img.shields.io/badge/IJCV-2024-1f6feb?style=flat-square) | ✅ | ✅ | ✅ | | Transformers |
| From Attributes to Natural Language: Text-based Person Re-ID | ![](https://img.shields.io/badge/IF-2025-0891b2?style=flat-square) | ✅ | | | | Text-based retrieval |
| Vision-Language Models for Person Re-ID: A Survey and Outlook | ![](https://img.shields.io/badge/IF-2026-0891b2?style=flat-square) | ✅ | | | | VLMs |
| 🌟 **Ours** | ![](https://img.shields.io/badge/arXiv-2026-b31b1b?style=flat-square) | ✅ | ✅ | ✅ | ✅ | **Unsupervised Re-ID** |

</details>

---

## 🗺️ Taxonomy

<p align="center">
  <img src="fig/taxonomy.png" width="96%" alt="Taxonomy"/>
  <br/><sub><b>Fig. 3.</b> We organize unsupervised object Re-ID into five research areas plus a dedicated VLM analysis.</sub>
</p>

<p align="center">
  <img src="fig/timeline.png" width="96%" alt="Timeline"/>
  <br/><sub><b>Fig. 4.</b> Representative milestones (2018 – 2026), colored by research area.</sub>
</p>

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

## 📚 Paper List

<details>
<summary><b>🔖 Badge legend</b></summary>
<br/>

| Badge | Meaning |
|:--|:--|
| ![](https://img.shields.io/badge/CVPR-2022-1f6feb?style=flat-square) | Top conference (CVPR / ICCV / ECCV / NeurIPS / ICLR / ICML / AAAI) |
| ![](https://img.shields.io/badge/TIP-2021-0891b2?style=flat-square) | Journal (TPAMI / TIP / IJCV / PR / IF / TOMM …) |
| ![](https://img.shields.io/badge/ACM%20MM-2023-7c3aed?style=flat-square) | ACM MM / BMVC / ACCV / WACV |
| ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | Venue to be updated |
| ![](https://img.shields.io/badge/UDA-f97316?style=flat-square) ![](https://img.shields.io/badge/USL-22c55e?style=flat-square) | With / without labeled source Re-ID data |

</details>

### 🧱 Technical Foundations

<p align="center"><img src="fig/usl_pipeline.png" width="96%" alt="Clustering-based USL pipeline"/></p>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **PUL** | Unsupervised Person Re-identification: Clustering and Fine-tuning | ![](https://img.shields.io/badge/TOMM-2018-0891b2?style=flat-square) | – |
| **BUC** | A Bottom-up Clustering Approach to Unsupervised Person Re-identification | ![](https://img.shields.io/badge/AAAI-2019-1f6feb?style=flat-square) | – |
| **MoCo** | Momentum Contrast for Unsupervised Visual Representation Learning | ![](https://img.shields.io/badge/CVPR-2020-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/facebookresearch/moco?style=social)](https://github.com/facebookresearch/moco) |
| **SimCLR** | A Simple Framework for Contrastive Learning of Visual Representations | ![](https://img.shields.io/badge/ICML-2020-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/google-research/simclr?style=social)](https://github.com/google-research/simclr) |
| **MMT** | Mutual Mean-Teaching: Pseudo Label Refinery for Unsupervised Domain Adaptation on Person Re-identification | ![](https://img.shields.io/badge/ICLR-2020-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/yxgeee/MMT?style=social)](https://github.com/yxgeee/MMT) |
| **SpCL** | Self-paced Contrastive Learning with Hybrid Memory for Domain Adaptive Object Re-ID | ![](https://img.shields.io/badge/NeurIPS-2020-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/yxgeee/SpCL?style=social)](https://github.com/yxgeee/SpCL) |
| **Cluster Contrast** | Cluster Contrast for Unsupervised Person Re-Identification | ![](https://img.shields.io/badge/ACCV-2022-7c3aed?style=flat-square) | [![](https://img.shields.io/github/stars/alibaba/cluster-contrast-reid?style=social)](https://github.com/alibaba/cluster-contrast-reid) |
| **HCL** | Hybrid contrastive learning (instance + cluster) | ![](https://img.shields.io/badge/Venue-2022-9ca3af?style=flat-square) | – |

<details>
<summary><b>📐 ClusterNCE loss</b></summary>

$$
\mathcal{L}_{\mathrm{ClusterNCE}} = -\frac{1}{B}\sum_{i=1}^{B}\log\frac{\exp(\mathbf{f}_i\cdot\mathbf{w}_{y_i}/\tau)}{\sum_{j=1}^{C}\exp(\mathbf{f}_i\cdot\mathbf{w}_j/\tau)}
$$

where $\mathbf{f}_i$ is the $\ell_2$-normalized feature, $\mathbf{w}_j$ the $j$-th cluster prototype, $y_i$ the pseudo-label and $\tau$ the temperature.

</details>

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

### 🖼️ Image-based Unsupervised Re-ID

#### ![](https://img.shields.io/badge/UDA-f97316?style=flat-square) Unsupervised Domain Adaptation

<p align="center"><img src="fig/uda_paradigms.png" width="96%" alt="UDA paradigms"/></p>

<details open>
<summary><b>① Feature-level Adaptation</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **MMFA** | Multi-task Mid-level Feature Alignment Network for Unsupervised Cross-Dataset Person Re-Identification | ![](https://img.shields.io/badge/BMVC-2018-7c3aed?style=flat-square) | – |
| **TJ-AIDL** | Transferable Joint Attribute-Identity Deep Learning for Unsupervised Person Re-Identification | ![](https://img.shields.io/badge/CVPR-2018-1f6feb?style=flat-square) | – |
| **TFusion** | Unsupervised Cross-dataset Person Re-identification by Transfer Learning of Spatial-Temporal Patterns | ![](https://img.shields.io/badge/CVPR-2018-1f6feb?style=flat-square) | – |
| **SAM-MAE** | SAM-driven MAE pre-training for identity-sensitive regions | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **F2TD-ReID** | Transitional representations via dictionary fusion | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |

</details>

<details open>
<summary><b>② Image-level Adaptation</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **PTGAN** | Person Transfer GAN to Bridge Domain Gap for Person Re-Identification | ![](https://img.shields.io/badge/CVPR-2018-1f6feb?style=flat-square) | – |
| **SPGAN** | Image-Image Domain Adaptation with Preserved Self-Similarity and Domain-Dissimilarity for Person Re-ID | ![](https://img.shields.io/badge/CVPR-2018-1f6feb?style=flat-square) | – |
| **HHL** | Generalizing A Person Retrieval Model Hetero- and Homogeneously | ![](https://img.shields.io/badge/ECCV-2018-1f6feb?style=flat-square) | – |
| **IPES-GAN** | Identity / environment disentangled translation | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **TAL-MIRN** | Geometry-constrained identity-consistent translation | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **DREAMT** | GAN translation + cross-branch mutual learning | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **DAPRH** | Multi-style synthesis for pseudo-label refinement | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |

</details>

<details open>
<summary><b>③ Clustering-based Self-training</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **MMT** | Mutual Mean-Teaching: Pseudo Label Refinery for UDA on Person Re-ID | ![](https://img.shields.io/badge/ICLR-2020-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/yxgeee/MMT?style=social)](https://github.com/yxgeee/MMT) |
| **SpCL** | Self-paced Contrastive Learning with Hybrid Memory | ![](https://img.shields.io/badge/NeurIPS-2020-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/yxgeee/SpCL?style=social)](https://github.com/yxgeee/SpCL) |
| **UCF** | Uncertainty-aware clustering framework | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **TRSL** | Curriculum-based reliable self-training | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **DMD** | Multi-branch cooperation against noisy labels | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **PDBN** | Multi-branch noise-robust learning | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **CaCL** | Camera-aware curriculum learning | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **TDSR** | Transformer-based self-training | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **MATNet** | Transformer for fine-grained discrimination | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **IDENet** | Inter-domain balancing framework | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |
| **Fed-UDA** | Federated UDA without centralizing raw images | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | – |

</details>

#### ![](https://img.shields.io/badge/USL-22c55e?style=flat-square) Unsupervised Learning

<details open>
<summary><b>① Pseudo-Label Generation & Optimization</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **BUC** | A Bottom-up Clustering Approach to Unsupervised Person Re-identification | ![](https://img.shields.io/badge/AAAI-2019-1f6feb?style=flat-square) | – |
| **HCT** | Hierarchical Clustering with Hard-batch Triplet Loss for Person Re-identification | ![](https://img.shields.io/badge/CVPR-2020-1f6feb?style=flat-square) | – |
| **ICE** | ICE: Inter-instance Contrastive Encoding for Unsupervised Person Re-identification | ![](https://img.shields.io/badge/ICCV-2021-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/chenhao2345/ICE?style=social)](https://github.com/chenhao2345/ICE) |
| **RLCC** | Refining Pseudo Labels with Clustering Consensus over Generations for Unsupervised Object Re-ID | ![](https://img.shields.io/badge/CVPR-2021-1f6feb?style=flat-square) | – |
| **ISE** | Implicit Sample Extension for Unsupervised Person Re-Identification | ![](https://img.shields.io/badge/CVPR-2022-1f6feb?style=flat-square) | – |
| **PPLR** | Part-based Pseudo Label Refinement for Unsupervised Person Re-identification | ![](https://img.shields.io/badge/CVPR-2022-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/yoonkicho/PPLR?style=social)](https://github.com/yoonkicho/PPLR) |
| **Plug-in Graph** | KNN-graph-based pseudo-label refinement | ![](https://img.shields.io/badge/Venue-2022-9ca3af?style=flat-square) | – |
| **Real-time Memory** | Real-time memory updating for clustering–contrast alignment | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | – |
| **Confidence-guided** | Silhouette-score-guided centroid selection | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |

</details>

<details open>
<summary><b>② Feature Representation Enhancement</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **TMGF** | Transformer Based Multi-Grained Features for Unsupervised Person Re-Identification | ![](https://img.shields.io/badge/WACVW-2023-7c3aed?style=flat-square) | – |
| **Multi-Expert** | Multi-expert feature aggregation | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | – |
| **Discriminative** | Identity-focused discriminative feature learning | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | – |
| **Joint Local Attn.** | Local attention for USL Re-ID | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **Multi-scale Attn.** | Multi-scale attention for USL Re-ID | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **DSG** | Disentangled sample guidance | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **Gen-Aug** | Generative positive-pair augmentation | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **VL-Graph** | Vision-language constraint graph learning | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **Large-scale Sampling** | Sampling strategies for USL Re-ID | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **Dual Distill** | Multi-view pseudo-label knowledge distillation | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **TCRL** | Triplet cluster representation learning | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **ACSA** | Mask-guided asymmetric contrast & distribution alignment | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | – |
| **AF2MA** | Regional fusion + instance/cluster memory augmentation | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | – |

</details>

<details open>
<summary><b>③ Camera Bias Mitigation</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **SSL** | Unsupervised Person Re-identification via Softened Similarity Learning | ![](https://img.shields.io/badge/CVPR-2020-1f6feb?style=flat-square) | – |
| **CAP** | Camera-aware Proxies for Unsupervised Person Re-Identification | ![](https://img.shields.io/badge/AAAI-2021-1f6feb?style=flat-square) | – |
| **CCIO** | Camera-aware online K-reciprocal mining | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **Hier. Contrast** | Hierarchical camera-aware contrastive learning | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **CGMAL** | Camera-aware graph propagation | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **FedCAPR** | Federated camera-aware proxy refinement | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |

</details>

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

### 🎞️ Video-based Unsupervised Re-ID

| Method | Title | Venue | Type |
|:--:|:--|:--:|:--:|
| **RACE** | Robust Anchor Embedding for Unsupervised Video Person Re-Identification in the Wild | ![](https://img.shields.io/badge/ECCV-2018-1f6feb?style=flat-square) | 🎯 Intra-tracklet |
| **DBC** | Dispersion based Clustering for Unsupervised Person Re-identification | ![](https://img.shields.io/badge/BMVC-2019-7c3aed?style=flat-square) | 🎯 Intra-tracklet |
| **TASTC** | Camera topology & spatio-temporal constraints | ![](https://img.shields.io/badge/Venue-2020-9ca3af?style=flat-square) | 🧭 Auxiliary cue |
| **NHAC** | Dynamic frame filtering & re-weighting | ![](https://img.shields.io/badge/Venue-2021-9ca3af?style=flat-square) | 🎯 Intra-tracklet |
| **SRC** | Noisy-frame trimming & re-weighting | ![](https://img.shields.io/badge/Venue-2021-9ca3af?style=flat-square) | 🎯 Intra-tracklet |
| **MCGA** | Multi-context grouped attention | ![](https://img.shields.io/badge/Venue-2021-9ca3af?style=flat-square) | 🎯 Intra-tracklet |
| **SCC** | Successive clustering consensus | ![](https://img.shields.io/badge/Venue-2022-9ca3af?style=flat-square) | 🎯 Intra-tracklet |
| **VLUReID** | Vision-language pretraining for video Re-ID | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | 🧭 Auxiliary cue |
| **DRMPCL** | Discrepant prototypes + progressive contrast | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | 🎯 Intra-tracklet |
| **SSR-C** | Sub-tracklet relation-based cluster refinement | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | 🎯 Intra-tracklet |
| **UMTF** | Visual features + wireless positioning trajectories | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | 🧭 Auxiliary cue |
| **Wang et al.** | Spatio-temporal co-occurrence & group movement | ![](https://img.shields.io/badge/Venue-TBD-9ca3af?style=flat-square) | 🧭 Auxiliary cue |

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

### 🔀 Cross-modal Unsupervised Re-ID

<p align="center"><img src="fig/crossmodal.png" width="96%" alt="Cross-modal Re-ID"/></p>

#### 📝 Text-to-Image Re-ID

| Method | Title | Venue | Type |
|:--:|:--|:--:|:--:|
| **CMMT** | Weakly Supervised Text-based Person Re-Identification | ![](https://img.shields.io/badge/ICCV-2021-1f6feb?style=flat-square) | 🔗 Paired data |
| **CANC** | CLIP-based cross-modal neighbor completion | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | 🧩 Completion |
| **ECCA** | Graph-enhanced completion & alignment | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | 🧩 Completion |
| **CCL** | Contrastive completion learning | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | 🧩 Completion |
| **WIN** | Multi-granularity reciprocal-neighbor completion | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | 🧩 Completion |
| **MUMA** | Multi-grained LVLM captions + uncertainty filtering | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | ✍️ Caption gen. |
| **GTR+** | Generative description refinement + confidence weighting | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | ✍️ Caption gen. |

#### 🌗 Visible-Infrared Re-ID

<details open>
<summary><b>① Pseudo-Label Learning with Clustering & Contrast</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **ADCA** | Augmented Dual-Contrastive Aggregation Learning for Unsupervised Visible-Infrared Person Re-ID | ![](https://img.shields.io/badge/ACM%20MM-2022-7c3aed?style=flat-square) | [![](https://img.shields.io/github/stars/yangbincv/ADCA?style=social)](https://github.com/yangbincv/ADCA) |
| **DCCL** | Dual-consistency collaborative learning | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | – |
| **SDCL** | Shallow-Deep Collaborative Learning for Unsupervised Visible-Infrared Person Re-ID | ![](https://img.shields.io/badge/CVPR-2024-1f6feb?style=flat-square) | – |
| **PCLHD** | Learning Commonality, Divergence and Variety for Unsupervised Visible-Infrared Person Re-ID | ![](https://img.shields.io/badge/NeurIPS-2024-1f6feb?style=flat-square) | – |
| **RPNR** | Robust Pseudo-label Learning with Neighbor Relation for Unsupervised VI-ReID | ![](https://img.shields.io/badge/ACM%20MM-2024-7c3aed?style=flat-square) | – |
| **PCM** | Part-based cross-modal learning | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **APPD** | Adaptive neighbor-relation calibration | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **PBE** | Part-based enhancement | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **DCM** | Multi-level dual-stream camera/modality learning | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **RoDE** | Robust duality learning | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **ADAL** | Evolutionary optimization for USL-VI-ReID | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **ACH** | Adaptive confidence & cross-modal hard mining | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | – |

</details>

<details open>
<summary><b>② Structure-aware Matching & Refinement</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **H2H** | Homogeneous-to-Heterogeneous: Unsupervised Learning for RGB-Infrared Person Re-ID | ![](https://img.shields.io/badge/TIP-2021-0891b2?style=flat-square) | – |
| **PGM** | Unsupervised VI-ReID via Progressive Graph Matching and Alternate Learning | ![](https://img.shields.io/badge/CVPR-2023-1f6feb?style=flat-square) | – |
| **GUR** | Towards Grand Unified Representation Learning for Unsupervised VI-ReID | ![](https://img.shields.io/badge/ICCV-2023-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/yangbincv/GUR?style=social)](https://github.com/yangbincv/GUR) |
| **MBCCM** | Efficient Bilateral Cross-Modality Cluster Matching for Unsupervised VI-ReID | ![](https://img.shields.io/badge/ACM%20MM-2023-7c3aed?style=flat-square) | – |
| **DOTLA** | Optimal-transport prototype alignment | ![](https://img.shields.io/badge/ACM%20MM-2023-7c3aed?style=flat-square) | – |
| **CHCR** | Cross-modal hierarchical clustering | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | – |
| **MMM** | Multi-Memory Matching for Unsupervised Visible-Infrared Person Re-ID | ![](https://img.shields.io/badge/ECCV-2024-1f6feb?style=flat-square) | – |
| **BCGM** | Bidirectional consistency graph matching | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **DLM** | Dual neighbor-based label matching | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **RULN** | Relieving label noise via neighbor inference | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **ECUL** | Extended cross-modal unified learning | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **SSRL** | Body-part cues with reconstructed shared prototypes | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | – |
| **HiTPro** | Hierarchical temporal prototypes (video VI-ReID) | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | – |

</details>

<details open>
<summary><b>③ Auxiliary Priors & Semantic Guidance</b></summary>
<br/>

| Method | Title | Venue | Code |
|:--:|:--|:--:|:--:|
| **CCLNet** | Unveiling the Power of CLIP in Unsupervised Visible-Infrared Person Re-ID | ![](https://img.shields.io/badge/ACM%20MM-2023-7c3aed?style=flat-square) | – |
| **SCA-RCP** | Camera-aware inter-/intra-modality learning | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **CMAM** | Asymmetric mutual learning via grayscale coupling | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | – |
| **TGMRL** | Text-guided multimodal representation learning | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **CEIL** | Camera-aware invariance learning | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **HCCL** | Hierarchical centrality consistency learning | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |
| **TokenMatcher** | Token-level cross-modal matching | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | – |

</details>

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

### 🎭 Scenario-specific Unsupervised Re-ID

<p align="center"><img src="fig/scenarios.png" width="96%" alt="Scenario-specific challenges"/></p>

<table>
<tr>
<th width="33%">👕 Clothing-Change</th>
<th width="33%">🔍 Cross-Resolution</th>
<th width="33%">👥 Group</th>
</tr>
<tr valign="top">
<td>

- **CPC** · Unsupervised Long-Term Person Re-ID with Clothes Change · ![](https://img.shields.io/badge/ICML-2023-1f6feb?style=flat-square)
- **SiCL** · Silhouette-driven contrastive learning · ![](https://img.shields.io/badge/arXiv-2023-b31b1b?style=flat-square)
- **CICL** · Clothing-invariant contrastive learning · ![](https://img.shields.io/badge/-2024-9ca3af?style=flat-square)
- **ICSM** · Identity-clothing similarity modeling · ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square)
- **JAPL** · Joint augmentation & part learning · ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square)

</td>
<td>

- **DRFM** · Dual-resolution feature fusion with SR · ![](https://img.shields.io/badge/-2024-9ca3af?style=flat-square)
- **ITSL** · Image-text semantic learning · ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square)
- **RLIM** · Robust labeling & resolution-cluster consistency · ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square)
- **ITKM** · Scenario-conditioned image-text joint learning · ![](https://img.shields.io/badge/-TBD-9ca3af?style=flat-square)

</td>
<td>

- **Mei et al.** · Supervised predecessor (background) · ![](https://img.shields.io/badge/-2020-9ca3af?style=flat-square)
- **Yu et al.** · Patch-based camera-aware + modified Hausdorff · ![](https://img.shields.io/badge/-2023-9ca3af?style=flat-square)
- **Chen et al.** · Adaptive clustering with quasi-distance vectors · ![](https://img.shields.io/badge/-2024-9ca3af?style=flat-square)
- **Chen et al.** · Strategic member harmonization (aerial) · ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square)

</td>
</tr>
</table>

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

### 🐾 Emerging Tasks

<p align="center"><img src="fig/emerging.png" width="96%" alt="Animal and vessel Re-ID"/></p>

#### 🚢 Vessel Re-ID

| Method | Title | Venue | Setting |
|:--:|:--|:--:|:--:|
| **MCL** | Multi-level contrastive learning (VesselReID) | ![](https://img.shields.io/badge/Venue-2023-9ca3af?style=flat-square) | ![](https://img.shields.io/badge/USL-22c55e?style=flat-square) |
| **IMCL** | Improved momentum contrast, military-civilian cross-domain | ![](https://img.shields.io/badge/Venue-2024-9ca3af?style=flat-square) | Cross-domain |
| **CCL** | Bridging the clustering–training gap | ![](https://img.shields.io/badge/Venue-2025-9ca3af?style=flat-square) | ![](https://img.shields.io/badge/USL-22c55e?style=flat-square) |
| **VAMN** | View-invariant learning via multi-frequency phase modulation | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | ![](https://img.shields.io/badge/USL-22c55e?style=flat-square) |
| **DGSC** | Density-guided clustering with progressive training | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | ![](https://img.shields.io/badge/UDA-f97316?style=flat-square) |
| **Nezhad et al.** | Self-supervised optical satellite ship identification | ![](https://img.shields.io/badge/Venue-2026-9ca3af?style=flat-square) | Self-supervised |

#### 🐯 Animal Re-ID

| Method | Title | Venue | Species | Type |
|:--:|:--|:--:|:--:|:--:|
| **Gao et al.** | Towards Self-Supervision for Video Identification of Individual Holstein-Friesian Cattle: The Cows2021 Dataset | ![](https://img.shields.io/badge/-2021-9ca3af?style=flat-square) | 🐄 Cattle | 🎞️ Tracklet |
| **Chan et al.** | Self-supervised honeybee Re-ID from short-term tracks | ![](https://img.shields.io/badge/-2022-9ca3af?style=flat-square) | 🐝 Honeybee | 🎞️ Tracklet |
| **Dubourvieux et al.** | Cumulative domain adaptation across farms | ![](https://img.shields.io/badge/-2023-9ca3af?style=flat-square) | 🐄 Cattle | 🖼️ Appearance |
| **Zhang et al.** | Feature-aware noise contrastive learning | ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square) | 🐼 Red panda | 🖼️ Appearance |
| **Liu & Zhao** | Part-attention pseudo-label refinement | ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square) | 🐄 Cattle face | 🖼️ Appearance |
| **Algasov et al.** | Unsupervised pelage pattern unwrapping | ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square) | 🦭 Seal / 🐆 Leopard | 🖼️ Appearance |
| **Williams et al.** | Tracklet-association animal Re-ID | ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square) | – | 🎞️ Tracklet |
| **Mask-TAUDL** | Mask-based tracklet association unsupervised learning | ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square) | – | 🎞️ Tracklet |
| **Yu et al.** | Detect-segment-identify for dense herds | ![](https://img.shields.io/badge/-2025-9ca3af?style=flat-square) | 🐄 Cattle | 🎞️ Tracklet |
| **Yu et al.** | Multi-camera cattle Re-ID with tracklet pseudo-labels | ![](https://img.shields.io/badge/-TBD-9ca3af?style=flat-square) | 🐄 Cattle | 🎞️ Tracklet |
| **Muthivhi & van Zyl** | Temporal pair mining from camera traps | ![](https://img.shields.io/badge/-TBD-9ca3af?style=flat-square) | 🦓 Wildlife | 🎞️ Tracklet |
| **Pose-aware Proxy** | Orientation-weakly-supervised contrastive learning | ![](https://img.shields.io/badge/-2026-9ca3af?style=flat-square) | 🦈 Thresher shark | 🎞️ Tracklet |

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

### 🧠 VLM-based Unsupervised Re-ID

<p align="center"><img src="fig/vlm_framework.png" width="96%" alt="From visual to VLM-based framework"/></p>

<table>
<tr>
<th width="50%">✍️ Text Augmentation</th>
<th width="50%">💬 Prompt Learning</th>
</tr>
<tr valign="top">
<td>

| Method | Task |
|:--|:--:|
| **MUMA** | Text → Image |
| **LVLM-AAM** | VIS ↔ IR |
| **FIRM** | VIS ↔ IR |
| **CANC** / **ECCA** | Text → Image |
| **CCL** / **WIN** | Text → Image |

</td>
<td>

| Method | Task |
|:--|:--:|
| **CLIP-ReID** [![](https://img.shields.io/github/stars/Syliz517/CLIP-ReID?style=social)](https://github.com/Syliz517/CLIP-ReID) | Image (sup. basis) |
| **CCLNet** | VIS ↔ IR |
| **VLUReID** | Video |
| **ViewCoOp** | Vehicle |
| **TGMRL** | VIS ↔ IR |
| **ICSM** | Clothing-change |
| **ITSL** | Cross-resolution |
| **Partial-wise Prompts** | Image |
| **Day-Night Prompts** | Vehicle |

</td>
</tr>
</table>

#### 🧪 Illustrative Experiment · Visual-Textual Dual Centroids

> Backbone: **CLIP ViT-B/16** · Setting: **USL** · Loss: **ClusterNCE** on both centroids · Prompt: `"A photo of [CLS] person"`

<p align="center"><img src="fig/dual_centroid.png" width="92%" alt="Dual-centroid results"/></p>

<div align="center">

| Dataset | Method | mAP | Rank-1 | Rank-10 |
|:--:|:--|:--:|:--:|:--:|
| **Market-1501** | Pure-visual | 85.2 | 93.2 | 98.2 |
| | 🌟 **Visual + Textual** | **85.8** <sub>🔺0.6</sub> | **93.6** <sub>🔺0.4</sub> | **98.5** <sub>🔺0.3</sub> |
| **DukeMTMC-reID** | Pure-visual | 67.9 | 80.8 | 90.4 |
| | 🌟 **Visual + Textual** | **69.1** <sub>🔺1.2</sub> | **81.1** <sub>🔺0.3</sub> | **91.1** <sub>🔺0.7</sub> |
| **MSMT17** | Pure-visual | 60.6 | 81.1 | 90.5 |
| | 🌟 **Visual + Textual** | **61.8** <sub>🔺1.2</sub> | **81.4** <sub>🔺0.3</sub> | **90.5** <sub>±0.0</sub> |

</div>

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

## 🗃️ Datasets

<p align="center"><img src="fig/datasets.png" width="92%" alt="Datasets overview"/></p>

<details open>
<summary><b>👤🚗 Person & Vehicle Datasets</b></summary>
<br/>

| Category | Dataset | Year | Samples | IDs | Object |
|:--:|:--|:--:|--:|--:|:--:|
| 🖼️ **Image** | Market-1501 | 2015 | 32,217 | 1,501 | 👤 |
| | DukeMTMC-reID | 2017 | 36,441 | 1,812 | 👤 |
| | MSMT17 | 2018 | 126,441 | 4,101 | 👤 |
| | VehicleID | 2016 | 221,763 | 26,267 | 🚗 |
| | VeRi-776 | 2016 | 49,357 | 776 | 🚗 |
| | VERI-Wild | 2019 | 416,314 | 40,671 | 🚗 |
| | Truck-ReID | 2023 | 32,353 | 13,137 | 🚚 |
| 🎞️ **Video** | MARS | 2016 | 20,715 | 1,261 | 👤 |
| | LPW | 2018 | 7,694 | 2,731 | 👤 |
| | DukeMTMC-VideoReID | 2018 | 4,832 | 1,404 | 👤 |
| 📝 **Image-Text** | CUHK-PEDES | 2017 | 40,206 / 80,422 | 13,003 | 👤 |
| | ICFG-PEDES | 2021 | 54,522 / 54,522 | 4,102 | 👤 |
| | RSTPReid | 2021 | 20,505 / 41,010 | 4,101 | 👤 |
| 🌗 **VIS-IR** | RegDB | 2017 | 4,120 / 4,120 | 412 | 👤 |
| | SYSU-MM01 | 2017 | 20,284 / 9,929 | 296 | 👤 |
| 👕 **Cloth-Changing** | PRCC | 2019 | 33,698 | 221 | 👤 |
| | Celeb-reID | 2019 | 34,186 | 1,052 | 👤 |
| | Celeb-reID-light | 2019 | 10,842 | 590 | 👤 |
| | VC-Clothes | 2020 | 19,060 | 256 | 👤 |
| | LTCC | 2020 | 17,119 | 152 | 👤 |
| 🔍 **Cross-Resolution** | CAVIAR | 2011 | 1,220 | 72 | 👤 |
| | MLR-CUHK03 | 2014 | 13,164 | 1,467 | 👤 |
| | D-Market-1501 | 2024 | 32,668 | 1,501 | 👤 |
| 👥 **Group** | RoadGroup | 2019 | 324 | 162 | 👥 |
| | SYSUGroup | 2020 | 7,071 | 208 | 👥 |

</details>

<details open>
<summary><b>🚢🐯 Vessel & Animal Datasets</b></summary>
<br/>

| Dataset | Year | Images | IDs | Species | Modality | Source |
|:--|:--:|--:|--:|:--:|:--:|:--|
| Boat Re-ID | 2019 | 5,523 | 107 | 🚢 Vessel | RGB | Coastal camera |
| VesselReID | 2023 | 30,587 | 1,248 | 🚢 Vessel | RGB | Ship spotting website |
| Warships-ReID | 2023 | 4,780 | 163 | 🚢 Vessel | RGB | Ship imaging website |
| CMShipReID | 2025 | 8,337 | 138 | 🚢 Vessel | VIS / NIR / TIR | UAV capture |
| HolsteinCattleRecog | 2018 | 1,237 | 136 | 🐄 Holstein | RGB + Thermal | Milking parlor |
| ATRW | 2019 | 3,649 | 92 | 🐯 Amur tiger | RGB (video) | Camera traps / zoos |
| ELPephants | 2019 | 2,078 | 276 | 🐘 Elephant | RGB | Wildlife sanctuaries |
| YakReID-103 | 2021 | 2,247 | 103 | 🐂 Yak | RGB | Outdoor farm |
| Cows2021 | 2021 | 13,784 | 182 | 🐄 Cattle | RGB (video) | Overhead cameras |
| RedPanda | 2025 | 3,487 | 43 | 🐼 Red panda | RGB | Enclosure cameras |
| CattleFace2025 | 2025 | 11,880 | 574 | 🐄 Holstein & Simmental | RGB | Ranch cameras |
| ThresherShark | 2025 | – | – | 🦈 Thresher shark | RGB (video) | Diver-held cams |
| HolsteinFriesianCrowd | 2026 | 524,469 | – | 🐄 Holstein | RGB | Farm CCTV |

</details>

### 📏 Evaluation Metrics

| Metric | Description |
|:--:|:--|
| **CMC / Rank-k** | Fraction of queries with a correct match in the top-*k* results |
| **mAP** | Mean of query-level Average Precision over all relevant gallery samples |
| **mINP** | Mean Inverse Negative Penalty — $\mathrm{INP}_i = N_i^+ / r_i^{\mathrm{last}}$, measures how early the *last* correct match appears |

<p align="right"><a href="#top">🔝 Back to top</a></p>

---

## 🔭 Future Directions

<p align="center"><img src="fig/future.png" width="96%" alt="Future directions"/></p>

| Direction | Key open problem |
|:--|:--|
| 🧠 **Meeting VLMs** | Use VLMs as dynamic *semantic verifiers* for pseudo-label correction, not only as feature extractors |
| 🌈 **Multi-Modality** | Cluster by identity rather than by sensor across RGB / NIR / TIR / sketch, with arbitrary missing modalities |
| 🔒 **Federated Learning** | Cross-client pseudo-label alignment and fairness-aware aggregation beyond size weighting |
| ♾️ **Lifelong Re-ID** | Avoid catastrophic forgetting *and* pseudo-label drift on continuous unlabeled streams |
| ⚡ **Lightweight Deployment** | Compact backbones, pruning, quantization and distillation for edge devices |

---

## 📝 Citation

If you find this survey or repository helpful, please consider giving a ⭐ and citing:

```bibtex
@article{unsupervised_reid_survey_2026,
  title   = {Unsupervised Object Re-Identification: Recent Advances, Challenges, and Future Directions},
  author  = {Author One and Author Two and Author Three},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year    = {2026}
}
```

---

## 🤝 Contributing

We warmly welcome contributions! If you find a missing paper, a wrong venue, or a new code release:

1. Fork this repo and add your entry in the matching section using the format below;
2. Open a Pull Request — or simply raise an [Issue](../../issues).

```markdown
| **Method** | Paper Title | ![](https://img.shields.io/badge/CVPR-2026-1f6feb?style=flat-square) | [![](https://img.shields.io/github/stars/owner/repo?style=social)](https://github.com/owner/repo) |
```

<details>
<summary><b>🎨 Regenerating the figures & demo video</b></summary>
<br/>

All figures in [`fig/`](fig) and the demo video are generated from code in [`scripts/`](scripts) (Python · Matplotlib · FFmpeg):

```bash
pip install matplotlib numpy pillow
python scripts/figs1.py fig          # banner, Re-ID process, settings, taxonomy, UDA, USL pipeline
python scripts/figs2.py fig          # scenarios, cross-modal, emerging, VLM, results, timeline, datasets, future
python scripts/video.py fig/_video   # renders 7 scenes → concat into fig/demo.mp4
```

</details>

## ✨ Star History

<div align="center">
<a href="https://star-history.com/#YOUR_ORG/Awesome-Unsupervised-ReID&Date">
  <img src="https://api.star-history.com/svg?repos=YOUR_ORG/Awesome-Unsupervised-ReID&type=Date" width="70%" alt="Star History"/>
</a>

<br/><br/>
<sub>Made with ❤️ by the authors · If this list helps you, a ⭐ means a lot!</sub>
</div>
