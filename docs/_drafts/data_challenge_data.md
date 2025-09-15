---
permalink: /data-challenge/data/
title: "Data Challenge Data"
sidebar:
  nav: "docs"
---

## Nexus mounted s3fs

Refer to [this notebook]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/workflow/) for examples of how to access the challenge data, on the Nexus.

## [Hugging Face](https://huggingface.co/RGES-PIT){:target="_blank"}

There are two datasets available for download from HuggingFace Hub. These include the. [`Beginner`](https://huggingface.co/RGES-PIT/Beginner){:target="_blank"} and [`Experienced`](https://huggingface.co/RGES-PIT/Experienced){:target="_blank"} datasets. These include challenge data for each tier (`"challenge.csv"`). The [`Experienced`](https://huggingface.co/RGES-PIT/Experienced){:target="_blank"} repo includes training data for machine learning purposes (`"train.csv"`), labeled, with an order of magnitude more events than the challenge set (~100 000 events).  

Below are instructions for downloading the [`Beginner`](https://huggingface.co/RGES-PIT/Beginner){:target="_blank"} dataset. Replace "Beginner" with "Experienced" to download the experienced datasets, including more lens arrangements and higher order effects and labeled training data. 

### Download Instructions

CLI:
```bash
hf download RGES-PIT/Beginner --repo-type dataset
```

Python:
```python
from huggingface_hub import hf_hub_download
import pandas as pd

REPO_ID = "YRGES-PIT/Beginner"
FILENAME = "challenge.csv"

dataset = pd.read_csv(
    hf_hub_download(
        repo_id=REPO_ID, 
        filename=FILENAME, 
        repo_type="dataset")
    )
```

Git:
```bash
git lfs install

# git clone git@hf.co:datasets/<dataset ID>
git clone git@hf.co:datasets/RGES-PIT/Beginner  
```
