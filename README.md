# Compressed Sensing in nano-FTIR Spectroscopy of SiC Microchips

This repository presents selected analysis workflows developed during my Bachelor's thesis at the Physikalisch-Technische Bundesanstalt (PTB) and Freie Universität Berlin.  
The research focuses on applying **compressed sensing** techniques in **nano-FTIR spectroscopy** of **SiC microchip structures**, utilizing synchrotron-based infrared radiation (BESSY II) to enhance spatial and spectral resolution.

---

## 📚 Project Overview

The goal was to investigate how **random and structured subsampling** of interferometric measurement points affects the quality of reconstructed nano-FTIR spectra. The objective was to **reduce measurement time** while preserving **signal integrity** in reconstructed data.

Measurements were conducted under **Strahlenschutz (radiation safety)** protocols with synchrotron IR sources.

---

## 📁 Repository Structure

```bash
notebooks/
├── Random-Subsampling_20.ipynb
├── ...
├── White-Light Subsampling_45.ipynb
├── Compressed Measurements/
│   └── [Exploratory notebooks]
figures/
├── [All plots & image figures]
thesis/
└── BSc_BV.pdf
```

---

## 🧪 Signal Regions

To assess reconstruction quality, three key spatial regions were defined:
- **S1** – Broad crack
- **S2** – Narrow crack
- **Bg** – Background

This segmentation is shown in the region map below:

![Signal Region Map](Figures/regions_s_bg.png)

---

## 🎯 Objectives

- Determine the minimal number of interferometer positions needed for reliable reconstruction.
- Compare reconstruction quality across subsampling strategies.
- Quantify Signal-to-Noise Ratio (SNR) degradation in each region (S1, S2, Bg).

---

## 🔬 Visual Comparisons of Subsampling Results

### Random Subsampling (45 positions / ~11.25%)

Reconstruction of example spectra from each region using 45 randomly selected interferometer points.

- **S1 – Broad crack** (high fidelity):  
  ![S1 random 45](Figures/45randS1good.png)

- **S2 – Narrow crack** (finer detail loss):  
  ![S2 random 45](Figures/45randS2good.png)

- **Bg – Background**:  
  ![Bg random 45](Figures/45randBGgood.png)

---

## 📊 SNR Evaluation – Strategy Comparison

Boxplot showing SNR distributions across all subsampling strategies (Random, Grid, WL) and signal regions:

![SNR Sampling Boxplot](Figures/SNRSamplingvBox.png)

- **Random** retains high SNR in S1 with fewer samples.
- **S2** shows more rapid SNR degradation at low sampling densities.

---

## 🔬 Simulated Subsampling – Best vs Worst Reconstructions

The following images show simulation-based comparisons of **reconstructed vs original interferograms and spectra** for different signal regions (S1, S2, Bg).  
Each figure shows the **best reconstruction (left)** and **worst reconstruction (right)** for the given **sampling strategy**.

---

### 🔁 Random Subsampling – Signal Regions

**S1 – Broad Crack (Random Sampling)**  
![S1 Random](Figures/S1rand.png)

**S2 – Narrow Crack (Random Sampling)**  
![S2 Random](Figures/S2rand.png)

**Background (Random Sampling)**  
![BG Random](Figures/BGrand.png)

---

### 🧩 Grid Subsampling – Signal Regions

**S1 – Broad Crack (Grid Sampling)**  
![S1 Grid](Figures/S1grid.png)

**S2 – Narrow Crack (Grid Sampling)**  
![S2 Grid](Figures/S2grid.png)

**Background (Grid Sampling)**  
![BG Grid](Figures/BGgrid.png)

---

### 💡 White-Light Sampling – Signal Regions

**S1 – Broad Crack (WL Sampling)**  
![S1 WL](Figures/S1WL.png)

**S2 – Narrow Crack (WL Sampling)**  
![S2 WL](Figures/S2WL.png)

**Background (WL Sampling)**  
![BG WL](Figures/BGWL.png)

---

Each panel compares the **subsampled points** (blue), **reconstructed signal** (black line), and **original measurement** (red dashed line).  
These synthetic tests allow direct comparison of how robust each method is against information loss in different signal environments.

---

## 📈 Spatial Feature Reconstruction

### Grid Subsampling – Intensity and Peak Position Maps

![Grid Max Intensity](Figures/grid_cm_maxI.png)  
![Grid Peak Position](Figures/grid_cm_peakposition.png)

### White-Light Subsampling – Peak Position Map

![White-Light Peak Map](Figures/HSA_cm_peakposition.png) 

---

## 🌐 Full Topographic Context

The full hyperspectral topography (overview):

![Topographic Map](Figures/hyper(topo).png)

---

## 🔎 Key Findings

> "Random subsampling down to ~11–12.5% (45–50 positions) preserved key spectral features in wide crack regions (S1).  
Fine structure areas (S2) required denser sampling (>15%) to retain detail.  
Grid and white-light methods were less robust in S2 but more consistent across broader areas."

---

## 🛠 Tools Used

- Python 3.x, Jupyter Notebooks
- NumPy, SciPy, Matplotlib, Pandas
- MATLAB (auxiliary comparison), Gwyddion (preprocessing)

---

## 🧩 Getting Started

```bash
git clone https://github.com/yourusername/nanoFTIR_SiC_CompressedSampling.git
cd notebooks/
jupyter notebook Random-Subsampling_45.ipynb
```

---

## 📜 License & Citation

MIT License  
> Vinatzer, B. (2021). *Compressed Sensing in nano-FTIR Spectroscopy*. Bachelor's thesis, Humboldt-Universität zu Berlin / PTB Berlin.

---

## 🙋‍♀️ Author

**Barbara Vinatzer**  
Research Associate @ TU Dresden (SynoSys)  
[GitHub](https://github.com/Batuffola)
