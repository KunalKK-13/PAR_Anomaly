# Introduction
This repository corresponds to the paper #1 [Real World Anomaly Detection in Surveillance Videos](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8578776)

# Environment and Dependencies
Install dependencies : <br>
`$ pip install -r requirement.txt `

# Creating Dataset
The I3D features of UCF-Crime is downloaded from here : https://stuxidianeducn-my.sharepoint.com/personal/pengwu_stu_xidian_edu_cn/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fpengwu%5Fstu%5Fxidian%5Fedu%5Fcn%2FDocuments%2FUCF%2DCrime%2FI3D
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
