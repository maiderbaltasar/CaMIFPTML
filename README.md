# CaM IFPTML model development

This repository contains the data, code, and results for the manuscript:  
**"A machine learning approach for predicting drug-like molecules targeting Calmodulin pathway proteins"**
> [DOI: 10.5281/zenodo.15423309](https://doi.org/10.5281/zenodo.15423309)
---

Maider Baltasar-Marchueta,1,2 Naia López,1 Sara Alicante,3 Iratxe Barbolla,1 Markel Garcia Ibarluzea,4,5 Rafael Ramis Cortés,4,5 Ane Miren Salomon,1 Arantza Muguruza-Montero,3 Eider Nuñez,3 Aritz Leonardo,4,5 Sonia Arrasate,1 Nuria Sotomayor,1 Matthew M Montemore,2 Alvaro Villarroel,*3 Aitor Bergara,*4,5 Esther Lete,*1 and Humberto González-Díaz*1,3,6

1 Department of Organic and Inorganic Chemistry, University of the Basque Country UPV/EHU, 48940, Leioa, Spain.
2 Department of Chemical and Biomolecular Engineering, Tulane University, 6823 St Charles Avenue, New Orleans, Louisiana 70118, United States.
3 Biofisika Institute, CSIC-UPV/EHU, 48940, Leioa, Spain.
4 Donostia International Physics Center, Donostia, Spain.
5 Departament of Physics and EHU Quantum Center, University of the Basque Country, UPV/EHU, Leioa, Spain.
6 IKERBASQUE, Basque Foundation for Science, 48011, Bilbao, Spain.

Keywords: Drug Discovery; Calmodulin; Chemoinformatics; Machine Learning; Molecular Synthesis; Biological Assays; Docking Studies.

Abstract. Recently, numerous models have been developed to predict drug interactions with molecules. However, integrating diverse data sources and improving the accuracy of biological activity predictions remains a challenge. This work proposes a novel solution that addresses these limitations. Here, we have developed a machine learning model to predict the efficacy of different assays and drugs for diseases related to calmodulin. To achieve this, we have compiled a comprehensive dataset including commercialized drugs and experimental compounds targeting CaM complexes. We have used the IFPTML modelling technique to identify key factors influencing these activities. We have also synthesized novel riluzole derivatives and have tested them both experimentally as well as computationally. Biological assays and molecular docking studies have been performed to provide a molecular-scale picture of the molecule-CaM interaction. Moreover, as a validation of the utility of the model in drug design, we have tested the model on these derivatives. We have found that the model correctly predicts which derivatives were most bioactive, indicating that this framework can be used to identify promising candidates for new drug formulations. This research not only advances our understanding of CaM-related diseases but also provides an effective framework for developing new treatments based on predictive modelling.

---

# 📁 Repository contents

- `Readable Data_Python.csv`: Dataset used to train and validate the machine learning models.
- `camptml.ipynb`: Jupyter notebook with the full workflow: data processing, model training (LDA, XGB), and evaluation.
- `Supporting Information II.xlsx`: Extended supplementary material.
- `train_set.csv`: Data used to train the models.
- `test_set.csv`: Independent data used to evaluate the models' predictive performance.
- PNG figures:
  - Confusion matrices:  
    `LDA_Train_Confusion_Matrix.png`, `LDA_Test_Confusion_Matrix.png`  
    `XGB_Train_Confusion_Matrix.png`, `XGB_Test_Confusion_Matrix.png`
  - Feature importance:  
    `Top_20_Feature_Importances_LDA.png`, `Top_20_Feature_Importances_XGB.png`
  - ROC curves and model comparisons:  
    `roc_curves_train_comparison.png`, `roc_curves_test_comparison.png`, `model_accuracy_comparison.png`
  - Others:  
    `heatmap_riluzole_derivatives_vs_calmodulin.png`, `correlation_matrix.png`, `success_by_assay_type.png`, `Success_Probability_Assays.png`

---

# ▶️ How to reproduce the results

1. Clone this repository:
   ```bash
   git clone https://github.com/maiderbaltasar/CaMIFPTML.git
   cd CaMIFPTML
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows use: env\Scripts\activate
   ```

3. Install dependencies (examples):
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn xgboost
   ```

4. Open and run the notebook:
   ```bash
   jupyter notebook camptml.ipynb
   ```

---

# 📌 Notes

- All data used is provided in `Readable Data_Python.csv`.
- The code and models were developed using Python and Jupyter Notebook.
- Results can be visually explored through the figures provided.

---

If you use this work, please cite the corresponding publication (when available) and/or the Zenodo archive:

> Baltasar-Marchueta M, López N, Alicante SM, Barbolla I, Garcia Ibarluzea M, Ramis Cortés R, Salomon AM, Muguruza-Montero A, Nuñez E, Leonardo A, Arrasate S, Sotomayor N, Montemore MM, Villarroel Á, Bergara A, Lete E, González-Díaz H.  
> *A machine learning approach for predicting drug-like molecules targeting Calmodulin pathway proteins.*  
> [DOI: 10.5281/zenodo.15423309](https://doi.org/10.5281/zenodo.15423309)
