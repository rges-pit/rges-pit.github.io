---
permalink: /data-challenge/data/
title: "RMDC26 Data"
sidebar:
  nav: "docs"
---
<!-- END PREAMBLE -->

<!-- BEGIN WEB CONTENT -->
<!-- SOURCE (web content): https://github.com/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/Session%20D%3A%20Data%20Challenge%20Q%26A/DATA.md -->

<script>
window.MathJax = {
  tex: {
    inlineMath: [["$", "$"], ["\\(", "\\)"]]
  }
};
</script>
<script async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>

The data created for the Roman Microlensing Data Challenge 2026 (RMDC26) is intended to be a semi-realistic representation of the microlensing data volume and type expected from the Roman Galactic Bulge Time Domain Survey.

In the simulated data, the inertial frame of reference is defined with the $x$-axis increasing from the binary center of mass toward the less massive lens at `t0`, the time of closest approach to the center of mass. When viewed from the Solar System barycenter, the inertial frame moves at the relative velocity `vlens_CoM - vobserver(t0)`. The orbital inclination is a counterclockwise rotation about the $x$-axis. $\alpha$ is the angle between the source trajectory and the $x$-axis when parallax is zero. Where finite-source effects are significant, a linear limb-darkening law is applied.

## Nexus mounted data

Challenge data is mounted on the Nexus at:

| Tier | Nexus path |
| :- | :- |
| Beginner | `/data/data-challenge/rges/RMDC26_Beginner_Tier.parquet` |
| Experienced | `/data/data-challenge/rges/RMDC26_Experienced_Tier.parquet` |

Refer to the [workflow notebook]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/workflow/) for examples of accessing these files on the Nexus.

## [Hugging Face](https://huggingface.co/RGES-PIT){:target="_blank"}

The two challenge datasets are also available as Parquet files from the Hugging Face Hub:

| Tier | Hugging Face repository | Filename | Contents |
| :- | :- | :- | :- |
| Beginner | [`RGES-PIT/Beginner`](https://huggingface.co/datasets/RGES-PIT/Beginner){:target="_blank"} | `RMDC26_Beginner_Tier_test.parquet` | 188 events; 9,230,048 observations; 14 columns |
| Experienced | [`RGES-PIT/Experienced`](https://huggingface.co/datasets/RGES-PIT/Experienced){:target="_blank"} | `RMDC26_Experienced_Tier_test.parquet` | 2,087 events; 103,281,456 observations; 18 columns |

The `_test` suffix allows Hugging Face to identify these challenge files as the test split for its Dataset Viewer. It does not indicate a difference in scientific content from the corresponding Nexus files, whose filenames omit `_test`.

The Beginner dataset contains photometric light curves. The Experienced dataset adds astrometric measurements and includes more complex lens and source configurations. The Experienced sample was filtered for likely anomalous events and is therefore not representative of the complete event population expected from Roman.

### [Machine Learning Training Data](https://huggingface.co/datasets/RGES-PIT/MachineLearning){:target="_blank"}

The separate [`RGES-PIT/MachineLearning`](https://huggingface.co/datasets/RGES-PIT/MachineLearning){:target="_blank"} dataset provides labeled simulations for training and benchmarking machine-learning models for event classification, parameter estimation, and anomaly detection. It contains 372,655 events and is organized into three related Parquet tables:

| Table | Filename | Contents |
| :- | :- | :- |
| Observations | `RMDC26_ML_Data_obs.parquet` | 18,441,855,367 time-series observations |
| Metadata | `RMDC26_ML_Data_meta.parquet` | Event labels, physical parameters, and population weights |
| Epochs | `RMDC26_ML_Data_epoch.parquet` | 98,974 observation times and telescope positions |

The observations table is approximately 172 GB and should not normally be downloaded or loaded into memory in full. The Hugging Face dataset card includes examples for querying individual events remotely and joining the three tables.

The raw event distribution is not directly representative of the expected Roman population. Use the `final_weight` column in the metadata table to weight events during training and analysis or to construct a more representative resampled dataset.

### Challenge Data Download Instructions

CLI:
```bash
# Beginner tier
hf download RGES-PIT/Beginner RMDC26_Beginner_Tier_test.parquet \
    --repo-type dataset

# Experienced tier
hf download RGES-PIT/Experienced RMDC26_Experienced_Tier_test.parquet \
    --repo-type dataset
```

Python:
```python
from huggingface_hub import hf_hub_download
import pandas as pd

datasets = {
    "Beginner": (
        "RGES-PIT/Beginner",
        "RMDC26_Beginner_Tier_test.parquet",
    ),
    "Experienced": (
        "RGES-PIT/Experienced",
        "RMDC26_Experienced_Tier_test.parquet",
    ),
}

tier = "Beginner"
repo_id, filename = datasets[tier]

local_path = hf_hub_download(
    repo_id=repo_id,
    filename=filename,
    repo_type="dataset",
)
dataset = pd.read_parquet(local_path)
```

Git:
```bash
git lfs install

# Clone the repository for the tier you need
git clone git@hf.co:datasets/RGES-PIT/Beginner
git clone git@hf.co:datasets/RGES-PIT/Experienced
```

<!-- END WEB CONTENT -->
<!-- COPY TO: "bin/data_challenge_data.md" -->
