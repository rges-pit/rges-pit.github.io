---
permalink: /data-challenge/aas-workshop/1-nexus/
title: "Introduction to the Roman Research Nexus (The Nexus)"
sidebar:
  nav: "workshop"
---
<!-- END PREAMBLE -->

<!-- BEGIN WEB CONTENT -->
<!-- SOURCE (web content): https://github.com/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/Session%20A%3A%20Nexus/ReadMe.md -->

The Roman Research Nexus (aka “the Nexus”) is a JupyterHub service, provided by Space Telescope Science Institute (STScI), with public, shared compute resources, intended for Roman-related data analysis. The Nexus is a high-level processing environment for Roman science data that is in close network proximity to cloud data storage.

Compute power is limited and use of resources expends tokens. Teams who are registered participants of the Roman Microlensing Data Challenge 2026 (RMDC26) or the Roman Galactic Exoplanet - Project Infrastructure Team (RGES-PIT) can chose the team they wish to open a server under and charge usage to. Please refrain from using Nexus resources for tasks unrelated to Roman data or your team's intended purpose.

If you encounter difficulties or have questions while using the Nexus, please contact the STScI help desk (see the button below).

<!-- Login, sign up, and help buttons -->
<div style="text-align: center; margin: 2em 0; display: flex; justify-content: center; gap: 1em; flex-wrap: wrap;">
  <a href="https://roman.science.stsci.edu/hub/" target="_blank" style="background-color: #4078c0; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Log In to Nexus</a>
  <a href="https://proper.stsci.edu/proper/authentication/auth" target="_blank" style="background-color: #4078c0; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Sign Up for MyST</a>
  <a href="https://stsci.service-now.com/roman" target="_blank" style="background-color: #4078c0; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Get Help</a>
</div>
<!-- End buttons -->

<!--
Welcome to Roman Research Nexus

The Roman Research Nexus (RRN) is a JupyterHub instance provided by the Space Telescope Science Institute (STScI) and its main goals are to provide a higher level processing environment for Roman science data in close network proximity to cloud data storage and to increase the accessibility of Roman scientific data and software. STScI's JupyterHub platforms achieve this by providing users with a pre-defined Linux computing environment hosted by AWS.

Getting Started with RRN
To use the Research Nexus, you need a MyST account. If you do not have a MyST account, go to the MyST account page, click on Create to request an account. Once you have your account, click the Launch button in the Registered Users panel to set properties and preferences for your account. You will then be able to “Sign in with MyST” below.

Additional information
Compute power is limited but comparable to a modern laptop. Four cores are available to enable multi-processing.
Data on RRN is saved to AWS and backed up by STScI every two weeks. Even so, you should periodically back up any essential files.
RRN is continually maintained and updated: there may be regular changes and downtime.
Your data is private and will not be shared with other scientists. However, storage and compute usage are monitored. Using RRNfor nefarious purposes will result in your access being restricted so that we can provide an acceptable level of service to all users.
At this time, we cannot guarantee prompt responses to any support requests.
-->

## Creating Nexus accounts

Creating a MyST account is required to log in to the Nexus. Click the “Sign Up for MyST” button above to navigate to the sign-up page.

## How to access the Nexus

1. Go to the Nexus login page (see the “Log In to Nexus” button at the top of the page).

2. Sign in with your MyST account.

3. Launch a server.  <br>
    - Choose from the dropdown list:
    <div style="margin-left: 2em;">
      <table>
        <thead>
          <tr>
            <th>Server Type</th>
            <th style="text-align: center;">vCPU</th>
            <th style="text-align: center;">RAM</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Small </td>
            <td style="text-align: center;">2</td>
            <td style="text-align: center;">16 GB</td>
          </tr>
          <tr>
            <td>Medium </td>
            <td style="text-align: center;">8</td>
            <td style="text-align: center;">16 GB</td>
          </tr>
          <tr>
            <td>Large - CPU optimized </td>
            <td style="text-align: center;">32</td>
            <td style="text-align: center;">64 GB</td>
          </tr>
          <tr>
            <td>Large - Memory optimized </td>
            <td style="text-align: center;">16</td>
            <td style="text-align: center;">128 GB</td>
          </tr>
        </tbody>
      </table>
    </div>
    
    - Choose an image: e.g., `RGES PIT Nexus`.

That’s all. You might have to wait a few minutes for the server to start. When it does, an instance of JupyterLab will automatically launch in your browser.

> If you use the `RGES PIT Nexus` image it will launch the RGES-PIT specific welcome page on start up and preload packages we think you will need to complete the challenge. 

<!--
Welcome to the Roman Research Nexus

The Roman Research Nexus (RRN) is a JupyterHub service provided by the Space Telescope Science Institute (STScI). Its primary goals are to:

Facilitate a stable computing environment with direct access to Roman Space Telescope data
Enable collaboration between both individuals and research teams to maximize the scientific discovery potential of the Roman mission.
STScI's JupyterHub platforms achieve these goals by providing users with a pre-defined Linux computing environment, hosted in the same datacenter that houses the mission data.

Getting Started with RRN
To use the Research Nexus, you need a MyST account. If you do not have a MyST account, go to the MyST account page, click on Create to request an account. Once you have your account, click the Launch button in the Registered Users panel to set properties and preferences for your account. You will then be able to "Sign in with MyST" below.

For Faster Start-up Time
The small server option is staged with the latest image resulting in faster start-up times. It is recommended that first time users and those without high performance computing needs select this default option. Other server options will provide greater computing resources with a slower start-up times.

Personal Server (Credits used: 0.05)
Servers

Images

rges-pit
Servers

Images

Additional Information
This site is currently under development and as such, you should have no expectations regarding service uptime, data preservation, etc. We anticipate greater reliability as we approach a wider community release. At this time, no data you upload or create within RRN is guaranteed to remain for any duration. Your usage of the Nexus is monitored, so that we can improve the functionality and reliability of this service.

If you encounter difficulties or questions while using the Nexus, please contact the STScI help desk. As this platform is still in active development, we cannot guarantee prompt resolutions to any support requests.
-->
  
## Named servers

You might decide to open more than one server at a time or simply create a more organized setup. Create multiple or named servers by clicking `Home` on the top navigation bar instead of launching a server immediately when you log in. <!-- Does this save the details of your server? -->

Type in a name for your new server (e.g. "test-server") and select the smaller blue button `Add new server`.

That's it. You should be greeted with a "Welcome to the Roman Research Nexus!" page in a JupyterLab instance.

## Stopping a server

The virtual server that runs your personal instance of the Nexus will shut down after approximately an hour of inactivity. You can restart this virtual server the next time you access the Nexus.

You can stop a server instance using the `Hub Control Panel`, which is accessed from the JupyterLab UI by clicking `File -> Hub Control Panel`.

## Teams

Teams on the Nexus have shared storage and token allocations, and can work together on collaborative servers.

### Creating teams 

To create a team, put in a request with the [Nexus helpdesk](https://stsci.service-now.com/roman).

### Shared files

Team storage can be accessed through `~/teams/<your team name>/` (see [`teams.md`](../../roman_notebooks/markdown/teams.md); [external link](https://github.com/spacetelescope/roman_notebooks/blob/main/markdown/teams.md)).

## Environments

There is robust documentation on creating environments on the Nexus, in [`software.md`](../..//roman_notebooks/markdown/software.md) ([external link](https://github.com/spacetelescope/roman_notebooks/blob/main/markdown/software.md)), which you can reach by clicking the "Installing extra software" link on the welcome page.

**TL;DR**
Environments are created, listed, activated, exported, and removed using:

```bash
# Create
kernel-create <environment-name> [<python-version>] [<lab-display-name>]

# List
kernel-list

# Activate
source kernel-activate <environment-name>

# Export
kernel-export <environment-name> <output-file-name.yaml>

# Remove
kernel-delete <environment-name>
```

These environments persist between sessions, whereas a conda/mamba environment may not. Alternatively, <python-version> may be replaced with a path to a YAML file, for conda-like environment creation. Using the provided YAML for this workshop, you can create a kernel with all the packages you need for running workshop notebook content:

```bash
kernel-create rges-pit-dc env.yml "rges-pit-dc"  # This may take a while to solve the environment and download and install the packages. We will have an image available in the future to avoid this tedious process.
```

You can download the YAML [here](https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/refs/heads/main/env.yml) or clone the [data-challenge-notebooks](https://github.com/rges-pit/data-challenge-notebooks.git) repo, which includes the YAML and all the RGES-PIT-provided assistive notebooks to help you with this challenge:

```bash
cd ~ # changes made in the landing directory on the Nexus do not persist between updates
git clone https://github.com/rges-pit/data-challenge-notebooks.git
cd data-challenge-notebooks
kernel-create rges-pit-dc env.yml "rges-pit-dc"
```

For further instructions on Nexus setup and usage, see this [STScI page](https://roman-docs.stsci.edu/data-handbook/roman-research-nexus) or any of the helpful documentation pages in the landing directory on the Nexus. This content can also be found in the [`roman_notebooks` repo](https://github.com/spacetelescope/roman_notebooks) when you are not on the Nexus.


## Microlensing Data Challenge Tools

The **RGES-PIT Microlensing Data Challenge** uses the `microlens-submit` toolkit—a stateful submission tool that provides a version-controlled workflow for managing, validating, and packaging your challenge submissions.

The official challenge repositories and documentation are hosted at:

**Notebook and Informational Repository:** https://github.com/rges-pit/data-challenge-notebooks

*Duplicates of most of these notebooks exist pre-loaded on the Nexus.*

**Submission Tool Repository:** https://github.com/rges-pit/microlens-submit

**Submission Documentation and Guides:** https://microlens-submit.readthedocs.io/en/latest/


### Data Challenge Submissions

The `microlens-submit` documentation includes detailed specifications for how to create a submission. **Strict adherence to the submission criteria is required**, as much of the evaluation process is automated.

A comprehensive tutorial notebook is available here and in the `microlens-submit` repository:
- **Tutorial:** https://microlens-submit.readthedocs.io/en/latest/cli_tutorial.html
- **Python API Documentation:** https://microlens-submit.readthedocs.io/en/latest/api.html
- **Usage Examples:** https://microlens-submit.readthedocs.io/en/latest/usage_examples.html
- **Manual Submission Format:** https://microlens-submit.readthedocs.io/en/latest/submission_manual.html

## Nexus notebook content

The Nexus JupyterLab session comes preloaded with useful pages and notebooks. These live inside the `reference/` directory. [`tutorials.md`](../../roman_notebooks/markdown/tutorials.md) ([external link](https://github.com/spacetelescope/roman_notebooks/blob/main/markdown/tutorials.md)) lists all the reference notebooks and links to access them.

| Note: |
| :- |
| The notebooks in this directory are read-only, but the file system itself is not, so the reference notebooks can execute. You should not create or save notebooks in this directory. It is regularly replaced with the contents of its source repository, and any changes you make here will be lost. |

In the notebook directory you will find the aforementioned notebooks and additional environment files ([`env.yaml`](https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/refs/heads/main/env.yml) and [`requirements.txt`](https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/refs/heads/main/requirements.txt)). Included in these environment files are the dependencies for the notebooks and packages we anticipate you may need for the data challenge.

### Using the Environment Files

You should not need to use the provided environment file; you only need to select the appropriate kernel in the Nexus-hosted notebook (`RGES PIT Nexus`). If you wish to use these files anyway, refer to this README: [`AAS Workshop/README.md`](https://github.com/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/README.md).

# Nexus Specific Notebooks

Included here is a series of notebook meant to assist you in your data challenge journey. Relevant notebooks are:

  * Data challenge workflow and creating data challenge submissions [(`~/reference/content/notebooks/rmdc2025_workflow.ipynb`)](../notebooks/a_rmdc26_workflow.ipynb).

    <!-- start buttons -->
    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      
      <!-- View on GitHub button -->
      <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/Session%20A:%20Nexus/Nexus_Workflow.ipynb" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
      </svg>
      View on GitHub
      </a>
      
      <!-- Start Download Button -->
      <a href="https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/main/AAS%20Workshop/Session%20A:%20Nexus/Nexus_Workflow.ipynb" target="_blank" download="nexus_microlensing_data_challenge_workflow.ipynb" style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
      <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
      </svg>
      Download
      </a>
      <!-- End Download Button -->

      <!-- Open on RGES-PIT Website -->
      <a href="{{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/workflow/" style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      RGES-PIT.org
      </a>
    </div>
    <!-- end buttons -->

  * Alternate workflow with the submission command line tool, for non-Python users. [(`~/references/nexus-notebooks/notebooks/x_microlens-submit_cli_tutorial.ipynb`)](`../notebooks/x_microlens-submit_CLI_tutorial.ipynb`)

    <!-- start buttons -->
    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      <a href="https://microlens-submit.readthedocs.io/en/latest/tutorial.html" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" viewBox="0 0 16 16" fill="currentColor" aria-hidden="true">
      <rect x="1" y="2" width="6" height="12" rx="1"></rect>
      <rect x="9" y="2" width="6" height="12" rx="1"></rect>
      <path d="M8 3v10" stroke="currentColor" stroke-width="1" fill="none"></path>
      </svg>
      View on RtD
      </a>

      <a href="https://microlens-submit.readthedocs.io/en/latest/" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" viewBox="0 0 16 16" fill="currentColor" aria-hidden="true">
      <rect x="1" y="2" width="6" height="12" rx="1"></rect>
      <rect x="9" y="2" width="6" height="12" rx="1"></rect>
      <path d="M8 3v10" stroke="currentColor" stroke-width="1" fill="none"></path>
      </svg>
      View Docs
      </a>

      <!-- Open on RGES-PIT Website -->
      <a href="{{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/submission-tutorial/" style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      RGES-PIT.org
      </a>
    </div>
  
  * Single lens fitting & pipelined full-season demonstration [(`~/references/nexus-notebooks/notebooks/b_single_lens.ipynb`)](../notebooks/b_single_lens.ipynb)

    <!-- start buttons -->
    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      
      <!-- View on GitHub button -->
      <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/Session%20B:%20Single%20Lens%20%26%20Pipelines/Single_Lens_Pipeline.ipynb" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
      </svg>
      View on GitHub
      </a>
      
      <!-- Start Download Button -->
      <a href="https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/main/AAS%20Workshop/Session%20B:%20Single%20Lens%20%26%20Pipelines/Single_Lens_Pipeline.ipynb" target="_blank" download="single_lens_pipeline.ipynb" style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
      <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
      </svg>
      Download
      </a>
      <!-- End Download Button -->

      <!-- Open on RGES-PIT Website -->
      <a href="{{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/pipeline/" style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      RGES-PIT.org
      </a>
    </div>

    <a href="https://colab.research.google.com/github/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/Session%20B:%20Single%20Lens%20%26%20Pipelines/Single_Lens_Pipeline.ipynb" target="_blank" rel="noopener"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
    <!-- end buttons -->

  * Binary lens fitting approaches [(`~/references/nexus-notebooks/notebooks/c_binary_lens.ipynb`)](../notebooks/c_binary_lens.ipynb)

    <!-- start buttons -->
    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      
      <!-- View on GitHub button -->
      <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/Session%20C:%20Binary%20Lens/Fitting_Binary_Lenses.ipynb" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
      </svg>
      View on GitHub
      </a>
      
      <!-- Start Download Button -->
      <a href="https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/main/AAS%20Workshop/Session%20C:%20Binary%20Lens/Fitting_Binary_Lenses.ipynb" target="_blank" download="binary_lens_fitting.ipynb" style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
      <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
      </svg>
      Download
      </a>
      <!-- End Download Button -->

      <!-- Open on RGES-PIT Website -->
      <a href="{{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/binary/" style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      RGES-PIT.org
      </a>
    </div>

    <a href="https://colab.research.google.com/github/rges-pit/data-challenge-notebooks/blob/main/AAS%20Workshop/Session%20C:%20Binary%20Lens/Fitting_Binary_Lenses.ipynb" target="_blank" rel="noopener"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
    <!-- end buttons -->

  * Microlensing open-source tool demonstrations [(`~/references/nexus-notebooks/notebooks/x_microlensing_tools.ipynb`)](../notebooks/x_microlensing_tools.ipynb)

    <!-- start buttons -->
    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      
      <!-- View on GitHub button -->
      <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/Extras/Microlensing_Tools.ipynb" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
      </svg>
      View on GitHub
      </a>
      
      <!-- Start Download Button -->
      <a href="https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/main/Extras/Microlensing_Tools.ipynb" target="_blank" download="microlensing_tools.ipynb" style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
      <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
      </svg>
      Download
      </a>
      <!-- End Download Button -->

      <!-- Open on RGES-PIT Website -->
      <a href="{{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/microlensing_tools/" style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      RGES-PIT.org
      </a>
    </div>

    <a href="https://colab.research.google.com/github/rges-pit/data-challenge-notebooks/blob/main/Extras/Microlensing_Tools.ipynb" target="_blank" rel="noopener"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab"/></a>
    <!-- end buttons -->

    <div>
      </a>
      <!-- Open on RGES-PIT Website -->
      <a href="{{ site.url }}{{ site.baseurl }}/tools/" style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      Find More Tools...
      </a>
    </div>

<!-- Removing this until I know if we need s3fs
  * Accessing data using `s3fs` [(`reference/content/notebooks/data_discovery_and_access/data_discovery_and_access.ipynb`)](references/roman_notebooks/notebooks/data_discovery_and_access/data_discovery_and_access.ipynb). 

    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      
      <a href="https://github.com/rges-pit/roman_notebooks/blob/main/content/notebooks/data_discovery_and_access/data_discovery_and_access.ipynb" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
      </svg>
      View on GitHub
      </a>
      
      <a href="https://s3fs.readthedocs.io/en/latest/api.html#" target="_blank" style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" viewBox="0 0 16 16" fill="currentColor" aria-hidden="true">
      <rect x="1" y="2" width="6" height="12" rx="1"></rect>
      <rect x="9" y="2" width="6" height="12" rx="1"></rect>
      <path d="M8 3v10" stroke="currentColor" stroke-width="1" fill="none"></path>
      </svg>
      View Docs
      </a>

      <a href="javascript:void(0)" onclick="downloadNotebook('https://raw.githubusercontent.com/rges-pit/roman_notebooks/main/content/notebooks/data_discovery_and_access/data_discovery_and_access.ipynb', 'data_discovery_and_access.ipynb'); return false;" style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
      <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
      </svg>
      Download
      </a>
    </div>
end buttons -->

## Using the Nexus with local tools

### VS Code (or Cursor)

Here's a step-by-step guide to using the Nexus with VS Code, through Jupyter notebooks.

1.  **Log in to the Nexus**  
    See above.

2.  **Create a named server (trust me — it’s easier)**  
    See above.

3.  **Open the terminal and Create an Environment**  
    See above; `kernel-create <environment-name> [<python-version>] [<lab-display-name>]`. You can skip this step on the `RGES PIT Nexus` image as the `rges-pit-dc` kernel already exists.

4.  **Reopen the Hub Control Panel**  
    See above.

5.  **Get your secret token:**
    * Click on `Token`, which is in the navigation bar at the top of the page.
    * Fill out the form:
      - Note: Give it a name that reminds you what it’s for.
      - Expiry: Shorter is more secure, but requires more maintenance.
      - Permissions: leave blank (full permissions) or specify a subset — your choice.
    * `Request a new API token`. 
    * **Copy the token.** Treat it like a password.

6.  **Build the URL:**
    * Take your server's base URL (like `https://roman.science.stsci.edu`).
    * Add your specific server path (like `/user/<user-name>/<server-name>/`). This is where having a sensibly named server is helpful. You can find this on the Token page in the `Hub Control Panel`, under “Authorized Applications” → “Application” → “Server at <your-server-path>”.
    * Tack on `?token=` and then paste your secret token at the end. 

    **TL;DR**  
    `server-URL`: `https://roman.science.stsci.edu/user/<user-name>/<server-name>/?token=<token>`

7.  **Connect VS Code to the kernel:**
    * Ensure you have the Jupyter extension pack (by Microsoft) installed.
    * In VS Code, with a notebook open, click `Select Kernel` or the current kernel name (if one is already selected). Then choose:
      - "Select Another Kernel..."
      - "Existing Jupyter Server..."
      - "Enter the URL of the running Jupyter Server..."
      - Paste your `server-URL` into the box and hit `Enter`.
      - Select your created kernel/environment.
        If your kernel doesn't show up, it is likely due to a missing IPython. Run `pip install ipython` in a terminal on the Nexus (with your environment activated) and try again.

| Note: |
| :- |
| If you are using AI agents in your workflow, ensure you have selected one with notebook editing capabilities. E.g. Claude Sonnet with GitHub Copilot. |

<!-- This is currently not working

### Colab

Requires set-up from hub end:

```python
# jupyterhub_config.py or a related config file
        c.JupyterHub.tornado_settings = {
            'headers': {
                'Access-Control-Allow-Origin': 'https://colab.research.google.com',
                'Access-Control-Allow-Credentials': 'true',
            }
        }
```

```bash
jupyter notebook \
    --NotebookApp.allow_origin='https://colab.research.google.com' \
    --port=8888 \
    --NotebookApp.port_retries=0 \
    --NotebookApp.allow_credentials=True
    --no-browser
```

Here's the step-by-step guide to using the Nexus with Colab.

1.  **Follow steps 1-4 in the VSCode instructions**

2.  **Create a Local `ssh` Tunnel**
    In terminal on your local machine:
    ```bash
    sh -N -L localhost:8888:localhost:8888 <user-name>@roman.science.stsci.edu
    ```
    This will occupy your terminal.

3.  **Connect colab to a local Runtime**

    Click on the "Connect" button in the top right corner on an open Colab instance, then select "Connect to a local runtime."

    In the dialog box, enter the URL for your remote JupyterHub instance, referencing the local port you forwarded in the SSH tunnel and including the API token.

    URL: http://localhost:8888/user/<user-name>/<server-name>/?token=<token>

-->

## FAQ

> **How do I use the terminal?**
>
> Use "+" button on the far right of the document tabs, then select `terminal`, which is sorted under "Other".

> **How do I select an environment?**
>
> In a notebook session, click the `select kernel` text at the top right of the embedded window (between the hamburger and the bug). If an environment or kernel has already been selected, it might say something like `Python 3 (ipykernel)`. Simply click that kernel name to change to a new kernel.

> **How do I open the Hub Control Panel from inside the JupyterLab instance?**
>
> Click `File -> Hub Control Panel` 

<!-- END WEB CONTENT -->
<!-- COPY TO: "bin/data_challenge_nexus_help.md" -->
