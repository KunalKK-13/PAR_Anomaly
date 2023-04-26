# Environment and Dependencies
1. Create conda environment with python version : **3.7.6**<br>
`conda create -n env_name python=3.7.6`
2. Install all the required packages <br>
`pip install -r requirements.txt`

# Creating Datasets
There are 6 datasets used in the experiments. Three parent datasets : [PETA](https://drive.google.com/drive/folders/1q4cux17K3zNBgIrDV4FtcHJPLzXNKfYG), [RAP(v1)](http://www.rapdataset.com/), [PA100k](https://drive.google.com/drive/folders/0B5_Ra3JsEOyOUlhKM0VPZ1ZWR2M?resourcekey=0-CdctEkdX1j2GSMSWWfrPSQ) and three derived datasets : peta_frontal, rap_frontal, pa100k_frontal. <br>
The direct download-able links are provided. Arrange the data by following the given tree directory : 
```
data
|--PETA
|   |--images
|   |--dataset.pkl
|--RAP
|   |--RAP_dataset
|   |--dataset.pkl
|--PA100k
|   |--data
|   |--dataset.pkl
|--peta_frontal
|   |--dataset.pkl
|--rap_frontal
|   |--dataset.pkl
|--pa100k_frontal
    |--dataset.pkl
```
The frontal version of each dataset contain the *.pkl* of the respective folder. The facial region images can be downloaded from [here](https://drive.google.com/drive/folders/1t9xvksiqQnwS2pWyGB-0oLWJbrBvesYT?usp=sharing). Each dataset zip has the folder `face_images`, which should be added to PETA, RAP and PA100k, in `data`.
# Testing the models
The checkpoint file against each training is provided along with the results. <br>
There are two variables in the *infer script* named `DATASET` and `DATASET_MODEL`. You need to change both to one of the **six possible names**: PETA, RAP, PA100k, peta_frontal, rap_frontal, or pa100k_frontal. <br> <br>
For testing, use the model for each dataset and change the path in `MODEL_CKPTS` in the *infer script*. Then run the following command : <br>
`bash infer.sh` <br> <br>
The checkpoints for each dataset is provided in the following table : 
| Dataset        | mA    | model       |
|----------------|-------|-------------|
| PETA           | 92.88 | [checkpoints](https://drive.google.com/file/d/1MSCLnSgorFGJB9-Zx65kjoPSA2wchStQ/view?usp=share_link) |
| PETA<sub>Frontal</sub>     | 92.18 | [checkpoints](https://drive.google.com/file/d/1Ici9pauDOd7q9ErriOvYgWYCxv2pBOSi/view?usp=share_link) |
| PA-100K        | 90.76 | [checkpoints](https://drive.google.com/file/d/146jL0lkbWv03FP62Vs8HnzBYeThd_2Qn/view?usp=share_link) |
| PA-100K<sub>Frontal</sub> | 92.70 | [checkpoints](https://drive.google.com/file/d/1Xkdq-T7tewaMr2zDIXs7TJQF8btd6WXR/view?usp=share_link) |
| RAP            | 95.95 | [checkpoints](https://drive.google.com/file/d/1-_QLqn2ZLym7Be9j9Dk_NfJ-6mRU5d1S/view?usp=share_link) |
| RAP<sub>Frontal</sub>    | 96.56 | [checkpoints](https://drive.google.com/file/d/1kqsxAgK0mZeAERbU_vJzQ3VRFae_vfHn/view?usp=share_link) |
---

# Example
1. Infer script for PETA dataset
<img src="imgs/peta-infer-script.jpg">
2. Result for PETA dataset
<img src="imgs/peta-test-res.jpg">

