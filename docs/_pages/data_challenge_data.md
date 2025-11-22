---
permalink: /data-challenge/data/
title: "RMDC2026 Data"
sidebar:
  nav: "docs"
---
<!-- END PREAMBLE -->

<!-- BEGIN WEB CONTENT -->

The data created for the Roman Microlensing Data Challenge 2026 (RMDC2026) is intended to be a semi-realistic representation of the microlensing data volume and type expected from the Roman Galactic Bulge Time Domain Survey.

It should be noted that in the simulated data, the inertial frame of reference was defined with the $x$-axis increasing from the binary center of mass towards the less massive lens at `t0`, the time of closest approach to the center of mass. If viewed from the solar system barycenter, the inertial frame moves at the relative velocity `vlens_CoM - vobserver(t0)`. The inclination of the orbit is a counter-clockwise rotation about the $x$-axis. $lpha$ is the angle that the source trajectory made with the $x$-axis (if parallax was 0). Where finite source effects were significant, a linear limb darkening law was applied.

## Nexus mounted s3fs

Refer to [this notebook]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/workflow/) for examples of how to access the challenge data, on the Nexus.

## [Hugging Face](https://huggingface.co/RGES-PIT){:target="_blank"}

There are two datasets available for download from the Hugging Face Hub: [`Beginner`](https://huggingface.co/RGES-PIT/Beginner){:target="_blank"} and [`Experienced`](https://huggingface.co/RGES-PIT/Experienced){:target="_blank"}. Each includes challenge data for its tier (`challenge.csv`). The [`Experienced`](https://huggingface.co/RGES-PIT/Experienced){:target="_blank"} repository also includes labeled training data for machine-learning purposes (`train.csv`), with roughly an order of magnitude more events than the challenge set (~100,000 events).  

Below are instructions for downloading the [`Beginner`](https://huggingface.co/RGES-PIT/Beginner){:target="_blank"} dataset. Replace "Beginner" with "Experienced" to download the experienced dataset, which includes more lens arrangements, higher-order effects, and labeled training data. 

### Download Instructions

CLI:
```bash
hf download RGES-PIT/Beginner --repo-type dataset
```

Python:
```python
from huggingface_hub import hf_hub_download
import pandas as pd

REPO_ID = "RGES-PIT/Beginner"
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

<!-- END WEB CONTENT -->
<!-- COPY TO: "bin/data_challenge_data.md" -->
