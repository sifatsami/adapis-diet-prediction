# Predicting the Diet of Extinct Genus *Adapis* using LDA

## Overview
This project investigates the dietary classification of the extinct primate genus *Adapis* using **Linear Discriminant Analysis (LDA)**.  
By analyzing molar geometric features such as Dirichlet Normal Energy (DNE) and surface area measurements, the model predicts dietary categories including Folivore, Frugivore, Insectivore, and Omnivore.  

The study also explores whether **Frugivore–Folivore** diets are statistically distinguishable from **Folivore** diets, using statistical tests and feature comparison plots.

---

## Dataset
The dataset includes 116 primate molar samples across multiple genera with the following key features:

- `DNE`: Dirichlet Normal Energy  
- `positive_DNE`: Positive component of DNE  
- `surface_area`: Total molar surface area  
- `positive_surface_area`: Positive surface area component  
- `Diet`: Labeled dietary class (some missing values)  
- `Genus`: Genus name of the primate specimen  

---

## Methodology

1. **Data Cleaning:** Missing dietary labels were identified and filtered.  
2. **Feature Comparison:**  
   A comparison was made between *Folivore* and *Frugivore–Folivore* diets to test for statistical differences across the four features.

   **Feature Comparison: Folivore vs Frugivore–Folivore**  
   ![Feature Comparison Plot](https://github.com/sifatsami/adapis-diet-prediction/blob/main/Folivore%20vs%20Frugivore%E2%88%92Folivore.png?raw=true)

   T-tests showed no significant difference (*p* > 0.05), leading to the merging of these two diet categories.  
3. **Model Training:**  
   LDA was applied using four geometric features as predictors.  
4. **Model Evaluation:**  
   The model achieved **70.27% accuracy** on the training dataset.  
5. **Prediction for *Adapis*:**  
   The trained LDA model classified all *Adapis* samples as **Omnivores**, suggesting a generalized diet.

---

## Results Summary
| Step | Description | Key Finding |
|------|--------------|--------------|
| Feature comparison | Folivore vs Frugivore–Folivore | No significant difference |
| Model accuracy | LDA classifier | 70.27% |
| *Adapis* prediction | Based on molar geometry | All predicted as Omnivore |

---

## Tools & Libraries
- **Language:** R  
- **Libraries:** `tidyverse`, `MASS`, `ggplot2`, `dplyr`
