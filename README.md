# ReLeaPS : Reinforcement Learning-based Illumination Planning for Generalized Photometric Stereo
[\[GitHub\]](https://github.com/jhchan0805/ReLeaPS)
[\[Homepage\]](https://jhchan0805.github.io/ReLeaPS)
[\[Video\]](https://youtu.be/5D4NBlf-L3w)

### Prerequisites
  * The code is tested on Linux with Python 3.10.
  * Install requirements from `requirements.txt` before running.

### Setup
This repo contains sub-module. Clone this repo:
```
git clone --recurse-submodules https://github.com/jhchan0805/ReLeaPS
```
  
  * To train and evaluate on `CNN-PS` backbone, download the pre-trained model `weight_and_model.hdf5` to `data` according to [CNN-PS][1].
  * To train and evaluate on `PS-FCN` backbone, download the pre-trained model `PS-FCN_B_S_32_normalize.pth.tar` to `src/PS-FCN/data/models` according to [PS-FCN][2].
  * To evaluate on `DiLiGenT` dataset, download `DiLiGenT.zip` to `data` according to [DiLiGenT][3].
  
[1]: https://github.com/satoshi-ikehata/CNN-PS-ECCV2018
[2]: https://github.com/guanyingc/PS-FCN
[3]: https://sites.google.com/site/photometricstereodata/single

### Training
  * Download the synthetic dataset (blobs & sculpture) for training from: [datasets](https://drive.google.com/file/d/1hZtjtY8DMOk-sITT_AoZzBs5oZzVdgkk/view?usp=drive_link) and place under `data`.
    ![image](https://github.com/user-attachments/assets/350d1fa9-fbe0-48a5-b962-8a47cd71a840)

  * Run `run_train.sh`.
    * `make train`
      * 这个 代码可以让你 使用 Makefile 里面定义好的 `make train` 指令, 这个的作用和 `run_train.sh` 是一样的
    * `make benchmark`
      * 这个 代码可以让你 使用 Makefile 里面定义好的 `make benchmark` 指令

     ![image](https://github.com/user-attachments/assets/3512aca9-46b0-44d3-9370-d61bfc4202a4)

### Evaluation
  * Train the models yourself or download the pre-trained models from: [TBD]() and place under `data/models`.
  * Run `run_benchmark.sh`.

## Citation
If you find our work useful for your research, please consider citing:
```BibTeX
@InProceedings{jh2023releaps,
    author = {Chan, Junhoong and Yu, Bohan and Guo, Heng and Ren, Jieji and Lu, Zongqing and Shi, Boxin},
    title = {{ReLeaPS}: Reinforcement Learning-based Illumination Planning for Generalized Photometric Stereo},
    booktitle = {Proceedings of the International Conference on Computer Vision (ICCV)},
    month = {October},
    year = {2023},
}
```

Copyright (c) 2022-2023 Bohan Yu. All rights reserved. \
ReLeaPS is free software licensed under GNU Affero General Public License version 3 or latter.

