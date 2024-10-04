# model-experimentation

Machine learning model experimentation for an American retail company.

## Project Execution

```
The steps required to execute this project are:
1. Starting point is the eda folder. 'bajaj_sidhant-25246568-eda.ipynb' is the initial file which performs eda and data cleaning. This notebook consumes the 'dataset.zip' which contains all the files. Once all the cells are executed, it will generate 4 files. 
    i. 'train_data_cleaned.csv' and 'test_data_cleaned.csv' will be used for transformation.
    ii. 'calendar_events.csv' is created for the forecast model .
    iii. 'items_id.json' file contains list of all the item ids that will be used by streamlit.
2. After running the eda file, "bajaj_sidhant-25246568-data_tranformation_forecasting.ipynb" and "bajaj_sidhant-25246568-data_tranformation_prediction.ipynb" need to be executed to apply transformation to the data based on the respective models.
    i. Forecasting notebok will generate - 'train_forecasting.csv', 'test_forecasting.csv' and 'holiday_data.csv
    ii. Prediction notebook will generate:
        a. CSVs: 'train_processed_1.csv', 'test_processed_1.csv'
        b. Transformers: 'target_mean_encoder_1.joblib', 'ordinal_encoder_1.joblib', 'scaler_1.joblib'
3. The predictive and forecast folder contains the experiments conducted on various models. The prophet notebook in the forecast folder generates 'prophet_1.joblib' file. The xgboost notebook produces the best model and generates "xgb4.joblib" file. 

The final report is added to the reports folder.

Custom package used - https://test.pypi.org/project/cstm_pkg_grp_9/

NOTE:
The joblib files are transferred to the backend directory for further usage. 
The csv files that are generated using the notebooks is not pushed to github due to their heavy size and are ignored using github. These files can be generated using above steps.
```
## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         model_experimentation and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── model_experimentation   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes model_experimentation a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations
```

--------

