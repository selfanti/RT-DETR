English | [简体中文](README_cn.md)


<h2 align="center">RT-DETR: DETRs Beat YOLOs on Real-time Object Detection</h2>
<p align="center">
    <!-- <a href="https://github.com/lyuwenyu/RT-DETR/blob/main/LICENSE">
        <img alt="license" src="https://img.shields.io/badge/LICENSE-Apache%202.0-blue">
    </a> -->
    <a href="https://github.com/lyuwenyu/RT-DETR/blob/main/LICENSE">
        <img alt="license" src="https://img.shields.io/github/license/lyuwenyu/RT-DETR">
    </a>
    <a href="https://github.com/lyuwenyu/RT-DETR/pulls">
        <img alt="prs" src="https://img.shields.io/github/issues-pr/lyuwenyu/RT-DETR">
    </a>
    <a href="https://github.com/lyuwenyu/RT-DETR/issues">
        <img alt="issues" src="https://img.shields.io/github/issues/lyuwenyu/RT-DETR?color=pink">
    </a>
    <a href="https://github.com/lyuwenyu/RT-DETR">
        <img alt="issues" src="https://img.shields.io/github/stars/lyuwenyu/RT-DETR">
    </a>
    <a href="https://arxiv.org/abs/2304.08069">
        <img alt="arXiv" src="https://img.shields.io/badge/arXiv-2304.08069-red">
    </a>
    <a href="mailto: lyuwenyu@foxmail.com">
        <img alt="emal" src="https://img.shields.io/badge/contact_me-email-yellow">
    </a>
</p>

---


This is the official implementation of papers 
- [DETRs Beat YOLOs on Real-time Object Detection](https://arxiv.org/abs/2304.08069)
- [RT-DETRv2: Improved Baseline with Bag-of-Freebies for Real-Time Detection Transformer](https://arxiv.org/abs/2407.17140)


<details>
<summary>Fig</summary>

<table><tr>
<td><img src=https://github.com/lyuwenyu/RT-DETR/assets/77494834/0ede1dc1-a854-43b6-9986-cf9090f11a61 border=0 width=500></td>
<td><img src=https://github.com/user-attachments/assets/437877e9-1d4f-4d30-85e8-aafacfa0ec56 border=0 width=500></td>
</tr></table>
</details>



## 📍 Implementations
- 🔥 RT-DETRv2
  - paddle: [code&weight](./rtdetrv2_paddle/)
  - pytorch: [code&weight](./rtdetrv2_pytorch/)
- 🔥 RT-DETR 
  - paddle: [code&weight](./rtdetr_paddle)
  - pytorch: [code&weight](./rtdetr_pytorch)


| Model | Input shape | Dataset | $AP^{val}$ | $AP^{val}_{50}$| Params(M) | FLOPs(G) | T4 TensorRT FP16(FPS)
|:---:|:---:| :---:|:---:|:---:|:---:|:---:|:---:|
| RT-DETR-R18 | 640 | COCO | 46.5 | 63.8 | 20 | 60 | 217 |
| RT-DETR-R34 | 640 | COCO | 48.9 | 66.8 | 31 | 92 | 161 |
| RT-DETR-R50-m | 640 | COCO | 51.3 | 69.6 | 36 | 100 | 145 |
| RT-DETR-R50 |  640 | COCO | 53.1 | 71.3 | 42 | 136 | 108 |
| RT-DETR-R101 | 640 | COCO | 54.3 | 72.7 | 76 | 259 | 74 |
| RT-DETR-HGNetv2-L | 640 | COCO | 53.0 | 71.6 | 32 | 110 | 114 |
| RT-DETR-HGNetv2-X | 640 | COCO | 54.8 | 73.1 | 67 | 234 | 74 |
| RT-DETR-R18 | 640 | COCO + Objects365 | **49.2** | **66.6** | 20 | 60 | **217** |
| RT-DETR-R50 | 640 | COCO + Objects365 | **55.3** | **73.4** | 42 | 136 | **108** |
| RT-DETR-R101 | 640 | COCO + Objects365 | **56.2** | **74.6** | 76 | 259 | **74** |
**RT-DETRv2-S** | 640 | COCO  | **48.1** <font color=green>(+1.6)</font> | **65.1** | 20 | 60 | 217 |
**RT-DETRv2-M**<sup>*<sup> | 640 | COCO  | **49.9** <font color=green>(+1.0)</font> | **67.5** | 31 | 92 | 161 |
**RT-DETRv2-M** | 640 | COCO | **51.9** <font color=green>(+0.6)</font> | **69.9** | 36 | 100 | 145 |
**RT-DETRv2-L** | 640 | COCO | **53.4** <font color=green>(+0.3)</font> | **71.6** | 42 | 136 | 108 |
**RT-DETRv2-X** | 640 | COCO | 54.3 | **72.8** <font color=green>(+0.1)</font>  | 76 | 259| 74 |

**Notes:**
- `COCO + Objects365` in the table means finetuned model on COCO using pretrained weights trained on Objects365.


## Citation
If you use `RT-DETR` or `RTDETRv2` in your work, please use the following BibTeX entries:
```
@misc{lv2023detrs,
      title={DETRs Beat YOLOs on Real-time Object Detection},
      author={Yian Zhao and Wenyu Lv and Shangliang Xu and Jinman Wei and Guanzhong Wang and Qingqing Dang and Yi Liu and Jie Chen},
      year={2023},
      eprint={2304.08069},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}

@misc{lv2024rtdetrv2improvedbaselinebagoffreebies,
      title={RT-DETRv2: Improved Baseline with Bag-of-Freebies for Real-Time Detection Transformer}, 
      author={Wenyu Lv and Yian Zhao and Qinyao Chang and Kui Huang and Guanzhong Wang and Yi Liu},
      year={2024},
      eprint={2407.17140},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2407.17140}, 
}
```
