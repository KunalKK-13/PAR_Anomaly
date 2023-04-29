# Introduction
This repository corresponds to the paper #3 
[Weakly-supervised Video Anomaly Detection with Robust Temporal Feature Magnitude Learning](https://arxiv.org/pdf/2101.10030v3.pdf)

# Environment and Dependencies
Install dependencies : <br>
`$ pip install -r requirement.txt `

# Creating Dataset
Download the extracted I3d features for ShanghaiTech and UCF-Crime dataset from links below :
1. [**ShanghaiTech features on Google dirve**](https://drive.google.com/file/d/1-w9xsx2FbwFf96A1y1GFcZ3odzdEBves/view?usp=sharing)
2. [**UCF-Crime train I3d features on Google drive**](https://drive.google.com/file/d/16LumirTnWOOu8_Uh7fcC7RWpSBFobDUA/view?usp=sharing)
3. [**UCF-Crime test I3d features on Google drive**](https://drive.google.com/drive/folders/1QCBTDUMBXYU9PonPh1TWnRtpTKOX-fxr?usp=sharing)

Change the file paths to the download datasets above in `list/shanghai-i3d-test-10crop.list` , `list/shanghai-i3d-train-10crop.list' , `ucf-i3d.list`, and `ucf-i3d-test.list`

# Testing the model
1. The pretrained model is provided in the following table : 

| Dataset      | AUC(%)       | Link                                                                                           |
| ------------ | ------------ | ---------------------------------------------------------------------------------------------- |
| ShanghaiTech    |   97.21      | [Model](https://drive.google.com/file/d/1Tb1Q1AVpzWukaP7u9q2Zk1E_hk8cswps/view?usp=sharing) |
| UCF-Crime       |   84.03      | [Model]() |



2. To test the model on the dataset, run the following command : <br><br>
```shell
python -m visdom.server
python main.py
```
