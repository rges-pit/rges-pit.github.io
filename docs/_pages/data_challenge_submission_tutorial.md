---
permalink: /data-challenge/aas-workshop/notebooks/submission-tutorial/
title: "Submission Command Line Tool Tutorial"
sidebar:
  nav: "workshop"
---
<!-- END PREAMBLE -->

> Getting Started with [`microlens-submit`](https://microlens-submit.readthedocs.io/en/latest/tutorial.html){:target="_blank"}

This comprehensive tutorial covers everything you need to know about using the [`microlens-submit`](https://microlens-submit.readthedocs.io/en/latest/tutorial.html){:target="_blank"} toolkit for packaging your data challenge solutions, using the command line.

<div style="margin: 1em 0;">
  <iframe src="https://microlens-submit.readthedocs.io/en/latest/tutorial.html" 
          width="100%" height="800" frameborder="0" 
          style="border: 1px solid #ddd; border-radius: 4px;">
  </iframe>
</div>

<div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
  <!-- View Full Documentation button -->
  <a href="https://microlens-submit.readthedocs.io/en/latest/" target="_blank"
     style="background-color: #a859e4; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
    <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8.5 2.687c.654-.689 1.782-.886 3.112-.752 1.234.124 2.503.523 3.388.893v9.923c-.918-.35-2.107-.692-3.287-.81-1.094-.111-2.278-.039-3.213.492V2.687zM8 1.783C7.015.936 5.587.81 4.287.94c-1.514.153-3.042.672-3.994 1.105A.5.5 0 0 0 0 2.5v11a.5.5 0 0 0 .707.455c.882-.4 2.303-.881 3.68-1.02 1.409-.142 2.59.087 3.223.877a.5.5 0 0 0 .78 0c.633-.79 1.814-1.019 3.222-.877 1.378.139 2.8.62 3.681 1.02A.5.5 0 0 0 16 13.5v-11a.5.5 0 0 0-.293-.455c-.952-.433-2.48-.952-3.994-1.105C10.413.809 8.985.936 8 1.783z"/>
    </svg>
    Full Documentation
  </a>
  
  <!-- GitHub Repository button -->
  <a href="https://github.com/rges-pit/microlens-submit" target="_blank"
     style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
    <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
    </svg>
    GitHub Repository
  </a>
</div>

## Quick Installation

```bash
# PyPI
pip install microlens-submit

# Conda-Forge
conda install microlens-submit
```



## Why Use microlens-submit?

Using the [`microlens-submit`](https://microlens-submit.readthedocs.io/en/latest/tutorial.html){:target="_blank"} toolkit is strongly recommended for the data challenge because it:

- **Reduces Errors**: Automatic validation catches common mistakes
- **Saves Time**: Automated workflow eliminates manual steps  
- **Ensures Consistency**: Standardized format across all submissions
- **Provides Documentation**: Rich HTML dossiers for review
- **Supports Collaboration**: Version control friendly project structure

## Key Features

- Complete workflow from project setup to final submission
- Parameter validation for all microlensing models
- Support for 1S1L, 1S2L, 2S1L, and other model types
- Higher-order effects: parallax, finite source, limb darkening
- Rich Markdown documentation with syntax highlighting
- HTML dossiers for submission review
- GitHub integration and compute tracking

---

*The tutorial above is embedded directly from the official microlens-submit documentation to ensure you always have the most up-to-date information.*
