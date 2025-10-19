## 🐧 Clustering Antarctic Penguin Species

![Penguins](https://github.com/allisonhorst/palmerpenguins/blob/main/man/figures/lter_penguins.png)

This repository contains my *DataCamp* project *“Clustering Antarctic Penguin Species”*. The goal is to apply unsupervised clustering techniques on penguin morphological data to uncover groups (species) from patterns in the features.

There are known to be at least three penguin species native to the region: Adélie, Chinstrap, and Gentoo. The clustering approach aims to recover these groupings from the data.  
(Source of the data: Dr. Kristen Gorman and Palmer Station, Antarctica LTER)  [1]

---

## 📄 Project Overview

Researchers collected measurements on penguins in Antarctica, but the species labels were omitted. Using the provided dataset (`penguins.csv`), the task is to:

- Explore and preprocess the data  
- Scale features appropriately  
- Use clustering (e.g. K‑Means) to partition the data into groups  
- Visualize cluster assignments and interpret the results  

The dataset includes the following variables:  
- `culmen_length_mm` — culmen length  
- `culmen_depth_mm` — culmen depth  
- `flipper_length_mm` — flipper length  
- `body_mass_g` — body mass  
- `sex` — the penguin’s sex (used as a categorical variable)

Steps taken:
1. *Load & examine data* — check for missing or strange values  
2. *Encode categorical variables* (e.g. `sex`) as one‑hot or integer dummies  
3. *Feature scaling* using `StandardScaler`  
4. *Elbow / inertia method* — try different values of *k* (number of clusters), plot inertia to select a plausible *k*  
5. *Fit K‑Means* with chosen *k*  
6. *Assign cluster labels* and inspect cluster centroids  
7. *Visualization*:
   - Scatter plot in 2D projections colored by cluster label  
   - Plot of centroids  
   - Compare cluster means across features  
8. *Interpretation & insights* — how well do the clusters align with expected species groupings?

---

## 📈 Sample Visuals & Results

*(Embed or link here to a few example plots, for instance: inertia curve, cluster scatter, centroid overlay. You can place images in `outputs/plots/` and link them.)*

- Inertia vs. *k* plot  
- Clustered scatter of first two principal components or raw features  
- Centroid markers superimposed on cluster plot  
- Table summarizing average feature values per cluster  

---

## 🏁 Key Findings & Discussion

- The *elbow plot* suggests that *k = 3* or *k = 4* may be reasonable choices  
- Clusters group observations that are similar in morphological traits (e.g., body mass, flipper length)
- Compare cluster feature means to known species traits (if species metadata is later provided)  
- Discuss where clustering may misclassify, overlap, or show ambiguous assignments  

---

## 📈 Plots

| *Elbow analysis*                                                                        | *Clusters*                                                                                 | 
| ---------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | 
| ![Elbow](https://github.com/Horlar-1st/Clustering-Antarctic-Penguin-Species/blob/main/elbow_analysis_on_number_of_clusters.png) | ![Cluster](https://github.com/Horlar-1st/Clustering-Antarctic-Penguin-Species/blob/main/plot_of_clustering.png) |
---

📁 Repository Structure

```
Clustering-Antarctic-Penguin-Species/
   ├── penguins.csv                      # Raw dataset (if licensing allows)
   ├── plots/                            # Visualizations (inertia plot, cluster scatter plots, etc.)
   ├── plots/                            # Visualizations (inertia plot, cluster scatter plots, etc.)
   |      └── elbow_analysis_on_number_of_clusters.png
   ├── notebook.ipynb                    # Jupyter notebook with analysis and visualizations
   ├── README.md                         # This overview
   └── requirements.txt                  # Python dependencies
```

---

## 🛠 How to Run / Use This Project

1. Clone this repository:  
   ```bash
   git clone https://github.com/Horlar-1st/Clustering-Antarctic-Penguin-Species.git
   cd clustering-penguins
   ```

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook notebook.ipynb
   ```

4. View or regenerate plots in the `outputs/plots/` folder  

---

## 📚 References & Acknowledgments

- Original penguin dataset and context via Dr. Kristen Gorman and the Palmer Station Antarctica LTER. [1]
- DataCamp *Clustering Antarctic Penguin Species* project prompt  
- Scikit‑learn documentation, community examples, clustering tutorials  

---

## 🙋 Author & Contact

*Shoyombo Moshood*  
- GitHub: [github.com/horlar-1st](https://github.com/horlar-1st)  
