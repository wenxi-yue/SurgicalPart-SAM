<h1 align="center"> SurgicalPart-SAM: Part-to-Whole Collaborative Prompting for Surgical Instrument Segmentation </h1>
<p align="center">
<a href="https://arxiv.org/pdf/2312.14481.pdf"><img src="https://img.shields.io/badge/arXiv-Paper-<color>"></a>
</p>
<h5 align="center"><em>Wenxi Yue, Jing Zhang, Kun Hu, Qiuxia Wu, Zongyuan Ge, Yong Xia, Jiebo Luo, Zhiyong Wang</em></h5>
</p>
<p align="center">
  <a href="#news">News</a> |
  <a href="#abstract">Abstract</a> |
  <a href="#results">Results</a> |
  <a href="#installation">Installation</a> |
  <a href="#data">Data</a> |
  <a href="#checkpoints">Checkpoints</a> |
  <a href="#train">Train</a> |
  <a href="#inference">Inference</a>
</p>


## News 

**2023.12.22** - The tech report is posted on arxiv. Work in progress.


## Abstract 
The Segment Anything Model (SAM) exhibits promise in generic object segmentation and offers potential for various applications. Existing methods have applied SAM to surgical instrument segmentation (SIS) by tuning SAM-based frameworks with surgical data. However, they fall short in two crucial aspects: (1) Straightforward model tuning with instrument masks treats each instrument as a single entity, neglecting their complex structures and fine-grained details; and (2) Instrument category-based prompts are not flexible and informative enough to describe instrument structures. To address these problems, in this paper, we investigate text promptable SIS and propose SurgicalPart-SAM (SP-SAM), a novel SAM efficient-tuning approach that explicitly integrates instrument structure knowledge with SAM's generic knowledge, guided by expert knowledge on instrument part compositions. Specifically, we achieve this by proposing (1) Collaborative Prompts that describe instrument structures via collaborating category-level and part-level texts; (2) Cross-Modal Prompt Encoder that encodes text prompts jointly with visual embeddings into discriminative part-level representations; and (3) Part-to-Whole Adaptive Fusion and Hierarchical Decoding that adaptively fuse the part-level representations into a whole for accurate instrument segmentation in surgical scenarios. Built upon them, SP-SAM acquires a better capability to comprehend surgical instruments in terms of both overall structure and part-level details. Extensive experiments on both the EndoVis2018 and EndoVis2017 datasets demonstrate SP-SAM's state-of-the-art performance with minimal tunable parameters. 


![](assets/method.png)
<figcaption align = "center"><b>Figure 1: Overview of SurgicalPart-SAM. 
 </b></figcaption>


 ## Results

<p align="center">
  <img src="assets/results_endovis18.png" alt="Image Description" width="900" height="YOUR_HEIGHT">
</p>

<p align="center">
  <img src="assets/results_endovis17.png" alt="Image Description" width="910" height="YOUR_HEIGHT">
</p>
<figcaption align = "center"><b>Figure 2: Visualisation Results of SurgicalPart-SAM.
 </b></figcaption>


 ##  Citing SurgicalPart-SAM

If you find SurgicalPart-SAM helpful, please consider citing:
```
@misc{yue2024surgicalpartsam,
      title={SurgicalPart-SAM: Part-to-Whole Collaborative Prompting for Surgical Instrument Segmentation}, 
      author={Wenxi Yue and Jing Zhang and Kun Hu and Qiuxia Wu and Zongyuan Ge and Yong Xia and Jiebo Luo and Zhiyong Wang},
      year={2024},
      eprint={2312.14481},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
