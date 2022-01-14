# NYCU_VRDL_HW4
 swin-ir

homework4 from NCTU VRDL class 2021 fall
By Ya-Shu Yang


## Dependencies:
+ Python 3.7.3
+ PyTorch 1.9.0
+ torchvision 0.10.0
+ timm 0.4.12

## Usage
### 1. Download pre-trained models from google drive

https://drive.google.com/file/d/10Eg8Nncyxjb01SsN5JeEQ4KfI9WeRVZH/view?usp=sharing


### 2. Prepare data


Please download the training images and testing images from CodaLab competition:
https://drive.google.com/file/d/1GL_Rh1N-WjrvF_-YOKOyvq0zrV6TF4hb/view
Put the training images to KAIR-master/trainsets/trainH,KAIR-master/trainsets/trainL, 
and put the testing images to KAIR-master/testsets/testH,KAIR-master/testsets/testL



### 3. Install required packages

detail in KAIR and SwinIR folder

### 4. Train

in "KAIR-master/", we use the option file name in 
+[KAIR-master/options/swinir/train_swinir_sr_hw4](https://github.com/pc0062296/NYCU_VRDL_HW4/blob/main/KAIR-master/options/swinir/train_swinir_sr_hw4.json)

### 5. Reproduce

To Reproduce the result:

Please download the pre-trained model 

and put it SwinIR-main/model_zoo

```bash
python main_test_swinir.py --task classical_sr --scale 3 --training_patch_size 48 --model_path model_zoo/swinir/hw4_final.pth --folder_lq testsets/test 
```


## Reference


```
@article{he2021transfg,
  title={TransFG: A Transformer Architecture for Fine-grained Recognition},
  author={He, Ju and Chen, Jieneng and Liu, Shuai and Kortylewski, Adam and Yang, Cheng and Bai, Yutong and Wang, Changhu and Yuille, Alan},
  journal={arXiv preprint arXiv:2103.07976},
  year={2021}
}
```
```
@article{liu2021Swin,
  title={Swin Transformer: Hierarchical Vision Transformer using Shifted Windows},
  author={Liu, Ze and Lin, Yutong and Cao, Yue and Hu, Han and Wei, Yixuan and Zhang, Zheng and Lin, Stephen and Guo, Baining},
  journal={International Conference on Computer Vision (ICCV)},
  year={2021}
}
```
