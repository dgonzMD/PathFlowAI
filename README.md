<h1 align="center">Welcome to PathFlowAI 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.1-blue.svg?cacheSeconds=2592000" />
  <a href="https://jlevy44.github.io/PathFlowAI/">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" target="_blank" />
  </a>
</p>

> A Convenient High-Throughput Workflow for Preprocessing, Deep Learning Analytics and Interpretation in Digital Pathology

### 🏠 [Homepage](https://github.com/jlevy44/PathFlowAI)

MedRxiv Manuscript: https://www.medrxiv.org/content/10.1101/19003897v1

Note: Wiki and installation tips are currently being worked on! Please submit issues in the meanwhile.

## Install

First, install [openslide](https://openslide.org/download/).

```sh
pip install pathflowai
```

## Usage

```sh
pathflowai-preprocess -h
pathflowai-train_model -h
pathflowai-monitor -h
pathflowai-visualize -h
```

See [Wiki](https://github.com/jlevy44/PathFlowAI/wiki) for more information on setting up and running the workflow.

## Author

👤 **Joshua Levy**

* Github: [@jlevy44](https://github.com/jlevy44)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/jlevy44/PathFlowAI/issues).

**Figures from the Paper**

![1](https://user-images.githubusercontent.com/19698023/62230963-0199d780-b391-11e9-96eb-ac9b86686723.jpeg)
<p style="text-align: center;">Fig. 1. PathFlowAI Framework: a) Annotations and whole slide images are preprocessed in parallel using
Dask; b) Deep learning prediction model is trained on the model; c) Results are visualized; d) UMAP
embeddings provide diagnostics; e) SHAP framework is used to find important regions for the prediction</p>

![2](https://user-images.githubusercontent.com/19698023/62231545-41ad8a00-b392-11e9-8d47-f9f83f4b764a.jpeg)
<p style="text-align: center;>Fig. 2. Comparison of PathFlowAI to Preprocessing WSI in Series for: a) Preprocessing time, b) Storage
Space, c) Impact on the filesystem. The PathFlowAI method of parallel processing followed by
centralized storage saves both time and storage space</p>

![3](https://user-images.githubusercontent.com/19698023/62231546-41ad8a00-b392-11e9-9b16-ea3b2b92bf3f.jpeg)
<p style="text-align: center; ">Fig. 3. Segmentation: Original (a) Annotations Compared to Predicted (b) Annotations; (c) Pathologist
annotations guided by the classification model</p>

![4](https://user-images.githubusercontent.com/19698023/62230966-02326e00-b391-11e9-989c-155ff0a9be67.jpeg)
<p style="text-align: center; ">Fig. 4. Portal Classification Results: a) Darker tiles indicate a higher assigned probability of portal classification, b)
AUC-ROC curves for the test images that estimate overall accuracy given different sensitivity cutoffs, c) H&E patch
(left) with corresponding SHAP interpretations (right) for four patches; the probability value of portal classification
is shown, and on the SHAP value scale, red indicates regions that the model attributes to portal prediction, d) Model trained UMAP embeddings of patches colored by original portal coverage (area of patch covered by portal) as judged
by pathologist and visualization of individual patches</p>
