---
permalink: /data-challenge/aas-workshop/1-nexus/
title: "Introduction to the Roman Research Nexus (The Nexus)"
sidebar:
  nav: "workshop"
---

<!-- Login, sign up, and help buttons -->
<div style="text-align: center; margin: 2em 0; display: flex; justify-content: center; gap: 1em; flex-wrap: wrap;">
  <a href="https://roman.science.stsci.edu/hub/" style="background-color: #4078c0; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Log In to Nexus</a>
  <a href="https://proper.stsci.edu/proper/authentication/auth" style="background-color: #4078c0; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Sign Up for MyST</a>
  <a href="https://stsci.service-now.com/roman" style="background-color: #4078c0; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: bold; display: inline-block; transition: background-color 0.2s;">Get Help</a>
</div>

The Roman Research Nexus (AKA Nexus), is a Jupyter Hub service with public, shared, compute resources, which is ultimately intended to be used for Roman related data analysis.

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

[Creating a MyST account](https://proper.stsci.edu/proper/authentication/auth) is *required** to log in to the Nexus. Click the `Sign Up for MyST` button above to navigate to the sign up page.

## How to access the Nexus

1. Go to the [Nexus log in page](https://roman.science.stsci.edu/hub/) (see the `Log in to Nexus` button at the top of the page).

2. Sign in with your MyST account.

3. Launch a simple server.  <br>
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
    
    - Choose an Image: e.g. `roman-17.1.1 (June 2025 patched)`.

That's all. You might have to wait a few minutes for the server to start. When it does, an instance of Jupyter lab will be automatically launched in your browser.

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
This site is currently under development and as such, you should have no expectations regarding service uptime, data preservation, etc. We anticipate greater reliability as we approach a wider community release. At this time, no data you upload or create within RRN is guaranteed to remain for any duration. Your usage of the nexus is monitored, so that we can improve the functionality and reliability of this service.

If you encounter difficulties or questions while using the nexus, please contact the STScI help desk. As this platform is still in active development, we cannot guarantee prompt resolutions to any support requests.
-->
  
## Named Server

You might decide that you would like to open more than oen server at a time or just create a more organized server set-up. You create multiple or named server by clicking `Home` on the top navigation bar instead of launching a server imediately when you log in. <!-- Does this save the details of your server? -->

Type in a name for your new server (e.g. "test-server") and select the smaller blue button `Add new server`.

That's it. You should be greated with a "Welcome to the Roman Research Nexus!" page in a JupyterLab instance.

## Stopping a server

The virtual server that runs your personal instance of the Nexus will shut down after approximately an hour of inactivity. You can restart this virtual server the next time you access the Nexus.

You can stop a server instance using the `Hub Control Pannel`, which is accesses for the JupiterLab UI by clicking `File -> Hub Control Panel`.

## Teams

### Creating Teams 

<!--Ask Nexus people about this) -->

### Shared Files

Team Storage can be access through `/teams/<your team name>/` (see `teams.md`).

## Environments

There exist robust documentation on the creation of environments on the Nexus in `software.md`, which you can get to by clicking the `Installing extra software` link on the welcome page.

**TL;DR**
Environments are created, listed, activated, exported and removed using

```
# Create
kernel-create <environment-name> [<python-version>] [<lab-display-name>]

# List
kernel-list

# Activate
source kernel-activate <environment-name>

# Export
kernel-export <environment-name> <output-file-name.yaml>

# Removed
kernel-delete <environment-name>
```

These environments persist between sessions.

## Using the Nexus with local tools

### VSCode

Here’s the step-by-step guide to using the Nexus with VSCode.

1.  **Log in to the Nexus**  
    See above.

2.  **Create a Named Server (trust me-it's just easier that way)**  
    See above.

3.  **Open the terminal and Create an Environment**  
    See above; `kernel-create <environment-name> [<python-version>] [<lab-display-name>]`.

4.  **Reopen the Hub Control Panel**  
    See above.

5.  **Get Your Secret Handshake (The Token):**
    * Click on `Token`, which is in the navigation bar at the top of the page.
    * Fill on the form:
      - Note: Give it a name that reminds you what it's for.
      - Expiry: Shorter is always more secure, but also more admin.
      - Permision: leave this blank (full permissions), or specifiy specific permissions; it's up to you.
    * `Request a new API token`. 
    * **Copy the token.** Treat it like your diary key.

6.  **Build the Magic URL:**
    * Take your server's base URL (like `https://roman.science.stsci.edu`).
    * Add your specific server path (like `/user/<user-name>/< server-name>/`). This is where having a sensibly named server is helpful. You can find this on the Token page in the `Hub Control Panel`, under "Authorized Applications" > "Application" > "Server at <your-server_path>
    * Tack on `?token=` and then paste your secret token at the end. 

    **TL;DR**  
    `server-URL`: `https://roman.science.stsci.edu/user/<user-name>/<server-name>/?token=<token>`

    <!-- https://roman.science.stsci.edu/user/malpas-1/instruction-test/?token=df7b23a5f66240b8b49c18289650518c -->

7.  **Connect VSCode to the Kernel:**
    * Ensure you have the Jupyter extension pack (by Microsoft) installed.
    * In VSCode, in an open notebook, click the `select kernel` or `<current-kernel-name>`, if one is already selected. Then select the following options when prompted:
      - "Select Another Kernel..."
      - "Existing Jupyter Server..."
      - "Enter the URL of the running Jupyter Server..."
      - Paste your `server-URL` into the box and hit `Enter`.
      - Select your created kernel/environment.
        If your kernel doesn't show up, it is likely because of a missing ipython. `pip install ipython` in a terminal on the Nexus's JupyterLab, with your environment activated, and try again.

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

Here’s the step-by-step guide to using the Nexus with Colab.

1.  **Follow steps 1-4 in the VSCode instructions**

2.  **Create a Local `ssh` Tunnel**
    In terminal on your local machine:
    ```bash
    sh -N -L localhost:8888:localhost:8888 <user-name>@roman.science.stsci.edu
    ```
    This will occupy your terminal.

3.  **Connect colab to a local Runtime**

    Click on the "Connect" button in the top right corner on an open colab instance, then select "Connect to a local runtime."

    In the dialog box, enter the URL for your remote JupyterHub instance, referencing the local port you forwarded in the SSH tunnel and including the API token.

    URL: http://localhost:8888/user/<user-name>/<server-name>/?token=<token>

-->

## Nexus notebook content

The Nexus JupiterLab session comes pre-load with a bunch of useful pages and notebooks This live inside the `reference/` directory. `tutorials.md` has a list of all the reference notebooks and links to access them.

| Note: |
|:- |
| The notebooks in this directory are read only but the file system itself is not, so that the reference notebooks can execute. You **should not** create and save notebooks in this directory. The directory is regularly replaced with the contents of its source repository, and any changes you make in here will be (without making someones life diffucult) lost. |

Relavent to this data challenge are 3 notebooks:
  * [Introduction to microlensing open source software]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/microlensing_tools) (`reference/content/notebooks/microlensing_tools/microlensing_tools.ipynb`).
  
    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      <!-- View on GitHub button -->
      <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/Microlensing_Analysis_Tools_colab.ipynb" 
         style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        View on GitHub
      </a>
      
      <!-- Download button with JavaScript -->
      <a href="#" 
         onclick="downloadNotebook('https://github.com/rges-pit/data-challenge-notebooks/raw/main/Microlensing_Analysis_Tools_colab.ipynb', 'Microlensing_Analysis_Tools_colab.ipynb')"
         style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
          <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
        </svg>
        Download
      </a>
    </div>

  * Accessing data using `s3fs` (`reference/content/notebooks/data_discovery_and_access/data_discovery_and_access.ipynb`).

    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      <!-- View on GitHub button -->
      <a href="https://github.com/rges-pit/roman_notebooks/blob/main/content/notebooks/data_discovery_and_access/data_discovery_and_access.ipynb" 
          style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        View on GitHub
      </a>
      
      <!-- View on Docs button -->
      <a href="https://s3fs.readthedocs.io/en/latest/api.html#" 
          style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        View Docs
      </a>
    </div>

  * [Data challenge workflow and creating data challenge submissions]({{ site.url }}{{ site.baseurl }}/data-challenge/aas-workshop/notebooks/workflow/) (`microlens-submit`) (`reference/content/notebooks/rmdc2025_workflow/rmdc2025_workflow.ipynb`).

    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      <!-- View on GitHub button -->
      <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/nexus_microlensing_data_challenge_workflow.ipynb" 
          style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        View on GitHub
      </a>
      
      <!-- Download button with JavaScript -->
      <a href="#" 
          onclick="downloadNotebook('https://github.com/rges-pit/data-challenge-notebooks/raw/main/nexus_microlensing_data_challenge_workflow.ipynb', 'nexus_microlensing_data_challenge_workflow.ipynb')"
          style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
          <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
        </svg>
        Download
      </a>
    </div>

  * Alternate workflow with the submission command line tool, for non-Python users.

    <div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
      <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/nexus_microlensing_data_challenge_workflow.ipynb" 
          style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        View on GitHub
      </a>
      <a href="https://microlens-submit.readthedocs.io/en/latest/" 
          style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
          <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.20-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
        </svg>
        View Docs
      </a>
    </div>

<script>
function downloadNotebook(url, filename) {
  fetch(url)
    .then(response => response.blob())
    .then(blob => {
      const link = document.createElement('a');
      link.href = URL.createObjectURL(blob);
      link.download = filename;
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    });
}
</script>

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