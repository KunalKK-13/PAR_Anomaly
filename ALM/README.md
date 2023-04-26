# Environment and Dependencies
1. Python version = 3.6+
2. Pytorch version = 0.4+

# Creating Datasets

1. Change the *data-path* in the *utils/datasets.py* file in line 183-197

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
