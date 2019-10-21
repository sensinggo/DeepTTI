# DeepTTI

This project is the code of ***Transportation Type Identification (TTI)***.

We provide the sampled code and part of dataset in SensingGO. You can replace the sample data with your own dataset.
Please see the samples in data folder for more details.

The complete data can be downloaded at 
https://https://sensinggo.org/

# Usage:

## Model Training
python train.py

### Parameters:

* task: train/test
* batch_size: the batch_size to train, default 400
* epochs: the epoch to train, default 100
* kernel_size: the kernel size of Geo-Conv, only used when the model contains the Geo-conv part
* pooling_method: attention/mean
* alpha: the weight of combination in multi-task learning
* log_file: the path of log file
* result_file: the path to save the predict result. By default, this switch is off during the training

Example:
```
python main.py --task train  --batch_size 10  --result_file ./result/deeptte.res --pooling_method attention --kernel_size 3 --alpha 0.1 --log_file run_log
```


## Model Evaluation

### Parameters:
* weight_file: the path of model weight
* result_file: the path to save the result

## Example:
```
python main.py --task test --weight_file ./saved_weights/weight --batch_size 10  --result_file ./result/deeptte.res --pooling_method attention --kernel_size 3 --alpha 0.1
```

## How to User Your Own Data
In the data folder we provide some sample data. You can use your own data with the corresponding format as in the data samples. The sampled data contains 1800 trajectories. To make the model performance close to our proposed result, make sure your dataset contains more than 5M trajectories.

### Format Instructions
 Updating...
 
 # Demo video:
[![IMAGE ALT TEXT](https://img.youtube.com/vi/vek4OLE3Yio/0.jpg)]
(https://youtu.be/vek4OLE3Yio "Hit to demo video on Youtube.")
 
