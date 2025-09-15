---
permalink: /data-challenge/
title: "Roman Microlensing Data Challenge 2025 (RMDC25)"
sidebar:
    nav: "docs"
---

<!-- sign up button -->
<div style="text-align: center; margin: 2em 0;">
  <a href="{{ site.url }}{{ site.baseurl }}/data-challenge/sign-up/" style="background-color: #a859e4; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Sign Up for RMDC25</a>
</div>

RMDC25 aims to:
- Encourage more people to join the field
- Encourage adoption of microlensing tools
- Encourage development and innovation
in preparation for the Roman mission.

Roman is expected to detect tens of thousands of microlensing events during its prime mission and thousands of exoplanets, probing fundamentally different regions of exoplanet parameter space than earlier missions.

<!-- Add a figure? -->

The data in this challenge is intended to be a semi-realistic representation of the microlensing data volume and type expected from the Roman Galactic Bulge Time Domain Survey. 

Our official launch will be during AAS 247, where we will host a [workshop]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/) covering various aspects of the Data Challenge (specific date and time TBD).

## Important Dates

| Milestone | Date |
| :- | -: |
| Challenge sign-up opens | early December 2025 |
| Kick-off workshop at AAS 247 | January 3 or 4, 2026 |
| Submission deadline | April 2026 |
| Evaluation begins | May 2026 |
| Evaluation panel discussions | July 2026 |
| Evaluation panel final reports due | July 2026 |

## Important Links

- [Data]({{ site.url }}{{ site.baseurl }}/data-challenge/data/)
- [Nexus]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/1-nexus/)
- [AAS 247 Workshop]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/)
- [Sign up]({{ site.url }}{{ site.baseurl }}/data-challenge/sign-up/) (*sign-up is not currently open*).
- [Help form]({{ site.url }}{{ site.baseurl }}/data-challenge/help/)

## Challenge Overview

### Ground Rules

1) Document dependencies and CPU hours.  
2) All developed code should be documented and open source.  
3) One final submission per team.  
4) Submissions must pass format validation with the submission tool.  
5) One designated team lead/contact person.  
6) Communication with experienced microlensers is encouraged.  

### Challenge Tiers

RMDC25 will offer two challenge tiers: a beginner tier for those new to microlensing and an experienced tier for veteran microlensers. Anyone can participate in either tier, but the beginner tier is not intended for entire teams with extensive microlensing modeling experience. Teams may make submissions in both tiers.

### Participant Goals

1) Classify all targets.  
2) Fit appropriate models to the microlensing events and tabulate the parameters derived in each case, optionally including derived physical parameters.  
3) Describe the approach taken to modeling; the software and hardware used; and any innovations in modeling or classification made in response to the challenge.  
4) Optional: provide plotted output for each model and posterior samples.  

### Submission

Submissions are validated using the [`microlens-submit`](https://microlens-submit.readthedocs.io/en/latest/){:target="_blank"} tool. It validates and packages submissions and creates draft dossiers so you can preview how your submission will look to evaluators. It is also useful for managing your many events and solutions and tracking your progress. You can use this tool through the CLI or Python API. It installs as a Python package via pip:

```bash
pip install microlens-submit
```

The `microlens-submit` documentation includes [detailed specifications](https://microlens-submit.readthedocs.io/en/latest/submission_manual.html){:target="_blank"} for how to create a submission. **Strict adherence to the submission criteria is required**, as much of the evaluation process is automated.

### Evaluation

The evaluation panel will assess each team’s entry on the following criteria:

| # | Criterion | Points |
| :-: | :- | -: |
| 1 | Accuracy of model parameters | 5 |
| 2 | Number of events modeled | 5 |
| 3 | Software/computational efficiency | 5 |
| 4 | Innovation | 5 |
| 5 | Broadening the field by bringing in new researchers | 5 |

You can find a copy of the evaluation rubric [here](https://rges-pit.org/data-challenge){:target="_blank"}.

## Microlensing Resources and References

* [AAS 247 RMDC2025 workshop content]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/) specifically related to this Data Challenge (**not yet released**).
* [RGES-PIT resources page]({{ site.url }}{{ site.baseurl }}/resources/) for other helpful resources and RGES-PIT/Roman-specific information.  
* [RGES-PIT tools page]({{ site.url }}{{ site.baseurl }}/tools/) for links to open-source microlensing tools.  
* [REU2025]({{ site.url }}{{ site.baseurl }}/outreach_mini_landing/) introductory mini course.
* [RGES-PIT GitHub Organization](https://github.com/rges-pit){:target="_blank"}.
* [RMDC2025 ADS Library](https://ui.adsabs.harvard.edu/public-libraries/gRI3mf-LQAGs3HbN4fuRSg){:target="_blank"} of useful microlensing papers and reviews.  
* [Microlensing Source](https://www.microlensing-source.org/){:target="_blank"}.  
* [TMGTTG](https://github.com/AmberLee2427/TheMicrolensersGuideToTheGalaxy.git){:target="_blank"} introductory notebook series.  
* [2017 Sagan Workshop](http://nexsci.caltech.edu/workshop/2017/){:target="_blank"} in microlensing. The recordings from this workshop can be found [here](https://www.youtube.com/watch?v=QPfKucBb9B8&list=PLIbTYGsIVYthWRS14eCEK8SK9IOTcaYsf){:target="_blank"}. 
* [Glossary of Terms](https://www.microlensing-source.org/glossary/){:target="_blank"}.  
* Ask [Nancy](https://rmdc2025.slack.com/archives/D098SMZTNR2){:target="_blank"} on the RMDC2025 Slack. <!-- or connect to her MCP server -->

## Contact

* [Contact us page]({{ site.url }}{{ site.baseurl }}/data-challenge/help/)
* Open an Issue on GitHub (see issues tab on the appropriate [`microlens-submit`](https://github.com/rges-pit/microlens-submit/issues){:target="_blank"} or [`data-challenge-notebooks`](https://github.com/rges-pit/data-challenge-notebooks/issues){:target="_blank"} repo.)
* Message us on the [`#general`](https://rmdc2025.slack.com/archives/C096QG09P5F){:target="_blank"} channel on the RMDC2025 Slack workspace.
