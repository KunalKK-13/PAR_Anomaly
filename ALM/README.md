# Environment and Dependencies
1. Python version = 3.6+
2. Pytorch version = 0.4+

# Creating Datasets
1. Download the data from the following links : [PETA](https://www.dropbox.com/s/52ylx522hwbdxz6/PETA.zip?dl=0), [RAP(v1)](http://www.rapdataset.com/), [PA100K](https://drive.google.com/drive/folders/0B5_Ra3JsEOyOUlhKM0VPZ1ZWR2M?resourcekey=0-CdctEkdX1j2GSMSWWfrPSQ)
2. Arrange the data directory in the following tree structure : 
```
data
|--peta
|   |--PETA_dataset
    |   |--3DPeS
        |--CAVIAR4REID
        |--CUHK
        |--GRID
        |--i-LID
        |--MIT
        |--PRID
        |--SARC3D
        |--TownCentre
        |--VIPeR
|--rap
|   |--RAP_dataset
    |--RAP_annotation
    |   |--RAP_annotation.mat
        |--rap_evaluation.m
        |--ReadMe.txt
|--pa100k

```
4. Change the `data-path` in the `utils/datasets.py` file in line 183-197

# Pretrained Models
The models are provided to run the test script.
| Dataset | mA    | Link                                                         |
| ------- | ----- | ------------------------------------------------------------ |
| PETA    | 86.34 | [Model]() |
| RAP     | 81.86 | [Model]() |
| PA-100K | 80.45 | [Model]() |

# Experiment
Change the `experiment` argument to peta, rap and pa100k accordingly. Then run the following script : <br><br>
`python main.py --approach=inception_iccv --experiment=rap -e --resume='model_path'`
