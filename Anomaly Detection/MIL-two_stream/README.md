# Introduction
This repository corresponds to the paper #2 
[Anomaly Event Detection in Security Surveillance Using Two-Stream Based Model](https://downloads.hindawi.com/journals/scn/2020/8876056.pdf)

# Creating Dataset
1. The I3D features (both rgb and flow) of UCF-Crime is downloaded from here : https://drive.google.com/file/d/18nlV4YjPM93o-SdnPQrvauMN_v-oizmZ/view?usp=sharing
2. The files `train_anomaly.txt` `train_normal.txt` `test_anomaly.txt` `test_normal.txt` given in the repo are to be arranged according to the given tree : 

```
DATA
|--UCF-Crime
|   |--all_rgbs/
|   |--all_flows/
|   |--train_anomaly.txt
|   |--train_normal.txt
|   |--test_anomaly.txt
|   |--test_normal.txt
```

# Testing the model
1. The following result was obtained after 75 epochs : 

| Dataset      | AUC(%)       |
| ------------ | ------------ | 
| UCF-Crime    |   84.45      |



2. To test the model on the dataset, run the following command : <br>
`$ python main.py`
