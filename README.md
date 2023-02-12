## ECG Classification using XGBoost
The code extracted the features in  the dataset provided by MIT-BIH Arrhythmia Database(https://www.physionet.org/content/mitdb/1.0.0/), applied some data transformation, and predicted the potential risks base on the wave of the  heartbeats.

## Requirements

Python implementation is on version 3.7.10. 

### [Python](python)

- [Numpy](https://docs.scipy.org/doc/numpy-1.13.0/user/install.html)
- [Scikit learn](http://scikit-learn.org/stable/install.html)
- [Pandas](https://pandas.pydata.org/docs/getting_started/install.html)
- [XGBoost](https://xgboost.readthedocs.io/en/stable/install.html)
- [keras](https://pypi.org/project/keras/)
- [itertools](https://pypi.org/project/more-itertools/)
- [Matplotlib](https://matplotlib.org/) (Optional)

## Run the code
 
1. Download the dataset:
    The raw signals files (.csv) and annotations files can be downloaded from [kaggle.com](https://www.kaggle.com/datasets/shayanfazeli/heartbeat)
    
2. Save it in the right path:
    Put the datasets into ./kaggle/input/heartbeat

3. Train:
    Run the file *ECG.ipynb* block by block. 
    In *ECG2.ipynb*, we use the same algorithm, but different dataset.
    Thank to the powerful XGBoost library, the training time is reduced to less them five minutes.

4. Evaluate:
    The Accuracy and Confusion matrix is shown in the end of the notebook. 
