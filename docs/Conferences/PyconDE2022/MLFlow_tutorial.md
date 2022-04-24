# Tutorial "Introduction to MLOps with MLflow"

- Talk page: https://2022.pycon.de/program/DV8PJT/
- Source code for tutorial: https://github.com/tsterbak/pydataberlin-2022 

#### Author:

- Tobias Sterbak
- tobiassterbak.com

- Blog: depends-on-the-definition.com [Tutorial on the blog.] - https://www.depends-on-the-definition.com/

  

## Agenda

- Introduction to MLOps
- MLflow componetnts
- Tracking ML experiments
- Deployment and management
- Trips and tricks.



## What is MLOps and why care?

- Set of tools to 
  - bring ML to production
  - Maintain them
  - Monitor them
- Reduce technial debt
- Lifecycle management



Exploratory Data Analytics &rarr;Data Prepation / Fature engineering &rarr;Model training / tuning &rarrw; Model review and governance (MLFLOw) &rarr; [Something] &rarr;Monitoring &rarr;Automated model retraining 



## Mlflow componenets

1. Tracking
   1. Record and query experiments
2. Projects
3. Models
4. Registry



## Hands-on!

- https://github.com/tsterbak/pydataberlin-2022 

### MLFlow store

- Tracking stores:
  - File store or db store
- Artifact stores
  - Store models, source code, plots etc.
  - S3, GCS etc.



### Setup and configure tracking server

### Tracking

- Scikit-learn: Autologing also available

```python
import mlflow
import mlflow.sklearn
```

- Basic things to track:

  - Parameters: Key-value input parameters: `mlflow.log_param, mlflow.log_params`
  - Metrics: Key-value metrics, where the value is numeric (can be updated over the run): `mlflow.log_metric, mlflow.log_metrics`

  ```python
  mlflow.log_metric("test_accuracy", test_score)   # <-- Track metrics
  mlflow.log_param("num_samples", data.shape[0])  # <-- ADDED: track the number of samples in the dataset
  mlflow.log_artifact("/path/to/file/1_Run and track experiments.ipynb")
  ```

  

### Log the model

```python
mlflow.sklearn.log_model(tree, "model")
```

### Compare models in the UI



### Add a signature to the model



## 2. How to deploy from MLFLow with Python

- Models
- Registered Models

