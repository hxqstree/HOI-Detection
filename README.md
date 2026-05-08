# Awesome Human-Object Interaction Detection

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Papers](https://img.shields.io/badge/Papers-HOI%20Detection-blue)](#papers)
[![Last Updated](https://img.shields.io/badge/Last%20Updated-2026--05-lightgrey)](#)

A curated collection of papers, codes, datasets, and resources for **Human-Object Interaction (HOI) Detection**.

HOI detection aims to localize humans and objects and recognize their interactions, usually represented as `<human, verb, object>` triplets.

> Scope: this repository focuses on image/video HOI detection, zero-shot/open-vocabulary HOI detection, and diffusion-based HOI detection. 3D HOI generation, human-object motion generation, animation generation, reconstruction-only papers, and contact-only papers are not included unless they directly target HOI detection.
>
> Note: the one-stage / two-stage split is a practical reading-oriented grouping. Some transformer or open-vocabulary methods may combine ideas from both families.

## Contents

- [Datasets](#datasets)
- [Papers](#papers)
  - [Vision-based HOI Detection](#vision-based-hoi-detection)
    - [One-stage / End-to-End](#one-stage--end-to-end)
    - [Two-stage / Proposal-based](#two-stage--proposal-based)
  - [Vision-Language Model based HOI Detection](#vision-language-model-based-hoi-detection)
    - [One-stage / End-to-End](#one-stage--end-to-end-1)
    - [Two-stage / Proposal-based](#two-stage--proposal-based-1)
  - [Diffusion Model based HOI Detection](#diffusion-model-based-hoi-detection)
- [Useful Resources](#useful-resources)
- [Contributing](#contributing)

## Datasets

| Dataset | Year | Task | Scale | Links |
|:---:|:---:|---|---|:---:|
| V-COCO | 2015 | Image HOI detection / visual semantic role labeling | 10,346 images | [[Dataset](https://paperswithcode.com/dataset/v-coco)] |
| HICO-DET | 2018 | Image HOI detection | 47,776 images, 600 HOI classes | [[Dataset](https://paperswithcode.com/dataset/hico-det)] |
| HCVRD | 2018 | Human-centric visual relationship detection | 52,855 images | [[Paper](https://arxiv.org/abs/1712.07160)] |
| HOI-A | 2019 | Image HOI detection | 38K+ images | [[Dataset](https://paperswithcode.com/dataset/hoi-a)] |
| SWiG-HOI | 2022 | Large-vocabulary HOI detection | Large-vocabulary interactions | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Wang_Learning_Transferable_Human-Object_Interaction_Detector_With_Natural_Language_Supervision_CVPR_2022_paper.html)] |
| VG-HOI | 2024 | Open-set HOI detection | 17K+ HOI relationships | [[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/28422)] |
| Magic-HOI / SynHOI | 2024 | Open-world HOI detection | Real and synthetic HOI data | [[Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Yang_Open-World_Human-Object_Interaction_Detection_via_Multi-modal_Prompts_CVPR_2024_paper.html)] |

## Papers

### Vision-based HOI Detection

Methods mainly based on visual features, object detection, pose, spatial relations, graph reasoning, or vision transformers.

#### One-stage / End-to-End

| Year | Venue | Method | Paper | Links |
|:---:|:---:|:---:|---|:---:|
| 2020 | CVPR | IP-Net | Learning Human-Object Interaction Detection Using Interaction Points | [[Paper](https://openaccess.thecvf.com/content_CVPR_2020/html/Wang_Learning_Human-Object_Interaction_Detection_Using_Interaction_Points_CVPR_2020_paper.html)] [[Code](https://github.com/vaesl/IP-Net)] |
| 2020 | CVPR | PPDM | Parallel Point Detection and Matching for Real-Time Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content_CVPR_2020/html/Liao_PPDM_Parallel_Point_Detection_and_Matching_for_Real-Time_Human-Object_Interaction_CVPR_2020_paper.html)] |
| 2020 | ECCV | UnionDet | Union-Level Detector Towards Real-Time Human-Object Interaction Detection | [[Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123600494.pdf)] |
| 2021 | CVPR | AS-Net | Reformulating HOI Detection as Adaptive Set Prediction | [[Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Chen_Reformulating_HOI_Detection_As_Adaptive_Set_Prediction_CVPR_2021_paper.html)] [[Code](https://github.com/yoyomimi/AS-Net)] |
| 2021 | CVPR | GGNet | Glance and Gaze: Inferring Action-Aware Points for One-Stage Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Zhong_Glance_and_Gaze_Inferring_Action-Aware_Points_for_One-Stage_Human-Object_Interaction_CVPR_2021_paper.html)] [[Code](https://github.com/SherlockHolmes221/GGNet)] |
| 2021 | CVPR | HOTR | End-to-End Human-Object Interaction Detection With Transformers | [[Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Kim_HOTR_End-to-End_Human-Object_Interaction_Detection_With_Transformers_CVPR_2021_paper.html)] [[Code](https://github.com/kakaobrain/HOTR)] |
| 2021 | CVPR | HOI Transformer | End-to-End Human Object Interaction Detection With HOI Transformer | [[Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Zou_End-to-End_Human_Object_Interaction_Detection_With_HOI_Transformer_CVPR_2021_paper.html)] [[Code](https://github.com/bbepoch/HoiTransformer)] |
| 2021 | CVPR | QPIC | Query-Based Pairwise Human-Object Interaction Detection With Image-Wide Contextual Information | [[Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Tamura_QPIC_Query-Based_Pairwise_Human-Object_Interaction_Detection_With_Image-Wide_Contextual_Information_CVPR_2021_paper.html)] [[Code](https://github.com/hitachi-rd-cv/qpic)] |
| 2021 | NeurIPS | CDN | Mining the Benefits of Two-stage and One-stage HOI Detection | [[Paper](https://papers.nips.cc/paper/2021/hash/8f1d43620bc6bb580df6e80b0dc05c48-Abstract.html)] [[Code](https://github.com/YueLiao/CDN)] |
| 2022 | CVPR | CATN | Category-Aware Transformer Network for Better Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Dong_Category-Aware_Transformer_Network_for_Better_Human-Object_Interaction_Detection_CVPR_2022_paper.html)] |
| 2022 | CVPR | DOQ | Distillation Using Oracle Queries for Transformer-Based Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Qu_Distillation_Using_Oracle_Queries_for_Transformer-Based_Human-Object_Interaction_Detection_CVPR_2022_paper.html)] |
| 2022 | CVPR | DisTR | Human-Object Interaction Detection via Disentangled Transformer | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Zhou_Human-Object_Interaction_Detection_via_Disentangled_Transformer_CVPR_2022_paper.html)] |
| 2022 | CVPR | MSTR | Multi-Scale Transformer for End-to-End Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Kim_MSTR_Multi-Scale_Transformer_for_End-to-End_Human-Object_Interaction_Detection_CVPR_2022_paper.html)] |
| 2022 | CVPR | SSRT | What To Look at and Where: Semantic and Spatial Refined Transformer for Detecting Human-Object Interactions | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Iftekhar_What_To_Look_at_and_Where_Semantic_and_Spatial_Refined_CVPR_2022_paper.html)] |
| 2022 | CVPR | STIP | Exploring Structure-Aware Transformer Over Interaction Proposals for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Zhang_Exploring_Structure-Aware_Transformer_Over_Interaction_Proposals_for_Human-Object_Interaction_Detection_CVPR_2022_paper.html)] [[Code](https://github.com/zyong812/STIP)] |
| 2023 | CVPR | CQL | Category Query Learning for Human-Object Interaction Classification | [[Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Xie_Category_Query_Learning_for_Human-Object_Interaction_Classification_CVPR_2023_paper.html)] |
| 2023 | CVPR | MUREN | Relational Context Learning for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Kim_Relational_Context_Learning_for_Human-Object_Interaction_Detection_CVPR_2023_paper.html)] |
| 2023 | ICCV | AGER | Agglomerative Transformer for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Tu_Agglomerative_Transformer_for_Human-Object_Interaction_Detection_ICCV_2023_paper.html)] |
| 2024 | AAAI | SCTC | Exploring Self- and Cross-Triplet Correlations for Human-Object Interaction Detection | [[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/28031)] |
| 2024 | CVPR | DP-HOI | Disentangled Pre-training for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Li_Disentangled_Pre-training_for_Human-Object_Interaction_Detection_CVPR_2024_paper.html)] [[Code](https://github.com/xingaoli/DP-HOI)] |
| 2025 | AAAI | ContextHOI | Spatial Context Learning for Human-Object Interaction Detection | [[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/32411)] |
| 2025 | AAAI | InterProDa | Orchestrating the Symphony of Prompt Distribution Learning for Human-Object Interaction Detection | [[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/32412)] |
| 2025 | CVPR | HORP | Human-Object Relation Priors Guided HOI Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Geng_HORP_Human-Object_Relation_Priors_Guided_HOI_Detection_CVPR_2025_paper.html)] [[Code](https://github.com/namegp/HORP)] |
| 2025 | ICCV | TSR | No More Sibling Rivalry: Debiasing Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Yang_No_More_Sibling_Rivalry_Debiasing_Human-Object_Interaction_Detection_ICCV_2025_paper.html)] |

#### Two-stage / Proposal-based

| Year | Venue | Method | Paper | Links |
|:---:|:---:|:---:|---|:---:|
| 2018 | CVPR | InteractNet | Detecting and Recognizing Human-Object Interactions | [[Paper](https://openaccess.thecvf.com/content_cvpr_2018/html/Gkioxari_Detecting_and_Recognizing_CVPR_2018_paper.html)] |
| 2018 | ECCV | GPNN | Learning Human-Object Interactions by Graph Parsing Neural Networks | [[Paper](https://openaccess.thecvf.com/content_ECCV_2018/html/Siyuan_Qi_Learning_Human-Object_Interactions_ECCV_2018_paper.html)] |
| 2019 | CVPR | Knowledge | Learning to Detect Human-Object Interactions With Knowledge | [[Paper](https://openaccess.thecvf.com/content_CVPR_2019/html/Xu_Learning_to_Detect_Human-Object_Interactions_With_Knowledge_CVPR_2019_paper.html)] |
| 2019 | CVPR | TIN | Transferable Interactiveness Knowledge for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content_CVPR_2019/html/Li_Transferable_Interactiveness_Knowledge_for_Human-Object_Interaction_Detection_CVPR_2019_paper.html)] [[Code](https://github.com/DirtyHarryLYL/Transferable-Interactiveness-Network)] |
| 2019 | ICCV | DCA | Deep Contextual Attention for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Wang_Deep_Contextual_Attention_for_Human-Object_Interaction_Detection_ICCV_2019_paper.html)] |
| 2019 | ICCV | No-Frills | No-Frills Human-Object Interaction Detection: Factorization, Layout Encodings, and Training Techniques | [[Paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Gupta_No-Frills_Human-Object_Interaction_Detection_Factorization_Layout_Encodings_and_Training_Techniques_ICCV_2019_paper.html)] |
| 2019 | ICCV | PMFNet | Pose-Aware Multi-Level Feature Network for Human Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Wan_Pose-Aware_Multi-Level_Feature_Network_for_Human_Object_Interaction_Detection_ICCV_2019_paper.html)] |
| 2019 | ICCV | RPNN | Relation Parsing Neural Network for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Zhou_Relation_Parsing_Neural_Network_for_Human-Object_Interaction_Detection_ICCV_2019_paper.html)] |
| 2020 | AAAI | FG | Detecting Human-Object Interactions via Functional Generalization | [[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/6616)] |
| 2020 | CVPR | VSGNet | Spatial Attention Network for Detecting Human Object Interactions Using Graph Convolutions | [[Paper](https://openaccess.thecvf.com/content_CVPR_2020/html/Ulutan_VSGNet_Spatial_Attention_Network_for_Detecting_Human_Object_Interactions_Using_CVPR_2020_paper.html)] |
| 2020 | ECCV | ACP | Detecting Human-Object Interactions with Action Co-occurrence Priors | [[Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/html/3850_ECCV_2020_paper.php)] [[Code](https://github.com/Dong-JinKim/ActionCooccurrencePriors)] |
| 2020 | ECCV | CHGNet | Contextual Heterogeneous Graph Network for Human-Object Interaction Detection | [[Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/html/2718_ECCV_2020_paper.php)] |
| 2020 | ECCV | DRG | Dual Relation Graph for Human-Object Interaction Detection | [[Paper](https://sanghani.cs.vt.edu/research/publications/2020/drg-dual-relation-graph-for-human-object-interaction-detection.html)] [[Code](https://github.com/vt-vl-lab/DRG)] |
| 2020 | ECCV | PD-Net | Polysemy Deciphering Network for Human-Object Interaction Detection | [[Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/html/3382_ECCV_2020_paper.php)] [[Code](https://github.com/MuchHair/PD-Net)] |
| 2020 | ECCV | VCL | Visual Compositional Learning for Human-Object Interaction Detection | [[Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123600579.pdf)] [[Code](https://github.com/zhihou7/HOI-CL)] |
| 2021 | CVPR | ATL | Affordance Transfer Learning for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Hou_Affordance_Transfer_Learning_for_Human-Object_Interaction_Detection_CVPR_2021_paper.html)] [[Code](https://github.com/zhihou7/HOI-CL)] |
| 2021 | CVPR | FCL | Detecting Human-Object Interaction via Fabricated Compositional Learning | [[Paper](https://openaccess.thecvf.com/content/CVPR2021/html/Hou_Detecting_Human-Object_Interaction_via_Fabricated_Compositional_Learning_CVPR_2021_paper.html)] |
| 2021 | ICCV | SG2HOI | Exploiting Scene Graphs for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/ICCV2021/html/He_Exploiting_Scene_Graphs_for_Human-Object_Interaction_Detection_ICCV_2021_paper.html)] |
| 2022 | CVPR | Interactiveness Field | Interactiveness Field in Human-Object Interactions | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Liu_Interactiveness_Field_in_Human-Object_Interactions_CVPR_2022_paper.html)] |
| 2022 | CVPR | UPT | Efficient Two-Stage Detection of Human-Object Interactions With a Novel Unary-Pairwise Transformer | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Zhang_Efficient_Two-Stage_Detection_of_Human-Object_Interactions_With_a_Novel_Unary-Pairwise_CVPR_2022_paper.html)] |
| 2023 | CVPR | ViPLO | Vision Transformer Based Pose-Conditioned Self-Loop Graph for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Park_ViPLO_Vision_Transformer_Based_Pose-Conditioned_Self-Loop_Graph_for_Human-Object_Interaction_CVPR_2023_paper.html)] |
| 2023 | ICCV | PViC | Exploring Predicate Visual Context in Detecting of Human-Object Interactions | [[Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Zhang_Exploring_Predicate_Visual_Context_in_Detecting_of_Human-Object_Interactions_ICCV_2023_paper.html)] |
| 2024 | CVPR | Hybrid Learning | Exploring Pose-Aware Human-Object Interaction via Hybrid Learning | [[Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Wu_Exploring_Pose-Aware_Human-Object_Interaction_via_Hybrid_Learning_CVPR_2024_paper.html)] |

### Vision-Language Model based HOI Detection

Methods that use CLIP, VLMs, LLMs, language supervision, prompt learning, open-vocabulary learning, or vision-language pre-training for HOI detection.

#### One-stage / End-to-End

| Year | Venue | Method | Paper | Links |
|:---:|:---:|:---:|---|:---:|
| 2022 | CVPR | - | Learning Transferable Human-Object Interaction Detector With Natural Language Supervision | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Wang_Learning_Transferable_Human-Object_Interaction_Detector_With_Natural_Language_Supervision_CVPR_2022_paper.html)] |
| 2022 | CVPR | GEN-VLKT | Simplify Association and Enhance Interaction Understanding for HOI Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2022/html/Liao_GEN-VLKT_Simplify_Association_and_Enhance_Interaction_Understanding_for_HOI_Detection_CVPR_2022_paper.html)] [[Code](https://github.com/YueLiao/gen-vlkt)] |
| 2023 | CVPR | OpenCat | Open-Category Human-Object Interaction Pre-Training via Language Modeling Framework | [[Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Zheng_Open-Category_Human-Object_Interaction_Pre-Training_via_Language_Modeling_Framework_CVPR_2023_paper.html)] |
| 2023 | ICCV | RLIPv2 | Re-mine, Learn and Reason: Exploring the Cross-modal Semantic Correlations for Language-guided HOI Detection | [[Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Cao_Re-mine_Learn_and_Reason_Exploring_the_Cross-modal_Semantic_Correlations_for_ICCV_2023_paper.html)] |
| 2024 | CVPR | CMD-SE | Exploring the Potential of Large Foundation Models for Open-Vocabulary HOI Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Lei_Exploring_the_Potential_of_Large_Foundation_Models_for_Open-Vocabulary_HOI_CVPR_2024_paper.html)] |
| 2024 | CVPR | MP-HOI | Open-World Human-Object Interaction Detection via Multi-modal Prompts | [[Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Yang_Open-World_Human-Object_Interaction_Detection_via_Multi-modal_Prompts_CVPR_2024_paper.html)] [[Project](https://MP-HOI.github.io/)] |
| 2025 | CVPR | SGC-Net | Stratified Granular Comparison Network for Open-Vocabulary HOI Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Lin_SGC-Net_Stratified_Granular_Comparison_Network_for_Open-Vocabulary_HOI_Detection_CVPR_2025_paper.html)] [[Code](https://github.com/Phil0212/SGC-Net)] |
| 2025 | ICCV | BC-HOI | Bilateral Collaboration with Large Vision-Language Models for Open Vocabulary Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Hu_Bilateral_Collaboration_with_Large_Vision-Language_Models_for_Open_Vocabulary_Human-Object_ICCV_2025_paper.html)] |
| 2025 | ICCV | INP-CC | Open-Vocabulary HOI Detection with Interaction-aware Prompt and Concept Calibration | [[Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Lei_Open-Vocabulary_HOI_Detection_with_Interaction-aware_Prompt_and_Concept_Calibration_ICCV_2025_paper.html)] [[Code](https://github.com/ltttpku/INP-CC)] |

#### Two-stage / Proposal-based

| Year | Venue | Method | Paper | Links |
|:---:|:---:|:---:|---|:---:|
| 2023 | CVPR | HOICLIP | Efficient Knowledge Transfer for HOI Detection With Vision-Language Models | [[Paper](https://openaccess.thecvf.com/content/CVPR2023/html/Ning_HOICLIP_Efficient_Knowledge_Transfer_for_HOI_Detection_With_Vision-Language_Models_CVPR_2023_paper.html)] |
| 2023 | ICCV | ADA-CM | Efficient Adaptive Human-Object Interaction Detection with Concept-guided Memory | [[Paper](https://openaccess.thecvf.com/content/ICCV2023/html/Lei_Efficient_Adaptive_Human-Object_Interaction_Detection_with_Concept-guided_Memory_ICCV_2023_paper.html)] [[Code](https://github.com/ltttpku/ADA-CM)] |
| 2023 | NeurIPS | CLIP4HOI | Towards Adapting CLIP for Practical Zero-Shot HOI Detection | [[Paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8fd5bc08e744fe0dfe798c61d1575a22-Abstract-Conference.html)] |
| 2023 | NeurIPS | UniHOI | Detecting Any Human-Object Interaction Relationship: Universal HOI Detector with Spatial Prompt Learning on Foundation Models | [[Paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/02687e7b22abc64e651be8da74ec610e-Abstract-Conference.html)] |
| 2024 | AAAI | DHD | Toward Open-Set Human Object Interaction Detection | [[Paper](https://ojs.aaai.org/index.php/AAAI/article/view/28422)] [[Code](https://github.com/mrwu-mac/DHD)] |
| 2024 | CVPR | BA-HOI | Bilateral Adaptation for Human-Object Interaction Detection with Occlusion-Robustness | [[Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Wang_Bilateral_Adaptation_for_Human-Object_Interaction_Detection_with_Occlusion-Robustness_CVPR_2024_paper.html)] |
| 2024 | CVPR | SICHOI | Discovering Syntactic Interaction Clues for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2024/html/Luo_Discovering_Syntactic_Interaction_Clues_for_Human-Object_Interaction_Detection_CVPR_2024_paper.html)] |
| 2025 | CVPR | LAIN | Locality-Aware Zero-Shot Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Kim_Locality-Aware_Zero-Shot_Human-Object_Interaction_Detection_CVPR_2025_paper.html)] |

### Diffusion Model based HOI Detection

Diffusion-based methods that directly target HOI detection. 3D HOI generation, animation generation, text-to-image interaction control, and reconstruction-only diffusion papers are intentionally excluded from this section.

| Year | Venue | Method | Paper | Links |
|:---:|:---:|:---:|---|:---:|
| 2025 | CVPR | HOI-IDiff | An Image-like Diffusion Method for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Hui_An_Image-like_Diffusion_Method_for_Human-Object_Interaction_Detection_CVPR_2025_paper.html)] |
| 2025 | ICCV | VRDiff | Visual Relation Diffusion for Human-Object Interaction Detection | [[Paper](https://openaccess.thecvf.com/content/ICCV2025/html/Cao_Visual_Relation_Diffusion_for_Human-Object_Interaction_Detection_ICCV_2025_paper.html)] |

## Useful Resources

| Name | Description | Links |
|---|---|:---:|
| Papers with Code: HICO-DET | Benchmarks and papers on HICO-DET | [[Link](https://paperswithcode.com/dataset/hico-det)] |
| HOI-CL | Compositional learning series for HOI detection | [[Project](https://zhihou7.github.io/HOI-CL/)] [[Code](https://github.com/zhihou7/HOI-CL)] |

## Contributing

Contributions are welcome. Please open an issue or pull request if you find missing papers, incorrect metadata, or broken links.

Recommended item format:

```markdown
| Year | Venue | Method | Paper | Links |
|:---:|:---:|:---:|---|:---:|
| 2026 | CVPR | METHOD | Paper Title | [[Paper](paper-url)] [[Code](code-url)] |
```
