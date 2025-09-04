# CSCA 5642: Introduction to Deep Learning

This repository tracks required projects for **Weeks 3–5** of the ***University of Colorado Boulder*** course **CSCA 5642: Introduction to Deep Learning**. Weeks 3 and 4 are complete. Week 5 is a placeholder.

## Repository Structure

<table>
  <thead>
    <tr>
      <th align="left">Path</th>
      <th align="left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>CSCA-5642-Introduction-to-Deep-Learning/</code></td>
      <td>Main repository root.</td>
     <tr>
      <td><code>├── 📁 Week3/</code></td>
      <td>Kaggle Competetion: CNN Cancer Detection.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📁 plots/</code></td>
      <td>ROC/PR curves, confusion matrices, OOF diagnostics.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📁 submissions/</code></td>
      <td>Final submission CSVs.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📄 Week3_Kaggle_CNN_Cancer_Detection.ipynb</code></td>
      <td>The main Jupyter Notebook for the project.</td>
    </tr>
    <tr>
      <td><code>│   ├──  📄 (other exports)</code></td>
      <td>HTML and PDF versions of the final notebook. </td>
    </tr>
    <tr>
      <td><code>│   └── 🖼️ kaggle_submission_screenshot_combined.png</code></td>
      <td>Screenshot of final Histopathologic Cancer Detection submission scores on Kaggle.</td>
    </tr>
    <tr>
      <td><code>├── 📁 Week4/</code></td>
      <td>Kaggle Competition: NLP with Disaster Tweets.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📁 datasets/</code></td>
      <td>Contains the <code>train.csv</code>, <code>test.csv</code>, and <code>sample_submission.csv</code> files.</td>
    </tr>
        <tr>
      <td><code>│   ├── 📁 plots/</code></td>
      <td>Diagnostic plots: per-fold AUC, ROC/PR curves, probability distributions.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📁 submissions/</code></td>
      <td>Final submission CSVs.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📄 Week4_Kaggle_NLP_Disaster_Tweets.ipynb</code></td>
      <td>The main Jupyter Notebook for the project.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📄 (other exports)</code></td>
      <td>HTML and PDF versions of the final notebook. </td>
    </tr>
    <tr>
      <td><code>│   └── 🖼️ Kaggle__Submission_ALL.png</code></td>
      <td>Screenshot of final Kaggle submission scores.</td>
    </tr>
    <tr>
      <td><code>├── 📁 Week5/</code></td>
      <td><i>placeholder</i></td>
    </tr>
    <tr>
      <td><code>└── 📄 README.md</code></td>
      <td>This file.</td>
    </tr>
  </tbody>
</table>

> **Note:** Datasets for Week 3 are not tracked in git due to their size. The Kaggle images exceed the size limits.
> https://www.kaggle.com/competitions/histopathologic-cancer-detection/data

## Week 3: CNN Cancer Detection (Kaggle)

**Goal:** Binary classification of histopathology patches with strong validation and reproducible training.

**Progression**
- **Section 5: Baseline** ResNet50, single fold (0/5), 224 px, 2 warm-up + 4 fine-tune.  
  Kaggle: **Private 0.9515**, **Public 0.9544**.
- **Section 6: Improved** ResNet50, 5-fold ensemble, 224px, 1 warm up + 2 fine tune.
  Kaggle: **Private 0.9628**, **Public 0.9781**.
- **Section 7: Advanced** EfficientNetV2-S, 5-fold, 320px, 2 warm up + 8 fine tune, 4-view TTA.  
  Kaggle: **Private 0.9814**, **Public 0.9776**.

## Week 4: NLP with Disaster Tweets (Kaggle)

**Goal:** Binary classification of tweet text with robust 5-fold CV to achieve a competitive F1 score of 0.84+.

**Progression**
- **Section 5: Baselines** TF-IDF with Logistic Regression and a calibrated SVM to establish a fast and strong benchmark.  
  Best Kaggle F1: **0.79834** (Logistic Regression).
- **Section 6: BiGRU + Attention** A sequence-aware model using a stacked BiGRU with GloVe 300d embeddings and an attention mechanism.  
  Kaggle F1: **0.8210**.
- **Section 7: DeBERTa Transformer** Fine-tuned a state-of-the-art `DeBERTa-v3-base` model, feeding it the tweet text combined with the keyword metadata.  
  Kaggle F1: **0.84615**.
- **Section 8: Ensemble Blend** A weighted blend of the OOF logits from all previous models.  
  Kaggle F1: **0.83941**.

---
<p align="center">
  Licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.
</p>

