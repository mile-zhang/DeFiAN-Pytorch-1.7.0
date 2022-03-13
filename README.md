# DeFiAN-PyTorch-1.7.0 (change from <a href="https://github.com/YuanfeiHuang/DeFiAN">YuanfeiHuang/DeFiAN</a> )
This repository is for DeFiAN introduced in the following paper

Yuanfei Huang, Jie Li, Xinbo Gao*, Yanting Hu and Wen Lu, "Interpretable Detail-Fidelity Attention Network for Single Image Super-Resolution", IEEE Transactions on Image Processing (TIP), vol.30, pp.2325-2339, 2021.

[TIP](https://ieeexplore.ieee.org/document/9334407)

[arXiv](https://arxiv.org/abs/2009.13134)

## Contents
1. [Architecture](#architecture)
2. [Requirement](#requirement)
3. [Train](#train)
4. [Test](#test)
5. [Results](#results)
6. [Citation](#citation)

## Architecture

![Framework of DeFiAN](/Figs/Framework_DeFiAN.png)

## Requirement:

1. Python==3.8.6

2. PyTorch==1.7.02

3. torchvision==0.8.0

4. numpy==1.19.4

5. scikit-image==0.18.1

6. imageio==2.9.0

7. matplotlib==3.3.3

8. tqdm==4.54.1

## Train
🎯Add <a href="https://github.com/YuanfeiHuang/TLSR/tree/main/data">common.py</a>
1. Replace the train dataset path '/mnt/Datasets/Train/' and validation dataset 'mnt/Datasets/Test/' with your training and validation datasets, respectively.

3. Set the configuration '--train' in 'option.py' as 'True', and other configurations as you want.

4. If you want to use GPU, Set the configuration '--cuda' in 'option.py' as 'True'

5. run 'main.py'.
## Test
🎯Add <a href="https://github.com/YuanfeiHuang/TLSR/tree/main/data">common.py</a>
1. Download models from [OneDrive](https://1drv.ms/u/s!ArdHek-3P6D-avrb8QJPrzqeU2c?e=Md84Tw), [Google Drive](https://drive.google.com/drive/folders/1C38IUUQCPlXcpmW_gki_IpWHGYMo7KL4?usp=sharing) or [BaiduYun](https://pan.baidu.com/s/10fLcejD2N5nTnk-TUj9a_A)(password: 3vj9).

2. Replace the test dataset path '/mnt/Datasets/Test/' with your datasets.

3. Set the configuration '--train' in 'option.py' as 'False'

4. If you want to use GPU, Set the configuration '--cuda' in 'option.py' as 'True'

5. run 'main.py'.

### Example
```python
# DeFiAN_s x2 
python main.py --cuda --dir_data /home/mile/dataset/

# DeFiAN_L x2 
python main.py 

# DeFiAN_s x3 
python main.py 

# DeFiAN_L x3 
python main.py 

# DeFiAN_s x4  
python main.py 

# DeFiAN_L x4
python main.py  
```

## Results
### Quantitative Results (PSNR/SSIM)
![Quantitative Results](/Figs/Quantitative_Results.png)

### Qualitative Results
![Fig.6](/Figs/Fig_6.png)
![Fig.7](/Figs/Fig_7.png)
![Fig.8](/Figs/Fig_8.png)
![Fig.9](/Figs/Fig_9.png) 

## Citation
```
@article{huang2021interpretable,
  title={Interpretable Detail-Fidelity Attention Network for Single Image Super-Resolution},
  author={Huang, Yuanfei and Li, Jie and Gao, Xinbo and Hu, Yanting and Lu, Wen},
  journal={IEEE Transactions on Image Processing},
  volume={30},
  pages={2325--2339},
  year={2021},
  publisher={IEEE}
}
```
