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
https://drive.google.com/file/d/1njspMHlEnXggk2v2KTgSDq-rfx69BUrk/view?usp=sharing
https://drive.google.com/file/d/10Q6x7aPXvmTuIDewzN7si9qG9OcHc5QK/view?usp=sharing
https://drive.google.com/file/d/1BKrb0AHt5DAJ0OFKWTTuSdyme0rJ97uq/view?usp=sharing
https://drive.google.com/file/d/136j4KWCWCTfY9oKur1mMRtzaMfT8utOD/view?usp=sharing
---

## 🔹 Step 3: Alignment
**Tool:** bwameth  

- Reference genome: hg38  
- Paired-end reads  

### 📷 Output
https://drive.google.com/file/d/1dON1D7i28jEa2doJUu2bvoeD6sUu5zQI/view?usp=sharing
---

## 🔹 Step 4: Methylation Bias
**Tool:** MethylDackel (mbias)  

### Output
https://drive.google.com/file/d/1OxTFaRnvaca4MV_q77L-MJrC6G9n3G3h/view?usp=sharing
https://drive.google.com/file/d/1y9L0dRUOsBwGHIpJ7x1C5H-GZgpid1Eo/view?usp=sharing
https://drive.google.com/file/d/1LwczTRnv14fwElKNR371twFybkQysHr_/view?usp=sharing
https://drive.google.com/file/d/1Jjwi-jpV1apr8fvRwAi2PatYq9lClY2v/view?usp=sharing
---

## 🔹 Step 5: Methylation Extraction
**Tool:** MethylDackel (extract)  

- Generated CpG methylation BedGraph  

### 📷 Output
https://drive.google.com/file/d/1wX5z_k4VECQpDgCt5kQBwXGXkqrw-ssa/view?usp=sharing

---

## 🔹 Step 6: Visualization
**Tools:** computeMatrix, plotProfile  

- Visualized methylation around TSS  

### 📷 Output
https://drive.google.com/file/d/1n78gU4H4D94F4MiCGZje_6gXG7840GZ7/view?usp=sharing
https://drive.google.com/file/d/1aJ9VMqZTazST47kCDCkucyX5HGPUbHup/view?usp=sharing
---

## 🔹 Step 7: Differential Methylation Analysis
**Tool:** Metilene  

- Compared normal vs tumor samples  

### 📷 Output
https://drive.google.com/file/d/1rsh7MEc_0S6nv3sIzYwIInYh5cTD1IGh/view?usp=sharing
https://drive.google.com/file/d/1scpcbIDMq0OniJtmDtVpr1l-_l40AiN6/view?usp=sharing
https://drive.google.com/file/d/1WatfbJfhNVEgEo3AHFn68GOQtuMZ90BZ/view?usp=sharing

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
https://drive.google.com/file/d/1flknPpJeA-6NvddhuxFqsVVOBqplkGDV/view?usp=sharing
https://drive.google.com/file/d/1w_mpz5VM4co60lQCRzdGJNsV5e3tPWr4/view?usp=sharing
---

### 🔥 Age Deviation Heatmap
https://drive.google.com/file/d/18QplfDS_bciUDlsGl6gLO7Ke2IsJeaKk/view?usp=sharing
https://drive.google.com/file/d/19Y_GHa6MbqYxEW98KDp3k-_2KpjZEP7H/view?usp=sharing
---

### 📈 Predicted vs Chronological Age
https://drive.google.com/file/d/1gGPptvIvU3rEy3wZUbr6w4O-nEJks3Gc/view?usp=sharing
https://drive.google.com/file/d/1D4Ayh2e8RLELQ24Jeyf0h46yWpOj6Hau/view?usp=sharing
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

