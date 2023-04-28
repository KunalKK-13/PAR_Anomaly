# Introduction
This repository corresponds to the paper #2 [Improving Person Re-identification by Attribute and Identity Learning](https://arxiv.org/abs/1703.07220)

# Dependencies
The following packages needs to be downloaded : 
* Python 3.5
* PyTorch >= 0.4.1
* torchvision >= 0.2.1
* matplotlib, sklearn, prettytable (optional)

# Creating Datasets
1. Download the data from the following link : [Market-1501](https://www.kaggle.com/datasets/pengcw1/market-1501)
2. Download the [Market-1501-Attribute](https://github.com/vana77/Market-1501_Attribute) annotations.
3. Arrange the data directory in the following tree structure : 
```
dataset
|--Market-1501
|   |--bounding_box_train
    |--bounding_box_test
    |--gt_bbox
    |--gt_query
    |--query
    |--readme.txt
    |--attribute
    |   |--market_attribute.mat

```


# Pretrained Models
1. The models are provided to run the test script.

| Dataset | mA    | Link                                                         |
| ------- | ----- | ------------------------------------------------------------ |
| Market-1501_Attribute     | 81.73 | [Model](https://drive.google.com/file/d/19e3YvAhlXGHTXAfzCS9zW8Y-dm0p9gMJ/view?usp=share_link)                                                    |

2. Download the model and move it to the `checkpoints` folder in the project directory.


# Experiment
Run the following command to test the pretrained model on the Market-1501_attribute dataset : <br><br>
`python3  test.py   --data-path  ~/dataset  --dataset  [market]  --model  resnet50  [--print-table]`

