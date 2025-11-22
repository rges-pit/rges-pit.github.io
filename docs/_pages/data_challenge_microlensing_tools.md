---
permalink: /data-challenge/aas-workshop/notebooks/microlensing_tools/
title: "Introduction to Microlensing Tools"
sidebar:
  nav: "workshop"
---
<!-- END PREAMBLE -->

<div style="margin: 1em 0;">
  <iframe src="https://nbviewer.org/github/rges-pit/data-challenge-notebooks/blob/main/Extras/Microlensing_Tools.ipynb" 
          width="100%" height="600" frameborder="0">
  </iframe>
</div>

<div style="display: flex; gap: 10px; margin: 1em 0; align-items: center;">
  <!-- View on GitHub button -->
  <a href="https://github.com/rges-pit/data-challenge-notebooks/blob/main/Extras/Microlensing_Tools.ipynb" target="_blank"
     style="background-color: #4078c0; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
    <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
    </svg>
    View on GitHub
  </a>
  
  <!-- Download button with JavaScript -->
  <a href="javascript:void(0)" 
     onclick="downloadNotebook('https://raw.githubusercontent.com/rges-pit/data-challenge-notebooks/main/Extras/Microlensing_Tools.ipynb', 'Microlensing_Tools.ipynb'); return false;"
     style="background-color: #28a745; color: white; padding: 8px 16px; text-decoration: none; border-radius: 4px; font-size: 14px; display: inline-flex; align-items: center; gap: 5px;">
    <svg width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
      <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5z"/>
      <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3z"/>
    </svg>
    Download
  </a>
</div>

<script>
function downloadNotebook(url, filename) {
  fetch(url, { mode: 'cors', redirect: 'follow' })
    .then(response => {
      if (!response.ok) throw new Error('Download failed: ' + response.status);
      return response.blob();
    })
    .then(blob => {
      const link = document.createElement('a');
      const objectUrl = URL.createObjectURL(blob);
      link.href = objectUrl;
      link.download = filename;
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
      setTimeout(() => URL.revokeObjectURL(objectUrl), 1000);
    })
    .catch(() => {
      window.open(url, '_blank', 'noopener');
    });
}
</script>
