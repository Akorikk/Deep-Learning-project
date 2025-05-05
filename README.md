# Deep-Learning-project

# This repository contains a modular and scalable deep learning pipeline for analyzing CT scan images. It is designed for medical imaging tasks such as classification, detection, and segmentation using modern deep learning frameworks.

* i have writen my common funcationalty inside utils common.py i have writen all my helper functions which i will be useing later, so in utils i have used something called @ensure_annotations on every function, let me explain what is the role of @ensure_annotations,

 The decorator @ensure_annotations is not a built-in Python function — it's from the third-party library ensure. It’s used to enforce type annotations at runtime.It checks that the inputs and outputs of your function match the types you declared in the function’s signature. If there's a mismatch, it will raise a TypeError.
 
example --> def add(x: int, y: int) -> int:
    return x + y

add("hello", 3)  # no error from Python, even though x should be int

and with @ensure_annotations 
from ensure import ensure_annotations

@ensure_annotations
def add(x: int, y: int) -> int:
    return x + y

add("hello", 3)  # ❌ This will raise a TypeError at runtime

## Why is it useful?
 * You often work with functions that take Path, dict, list, str, etc.
* Using @ensure_annotations helps catch bugs early by validating types at runtime.
* It improves code reliability, especially in larger projects.

just type pip install ensure and your ready to use 


## Pipelines
1. Workflows
2. Update config.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline
8. Update the main.py
9. Update the dvc.yaml

* Data Ingestion

* IMPORTANT  when we do data ingestion task we should not keep our params.yaml file empty because whenever you will executing it will throw error, for that just take one key dummy value example i have taken key: val, later on you can changes it will all the model parameters 

Data Ingestion is the process of collecting and importing data from various sources into a system where it can be stored, processed, and analyzed.

It's like gathering raw ingredients before cooking. You're pulling data from different places so your data science models or analysis can use it.

🧩 Sources of Data:
Databases (SQL, NoSQL)

APIs (Twitter API, weather APIs)

Files (CSV, Excel, JSON, XML)

Cloud storage (AWS S3, Google Cloud Storage)

Web scraping

IoT devices or sensors