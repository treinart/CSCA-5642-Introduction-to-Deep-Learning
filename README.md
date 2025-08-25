# CSCA 5642: Introduction to Deep Learning

This repository tracks required projects for **Weeks 3–5** of the ***University of Colorado Boulder*** course **CSCA 5642: Introduction to Deep Learning**.  
Weeks 4–5 are placeholders. Week 3 is complete.

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
      <td>Main repository.</td>
    </tr>
    <tr>
      <td><code>├── 📁 Week3/</code></td>
      <td>Kaggle mini-project: CNN Cancer Detection.</td>
    </tr>
    <tr>
      <td><code>│&nbsp;&nbsp;&nbsp;├── 📁 plots/</code></td>
      <td>ROC/PR curves, confusion matrices, OOF diagnostics.</td>
    </tr>
    <tr>
      <td><code>│&nbsp;&nbsp;&nbsp;├── 📁 submissions/</code></td>
      <td>Final submission CSVs.</td>
    </tr>
    <tr>
      <td><code>│&nbsp;&nbsp;&nbsp;└── 📄 Week3_Kaggle_CNN_Cancer_Detection.ipynb</code></td>
      <td>The main Jupyter Notebook for the project.</td>
    </tr>
    <tr>
      <td><code>│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── 📄 (other exports)</code></td>
      <td>HTML and PDF versions of the final notebook. </td>
    </tr>
    <tr>
      <td><code>│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── 🖼️ kaggle_submission_screenshot_combined.png</code></td>
      <td>Screenshot of final Histopathologic Cancer Detection submission scores on Kaggle.</td>
    </tr>
    <tr>
      <td><code>├── 📁 Week4/</code></td>
      <td><i>placeholder</i></td>
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

> **Note:** Datasets are **not** tracked in git. The Kaggle images exceed the size limits.
> 
> https://www.kaggle.com/competitions/histopathologic-cancer-detection/data

## Week 3: CNN Cancer Detection (Kaggle)

**Goal:** binary classification of histopathology patches with strong validation and reproducible training.

**Progression**
- **Section 5: Baseline**  
  ResNet50, single fold (0/5), 224 px, 2 warm-up + 4 fine-tune.  
  Validation: **ROC AUC 0.9921**, **PR AUC 0.9893**.  
  Kaggle: **Private 0.9515**, **Public 0.9544**.
- **Section 6: 5-Fold ResNet50 Ensemble**  
  ResNet50 across 5 folds; out-of-fold diagnostics and ensembling.
- **Section 7: EfficientNetV2-S + TTA**  
  320 px input, label smoothing, 5-fold training, test-time augmentation with logit averaging.  
  Kaggle: **Private 0.9775**.

---
<p align="center">
  Licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.
</p>
