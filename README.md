# End to End Data Science Project

### Workflows--ML Pipeline

1. Data Ingestion
2. Data Validation
3. Data Transformation-- Feature Engineering,Data Preprocessing
4. Model Trainer
5. Model Evaluation- MLFLOW,Dagshub

## Workflows

1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py

# End-to-End Data Science Project

This project implements a complete **Machine Learning pipeline** with configuration management, modular components, and experiment tracking using **MLflow** (local or DagsHub).  

---

## ML Pipeline Steps (Functional Workflow)

These are the main steps executed by the pipeline:

| Step | Description |
|------|-------------|
| **Data Ingestion** | Download or load raw data from sources. |
| **Data Validation** | Check schema, missing values, and data quality. |
| **Data Transformation** | Feature engineering, preprocessing, and cleaning. |
| **Model Trainer** | Train ML models using processed data. |
| **Model Evaluation** | Test models, compute metrics, and log to MLflow/DagsHub. |

---

## Project Workflows (Maintenance & Updates)

These are tasks to maintain or extend the project. They support the ML pipeline:

1. **Update `config.yaml`** – artifact paths, directories, or URLs.  
2. **Update `schema.yaml`** – dataset columns or target changes.  
3. **Update `params.yaml`** – hyperparameters for model training.  
4. **Update entity classes** – e.g., `DataIngestionConfig`, `ModelTrainerConfig`.  
5. **Update `ConfigurationManager`** – reflect new configs or pipeline components.  
6. **Update components** – modify logic for ingestion, transformation, trainer, etc.  
7. **Update pipeline** – integrate all components sequentially.  
8. **Update `main.py`** – orchestrate the pipeline execution.

---

## Relationship Between Pipeline Steps and Workflow Items

| Pipeline Step | Related Workflow Tasks |
|---------------|----------------------|
| Data Ingestion | `config.yaml`, entity classes, components |
| Data Validation | `schema.yaml`, components |
| Data Transformation | `config.yaml`, `schema.yaml`, components, pipeline |
| Model Trainer | `params.yaml`, components, pipeline |
| Model Evaluation | `config.yaml`, components, pipeline, MLflow/DagsHub setup |

**Explanation:**  
- **Pipeline steps** = the “machine” that runs ML tasks.  
- **Workflow items** = the “tools and controls” that ensure the machine runs correctly.  
- Updating any pipeline step often requires modifying multiple workflow items to maintain consistency.

---

## MLflow Integration

- **Local MLflow**: run `mlflow ui` and set URI to `http://127.0.0.1:5000`.  
- **DagsHub MLflow**: set tracking URI to your repo MLflow endpoint, e.g.,  
  `https://dagshub.com/<username>/<repo>.mlflow`.  
- Artifacts are logged to MLflow, metrics are tracked, and models can be downloaded from the MLflow tab.  

---

## Folder Structure (Recommended)

