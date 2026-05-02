# 🧬 DNA Methylation Analysis & Aging Clock Evaluation

## 📌 Overview
This project performs Whole Genome Bisulfite Sequencing (WGBS) analysis using Galaxy and evaluates epigenetic aging clocks using Python (Google Colab).

The workflow includes:
- Quality control of sequencing data  
- Alignment of bisulfite-treated reads  
- Methylation extraction and visualization  
- Identification of Differentially Methylated Regions (DMRs)  
- Comparison of biological aging models across datasets  

---

# 🧪 PART 1 — WGBS Analysis (Galaxy Workflow)

## 🔹 Step 1: Data Upload
- Created a new Galaxy history  
- Imported:
  - subset_1.fastq  
  - subset_2.fastq  

---

## 🔹 Step 2: Quality Control
**Tool:** Falco  

- Checked base quality and GC distribution  
- Observed C→T bias due to bisulfite conversion  

### 📷 Output
![QC](results/galaxy_outputs/qc.png)

---

## 🔹 Step 3: Alignment
**Tool:** bwameth  

- Reference genome: hg38  
- Paired-end reads  

### 📷 Output
![Alignment](results/galaxy_outputs/alignment.png)

---

## 🔹 Step 4: Methylation Bias
**Tool:** MethylDackel (mbias)  

### 📷 Output
![Methylation Bias](results/galaxy_outputs/mbias.png)

---

## 🔹 Step 5: Methylation Extraction
**Tool:** MethylDackel (extract)  

- Generated CpG methylation BedGraph  

### 📷 Output
![Methylation Output](results/galaxy_outputs/methylation.png)

---

## 🔹 Step 6: Visualization
**Tools:** computeMatrix, plotProfile  

- Visualized methylation around TSS  

### 📷 Output
![Profile Plot](results/galaxy_outputs/profile.png)

---

## 🔹 Step 7: Differential Methylation Analysis
**Tool:** Metilene  

- Compared normal vs tumor samples  

### 📷 Output
![Metilene](results/galaxy_outputs/metilene.png)

---

## 🔑 Key Observations
- Bisulfite sequencing causes C→T conversion  
- Methylation patterns vary across samples  
- DMRs indicate disease-associated regions  

---

# ⏳ PART 2 — Aging Clock Analysis (Python / Colab)

## 🔹 Datasets
- Dataset 1: Normal aging  
- Dataset 2: Cancer-like (age acceleration)  

---

## 🔹 Aging Models (8 Clocks)
- Horvath  
- Hannum  
- PhenoAge  
- GrimAge  
- DunedinPACE  
- SkinBlood  
- PedBE  
- Lin  

---

## 🔹 Analysis

### 📊 Correlation Matrix
![Correlation 1](results/heatmaps/corr_dataset1.png)  
![Correlation 2](results/heatmaps/corr_dataset2.png)

---

### 🔥 Age Deviation Heatmap
![Deviation 1](results/heatmaps/deviation_dataset1.png)  
![Deviation 2](results/heatmaps/deviation_dataset2.png)

---

### 📈 Predicted vs Chronological Age
![Scatter 1](results/plots/scatter_dataset1.png)  
![Scatter 2](results/plots/scatter_dataset2.png)

---

## 📊 Key Results
- Strong correlation among aging clocks  
- Cancer dataset shows higher biological age  
- Some models show greater deviation  

---

# 🛠️ Tools & Technologies

## Galaxy
- Falco  
- bwameth  
- MethylDackel  
- computeMatrix / plotProfile  
- Metilene  

## Python
- pandas  
- seaborn  
- matplotlib  

---


---

# 🧠 Conclusion
This project demonstrates:
- End-to-end methylation analysis  
- Identification of epigenetic changes in disease  
- Comparison of biological aging models  

---

# 📚 Reference
Lin et al. (2015)  
Hierarchical Clustering of Breast Cancer Methylomes Revealed Differentially Methylated and Expressed Breast Cancer Genes  

---

# ✅ Status
✔ Analysis complete  
✔ Visualizations generated  
✔ Ready for submission  
