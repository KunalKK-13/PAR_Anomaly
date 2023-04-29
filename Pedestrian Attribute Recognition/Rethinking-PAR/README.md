# Dependencies

- python 3.7
- pytorch 1.7.0
- torchvision  0.8.2
- cuda 10.1


# Creating Dataset
1. Download the datasets from the following links : [PETA](https://drive.google.com/drive/folders/1q4cux17K3zNBgIrDV4FtcHJPLzXNKfYG), 
2. [RAP(v2)](http://www.rapdataset.com/) , and [PA100k](https://drive.google.com/drive/folders/0B5_Ra3JsEOyOUlhKM0VPZ1ZWR2M?resourcekey=0-CdctEkdX1j2GSMSWWfrPSQ)
3. Prepare datasets to have following structure:
    ```
    ${project_dir}/data
        PETA
            images/
            PETA.mat
            dataset_all.pkl
            dataset_zs_run0.pkl
        PA100k
            data/
            dataset_all.pkl
        RAP2
            RAP_dataset/
            RAP_annotation/
            dataset_zs_run0.pkl
    ```
    
# Training 
The baseline based on resnet50 trained using the command : 
    ```
    sh train.sh
    ``` 
