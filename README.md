# ECG Classification using XGBoost
## Hardware Flow
1. Every wristband capture data and sends them to its corresponding halfway node via LoRaWAN
2. The halfway node pends all collected data and sends them to the central terminal at a hospital via LoRaWAN or cables (if available)
3. The central terminal executes the AI model to evaluate the cases
4. If no abnormal case is detected, process continues. If an abnormal case is detected, an interrupt is triggered to execute the following two steps
5. An simple alert signal (pulse) will be sent via back to the halfway node to inform all the nearby wristband using vibration or buzzar
6. A medical profession at hospital will access the raw data for the abnormal case for diagnosis, and then advice proper measures using voice or texts, which will be displayed on the halfway node
The overall task flow is suggested as the following flowchart.
## Software Flow
The code extracted the features in  the dataset provided by [MIT-BIH Arrhythmia Database](https://www.physionet.org/content/mitdb/1.0.0/), applied some data transformation, and predicted the potential risks base on the wave of the  heartbeats.
### Requirements
Python implementation is on version 3.7.10. 
#### [Python](python)
- [Numpy](https://docs.scipy.org/doc/numpy-1.13.0/user/install.html)
- [Scikit learn](http://scikit-learn.org/stable/install.html)
- [Pandas](https://pandas.pydata.org/docs/getting_started/install.html)
- [XGBoost](https://xgboost.readthedocs.io/en/stable/install.html)
- [keras](https://pypi.org/project/keras/) (Optional)
- [itertools](https://pypi.org/project/more-itertools/) (Optional)
- [Matplotlib](https://matplotlib.org/) (Optional)
### Run the code
1. Download the dataset:
    The dataset is too large to be uploaded to GitHub, thus, users will need to 
    The raw signals files (.csv) and annotations files can be downloaded from [kaggle.com](https://www.kaggle.com/datasets/shayanfazeli/heartbeat)
2. Save it in the right path:
    Put the datasets into ./kaggle/input/heartbeat
3. Train:
    Run the file *ECG.ipynb* block by block. 
    In *ECG2.ipynb*, we use the same algorithm, but different dataset.
    Thank to the powerful XGBoost library, the training time is reduced to less them five minutes.
4. Evaluate:
    The Accuracy and Confusion matrix is shown in the end of the notebook. 
### Result

