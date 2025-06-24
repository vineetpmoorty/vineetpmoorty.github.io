---
layout: default
permalink: /cv/
title: cv
nav: true
nav_order: 2
cv_pdf: Resume_Vineet_Punyamoorty.pdf
description: Vineet Punyamoorty's Resume
---

<div style="margin-bottom: 20px;">
  <a href="/assets/pdf/Resume_Vineet_Punyamoorty.pdf" download class="btn btn-primary">Download Resume (PDF)</a>
</div>

<canvas id="pdf-viewer" style="width: 100%; max-width: 800px;"></canvas>

<!-- PDF.js Library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>

<script>
  const url = '/assets/pdf/Resume_Vineet_Punyamoorty.pdf';
  const loadingTask = pdfjsLib.getDocument(url);

  loadingTask.promise.then(function(pdf) {
    pdf.getPage(1).then(function(page) {
      const scale = 1.5;
      const viewport = page.getViewport({ scale: scale });

      const canvas = document.getElementById('pdf-viewer');
      const context = canvas.getContext('2d');
      canvas.height = viewport.height;
      canvas.width = viewport.width;

      const renderContext = {
        canvasContext: context,
        viewport: viewport
      };
      page.render(renderContext);
    });
  });
</script>