# CSCA 5642: Introduction to Deep Learning

This repository tracks required projects for **Weeks 3-6** of the ***University of Colorado Boulder*** course **CSCA 5642: Introduction to Deep Learning**. All projects for Weeks 3, 4, and 5 are complete.

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
      <td><code>├── 📁 Week6/</code></td>
      <td>Predicting Class 8 Truck Fuel Rate in ADAS Platoons with CNN→GRU</td>
    </tr>
        <tr>
      <td><code>│   ├── 📁 plots/</code></td>
      <td>Diagnostic plots and image previews from the notebook.</td>
    </tr>
        <tr>
      <td><code>│   ├── 📄 CSCA5642_Final_Project_Fuel_Rate.ipynb</code></td>
      <td>The main Jupyter Notebook for the project.</td>
    </tr>
    <tr>
      <td><code>│   ├── 📄 (other exports)</code></td>
      <td>HTML and PDF versions of the final notebook. </td>
    </tr>
        <tr>
      <td><code>└── 📄 README.md</code></td>
      <td>This file.</td>
    </tr>
  </tbody>
</table>

**Note:** Datasets for Week 3, Week 5, and Week 6 are not tracked in git due to size limits. See the pages linked below to download datasets.
* **Week 3 Data:** [Histopathologic Cancer Detection](https://www.kaggle.com/competitions/histopathologic-cancer-detection/data)
* **Week 5 Data:** [Kaggle: I’m Something of a Painter Myself](https://www.kaggle.com/competitions/gan-getting-started/data)
* **Week 6 Data:** [Energy.gov NREL: Truck Platooning Performance](https://livewire.energy.gov/ds/nrel-mdhd-cav/ds0)

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

Of course. A good `README` is crucial for telling the story of a project. I've reviewed your current structure and drafted a description for Week 6 that matches the format and style of the other sections.

This new section summarizes the goal, the progression from the baseline to the final deep learning model, and the ultimate outcome of the analysis.

---
## Week 6: Predicting Truck Fuel Rate with CNN→GRU (Final Project)
**Goal:** Predict the instantaneous fuel rate of Class 8 trucks from time-series data and use the model to quantify the fuel savings benefits of ADAS platooning.
**Progression**
- **Section 7: Classical Baseline** An XGBoost model was trained on statistical features aggregated over 10-second windows. This established a strong, non-sequential benchmark.  
  Best Validation MAE: **1.31 L/hr**.
- **Section 8: CNN→GRU Model** A hybrid deep learning model using a CNN to extract features and a GRU to model temporal dependencies was trained on the full sequence data. This model significantly outperformed the baseline.  
  Best Validation MAE: **0.95 L/hr**.
- **Section 10: Platoon Savings Analysis** The trained CNN→GRU model was used to analyze real-world platoon runs. The final analysis calculated the team-average fuel savings compared to a solo truck baseline (6.8 MPG) during highway driving (≥100 km/h).  
  Measured Savings: **8.3% (2-Truck)** and **12.2% (3-Truck)**.

### Visit the live link for [Truck Platooning: Interactive ROI Calculator](https://treinart.github.io/CSCA-5642-Introduction-to-Deep-Learning/Truck_Platooning_ROI_Calculator_v9.html).

---
<p align="center">
  Licensed under the <a href="https://opensource.org/licenses/MIT">MIT License</a>.
</p>
