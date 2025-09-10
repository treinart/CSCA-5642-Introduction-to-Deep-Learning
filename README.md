# CSCA 5642: Introduction to Deep Learning

This repository tracks required projects for **Weeks 3-5** of the ***University of Colorado Boulder*** course **CSCA 5642: Introduction to Deep Learning**. All projects for Weeks 3, 4, and 5 are complete.

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
    </tr>
    <tr>
      <td><code>├── 📁 Week3/</code></td>
      <td>Kaggle Competition: CNN Cancer Detection.</td>
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
      <td>Kaggle Competition: I'm Something of a Painter Myself (GANs).</td>
    </tr>
    <tr>
      <td><code>│   ├── 📁 generated_showcase/</code></td>
      <td>A hand-picked showcase of 37 final generated images.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📁 plots/</code></td>
      <td>Diagnostic plots and image previews from the notebook.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📄 Notebook & Exports</code></td>
      <td>The final <code>.ipynb</code> and <code>.html</code> files are available as assets in the GitHub Release due to their large size.</td>
    </tr>
    <tr>
      <td><code>│   └── 🖼️ kaggle_monet_scores.png</code></td>
      <td>Screenshot of final Kaggle submission scores.</td>
    </tr>
    <tr>
      <td><code>└── 📄 README.md</code></td>
      <td>This file.</td>
    </tr>
  </tbody>
</table>

**Note:** Datasets for Week 3 and Week 5 are not tracked in git due to size limits. See the Kaggle data pages linked below.
> Week 3 Data: https://www.kaggle.com/competitions/histopathologic-cancer-detection/data  
> Week 5 Data: https://www.kaggle.com/competitions/gan-getting-started/data

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

## Week 5: I'm Something of a Painter Myself (Kaggle)

**Goal:** Generate Monet-style paintings from landscape photos using a CycleGAN, aiming for a competitive MiFID score of 60 or less.

**Progression**
- **Baseline Run (15 Epochs):** An initial training run established a strong but insufficient baseline score.
  Kaggle MiFID: **69.06**.
- **Fine-Tuning & TTA (10 Epochs):** A targeted fine-tuning run with a lower learning rate, re-enabled replay buffers, and a more aggressive identity loss was performed. The final submission was generated using Test-Time Augmentation.
  Kaggle MiFID: **57.83**; public leaderboard **#11** at publish time..

[View the "I’m Something of a Painter Myself" Leaderboard (Team: Travis Reinart)](https://www.kaggle.com/competitions/gan-getting-started/leaderboard)

### Large Files
The final notebook and HTML are ~43 MB each. To keep the repo small, they are published as GitHub Release assets. The live report is also viewable on Netlify.

- **Live HTML Report (Netlify):** https://roaring-sprinkles-7dbf83.netlify.app/
- **Release Assets Page:** https://github.com/treinart/CSCA-5642-Introduction-to-Deep-Learning/releases/tag/Week5_Kaggle_Monet_Competition
- **Download Notebook (.ipynb):** https://github.com/treinart/CSCA-5642-Introduction-to-Deep-Learning/releases/download/Week5_Kaggle_Monet_Competition/Week5_Kaggle_Monet_Competition.ipynb
- **Download HTML:** https://github.com/treinart/CSCA-5642-Introduction-to-Deep-Learning/releases/download/Week5_Kaggle_Monet_Competition/Week5_Kaggle_Monet_Competition.html


---
<p align="center">
  Licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.
</p>
