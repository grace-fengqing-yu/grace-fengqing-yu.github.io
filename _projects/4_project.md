---
layout: page
title: project 4
description: another without an image
img:
importance: 3
category: fun
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/TCRP.png" title="Performance" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Evaluation of drug response prediction with paclitaxel as an example. Here TCRP is compared against other conventional ML methods on diverse datasets, from cell lines, patient-derivated xenografts models, to clinical trials. 
</div>

Cancer is difficult to treat due to its heterogeneity. Tumours are often composed of diverse
cell subpopulations which yield unique drug responses. As patient samples are often
difficult to obtain, different biological models such as cell lines, mouse
models, patient-derived xenografts (PDXs), or organoids are used to study the predictive biomarkers for drug responses. Most of current studies focus on training drug response predictors from large-scale preclinical data, and assessing the performance of the resulting predictive models using limited patient data. If the translation is successful, these predictors will hold great potential for improving the selection of anticancer therapies. However, preclinical models, do not always
faithfully recapitulate the therapy response observed in patients. 

Recently, Ma et al. (Nature Cancer 2021) have developed a method called ‘transfer of cell line response prediction’ (TCRP) to train predictors of drug response in cancer cell lines and optimize their performance in higher complex cancer model systems through few-shot learning. TCRP has been presented as a successful modelling approach in several case studies. Given the importance of this approach for assisting clinicians in their treatment decision processes, we sought to independently reproduce the authors’ findings and improve the reusability of TCRP in new case studies, including validation in clinical-trial datasets—a high bar for drug-response prediction. 

Our reproducibility results, while not reaching the same level of superiority as those of the original authors, were able to confirm the superiority of TCRP in the original clinical context. Our reusability results indicate that, in the majority of novel clinical contexts, TCRP remains the superior method for predicting response for both preclinical and clinical settings. Our results thus support the superiority of TCRP over established statistical and machine learning approaches in preclinical and clinical settings. We also developed new resources to increase the reusability of the TCRP model for future improvements and validation studies.

[Check out our paper here!](https://www.nature.com/articles/s42256-023-00688-4)