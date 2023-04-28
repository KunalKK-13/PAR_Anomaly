# Introduction
This repository corresponds to the paper #1 [Real World Anomaly Detection in Surveillance Videos](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8578776)

# Creating Dataset
The I3D features of UCF-Crime is downloaded from here : https://stuxidianeducn-my.sharepoint.com/personal/pengwu_stu_xidian_edu_cn/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Fpengwu%5Fstu%5Fxidian%5Fedu%5Fcn%2FDocuments%2FUCF%2DCrime%2FI3D. <br>

The data is then arranged accordingly : 
```
c3d_features/test/RGB/
|--Abuse
|--Arrest
|--Arson
|--Assault
|--Burglary
|--Explosion
|--Fighting
|--RoadAccidents
|--Robbery
|--Shooting
|--Shoplifting
|--Stealing
|--Vandalism
|--Testing_Normal_Videos_Anomaly

```

# Testing the model
1. The pretrained model is provided in the following table : 

| Dataset      | AUC(%)       | Link                                                                                           |
| ------------ | ------------ | ---------------------------------------------------------------------------------------------- |
| UCF-Crime    |   73.52      | [Model](https://drive.google.com/file/d/1lq2VvOIYbO_fs9Aimqt3TIKTerhFADw9/view?usp=sharing)    |



2. To test the model on the dataset, run the following command : <br><br>
`python infer.py`
