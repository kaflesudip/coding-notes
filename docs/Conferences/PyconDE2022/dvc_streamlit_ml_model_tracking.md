# Flexible ML Experiment Tracking System for Python Coders with DVC and Streamlit

- https://2022.pycon.de/program/WADNGC/
- Antoine Toubhans
- Slides: https://github.com/sicara/pycon-2022-dvc-streamlit
- YOutube: https://www.youtube.com/watch?v=YOSVMMwTlHM



## Motivation:

- in addition to the code, the data should also be versioned;
- in its essence, ML engineering is an exploratory work: one can not know if the model is going to work before testing it;
- there is no clear way to guarantee the quality of the trained model: the data-scientist has to play with it to make it “talk”.

**DVC **(Data Version Control): Versioning your ML data, code, model

**Streamlit**: Build apps to play with trained models



## MLFLow vs DVC + Streamlit

- MLFlow is complete framework.
- DVC and Streamlit provide you flexibility

## Train pipeline

1. Download_data.py
2. Split_dataset.py
3. train.py
4. evaluate.py



## DVC (Data Version Control)

- What goes to git and what to dvc?
- GIt: 
  - train.py
  - evaluate.py
- `dvc add .`
  - Generates `model.h5.dv` (git tracked)
  - `model.h5` [DVC tracked]

- Data has **non-linear workflow** but classical software enginnering has **linear workflow**

- With dvc, you can return
  - All experiments with given commit hash



## Streamlit

- Strmlit  + DVC don't need any infra
  - unlike MLFlow.
