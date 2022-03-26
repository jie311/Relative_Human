<h1 align="center"> 
  <img src="assets/RH_logo.png" width="20%" />
</h1>
<h2 align="center"> Relative depth & age in the wild. </h2>

Relative Human (RH) contains the following annotations of **multi-person in-the-wild** RGB images:
 **Depth layers:** relative depth relationship/ordering between all people in the image.
 **Age group classfication:** adults, teenagers, kids, babies.
 Others: **Genders**, **Bounding box**, **2D pose**

<p float="center">
  <img src="assets/RH_demos.png" width="48%" />
  <img src="assets/RH_skeletons.png" width="48%" />
</p>

It is introduced in CVPR 2022 paper [Putting People in their Place: Monocular Regression of 3D People in Depth](https://arxiv.org/abs/2112.08274).

## Download

[Google drive]()
[Baidu drive]()

## Why do we need RH?

<p float="center">
  <img src="assets/RH_table.png" width="48%" />
</p>

Existing 3D datasets are poor in diversity of age and multi-person scenories. In contrast, RH contains richer subjects with explicit age annotations in the wild. We hope that RH can promote relative research, such as monocular depth reasoning, baby / child pose estimation, and so on. 

## How to use it?

We will provide a toolbox for data loading and evaluation. 

Firstly, download the data and set the path in code.

To use it for training, please refer to [BEV](https://github.com/Arthur151/ROMP) for details.

## Re-implementation

To re-implement RH results (in Tab. 1 of BEV paper), please first download the predictions from [here](all_results.zip), then 
```
cd Relative_Human/
# BEV / ROMP / CRMH : set the path of downloaded results (.npz) in RH_evaluation/evaluation.py, then run
python -m RH_evaluation.evaluation

cd RH_evaluation/
# 3DMPPE: set the paths in eval_3DMPPE_RH_results.py and then run
python eval_3DMPPE_RH_results.py
# SMAP: set the paths in eval_SMAP_RH_results.py and then run
python eval_SMAP_RH_results.py
```

## Citation
Please cite our paper if you use RH in your research. 
```bibtex
@InProceedings{sun2022BEV,
author = {Sun, Yu and Liu, Wu and Bao, Qian and Fu, Yili and Mei, Tao and Black, Michael J},
title = {Putting People in their Place: Monocular Regression of 3D People in Depth},
booktitle = {CVPR},
year = {2022}
}
```