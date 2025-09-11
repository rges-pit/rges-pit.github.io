---
permalink: /data-challenge/data/
title: "Data Challenge Data"
sidebar:
  nav: "docs"
---


## Nexus mounted server thingy


## [Hugging Face](https://huggingface.co/RGES-PIT)

Hugging FaceThere are two datasets available for download from HuggingFace Hub. These include the. [`Beginner`](https://huggingface.co/RGES-PIT/Beginner) and [`Experienced`](https://huggingface.co/RGES-PIT/Experienced) datasets. Below are instructions for downloading the [`Beginner`](https://huggingface.co/RGES-PIT/Beginner) dataset. Replace "Beginner" with "Experienced" to download the experienced data sets included more lens arrangements and higher order effects. 

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
FILENAME = "train.csv"

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
