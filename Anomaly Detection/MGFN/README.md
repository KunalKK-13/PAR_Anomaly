# Introduction
This repository corresponds to the paper #4 [MGFN : Magnitude-Contrastive Glance-and-Focus Network for Weakly-Supervised Video Anomaly Detection](https://arxiv.org/pdf/2211.15098v1.pdf)

# Environment and Dependencies
Install dependencies : <br>
`$ pip install -r requirement.txt `

# Creating Dataset
Download the [UCF-Crime dataset](https://connecthkuhk-my.sharepoint.com/personal/cyxcarol_connect_hku_hk/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fcyxcarol%5Fconnect%5Fhku%5Fhk%2FDocuments%2FUCF%2DCrime&ga=1) and arrange the data according to the following tree : <br>

```
data
|--UCF_Test_ten_i3d
|--UCF_Train_ten_i3d
|--ucf-i3d-test.list
|--ucf-i3d.list
```

# Testing the model
1. The pretrained model is provided in the following table : 

| Dataset      | AUC(%)       | Link                                                                                           |
| ------------ | ------------ | ---------------------------------------------------------------------------------------------- |
| UCF-Crime    |   86.98      | [Model](https://drive.google.com/file/d/1Tb1Q1AVpzWukaP7u9q2Zk1E_hk8cswps/view?usp=sharing)    |



2. To test the model on the dataset, run the following command : <br><br>
`$ python test.py ----rgb-list='data-path/ucf_tencrop_1d/ucf-i3d.list' --test-rgb-list='data-path/ucf_tencrop_1d/ucf-i3d-test.list' --gt='data-path/ucf_tencrop_1d/gt-ucf.npy'`
