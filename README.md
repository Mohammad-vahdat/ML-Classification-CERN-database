# Project : Detecting Higgs Boson

The Higgs Boson is an elementary particle in the standard model of physics, which is proposed to explain why particles have mass. The boson's existence was confirmed in 2012 based on collisions in the Large Hadron Collider (LHC) at CERN. We got some data from the Large Hadron Collider at CERN. The deterministic analysis of data is intensely hard because of the huge volume of the data and the complexity of the physical processes. We want to estimate the likelihood that the signature of a given event is the result of a Higgs Boson, namely signal, or some other process/particle, namely background noise. The goal is to predict whether this event is a signal or a background. Hence, we propose a Machine Learning approach for binary classification. 

![image](https://user-images.githubusercontent.com/57172944/168263128-7e11d8e2-2118-4ed5-bbd3-2fc93dee0dd7.png)


## Project Structure

The project is organized as follows:

    .
    ├── data                     # Train and test datasets.
        ├──sub_datasets          # Splitting datasets into 8 sub-datasets.

    ├── scripts                  # files to pre-process, train and test datasets.
    │   ├── helper_functions.py   
    │   ├── proj1_helpers.py     
    │   ├── implementations.py   

    ├── README.md                # README file.

    ├── report                   # The requested report.

    └── run_reg_logestic_regression.py      # Script to train the regularized logestic regression model. This is the one that we submitted.
    
    └── run_ridge_regression.py  # Script to train the ridge regression model.

    └── run_test.py              # compare 6 different methods.

    └── Final_Prediction-Submitted.csv     # Final predictions (Categorical Accuracy = 0.837, F1-Score = 0.754)
    
## Running

Before running the code, please make sure that the train.csv and test.csv files are in the `data` folder. You just need to unzip the files : `data\train.zip` and `data\test.zip` in the data folder.

To reproduce our results, the one we submitted, you just need to run the following command:

``` 
python run_reg_logestic_regression.py
```

After running the script, you can find the generated predictions in the same folder that you are. Our final predictions are in the `Final_Prediction-Submitted.csv` file for comparison.

Note: After running the code, we make a sub-folder in data folder. So, if you want to run the code another time, please make sure that you have deleted this sub-folder before running. 

#------------------

Beside the regularized logestic regression metheod, we implemented the ridge regression method as well. To see the result of this method, you need to run the following command: 

``` 
python run_ridge_regression.py
```
#------------------

Finally, in order to make a comparison between 6 different methods, you need to run the following command: 

``` 
python run_test.py
```

At the end of this section, we just understand in our case the best way is using the regularized logestic regression method.

## Author

* Mohammad Tohidivahdat     mohammad.vahdat@epfl.ch

