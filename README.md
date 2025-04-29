# Compressed Sensing in nano-FTIR Spectroscopy of SiC Microchips

This repository documents selected analysis workflows developed during my Bachelor's thesis at the Physikalisch-Technische Bundesanstalt (PTB) and Freie Universität Berlin.  
The research focuses on applying **compressed sensing** techniques in **nano-FTIR spectroscopy** of **SiC microchip structures**, utilizing synchrotron-based infrared radiation (BESSY II) to enhance spatial and spectral resolution.

---

## 📚 Project Overview

The goal was to investigate how **random subsampling** of interferometric measurement points impacts the quality of reconstructed nano-FTIR spectra. The objective was to **optimize measurement time** while preserving **signal integrity** in reconstructed data.

Measurements were conducted under **Strahlenschutz (radiation safety)** protocols with synchrotron IR sources.

---

## 📁 Repository Structure

```bash
notebooks/
├── Random-Subsampling_20.ipynb
├── Random-Subsampling_30.ipynb
├── Random-Subsampling_40.ipynb
├── Random-Subsampling_45.ipynb
├── Random-Subsampling_50.ipynb
├── Random-Subsampling_60.ipynb
├── Random Subsampling SNR-Distribution.ipynb
├── Grid_Subsampling_45.ipynb
├── Equidistant Subsampling_45.ipynb
├── White-Light Subsampling_45.ipynb
├── Compressed Measurements/
│   └── [Exploratory notebooks: grid, random, white-light comparisons]
thesis/
└── BSc_BV.pdf
```

---

## 🎯 Objectives

- Determine the minimum number of interferometer positions necessary to achieve reliable spectral reconstructions.
- Quantify the impact of different **subsampling strategies** on spectral quality.
- Evaluate signal-to-noise ratios (SNR) in regions of interest (e.g., cracks in SiC structures).

---

## 🧪 Subsampling Strategies Evaluated

| Strategy            | Description |
|---------------------|--------------|
| **Random**           | Randomly selected interferometer points (20–60 out of 400) |
| **Grid**             | Regularly spaced points (grid sampling) |
| **Equidistant**      | Uniform sampling intervals |
| **White-Light**      | Sampling aligned with white-light fringe positions |

Each strategy was tested across multiple sampling densities, including 5%, 7.5%, 10%, 11.25%, 12.5%, and 15% of the full interferogram.

---

## 📊 Analysis Overview

Each notebook demonstrates:

- Loading and preprocessing of interferograms
- Application of compressed sensing reconstruction
- Visualization of peak maps and spectral reconstructions
- Signal-to-noise ratio (SNR) analysis across two primary feature regions (S1 and S2) and background (Bg)
- Comparative boxplots summarizing SNR behavior under different sampling densities

The notebook `Random Subsampling SNR-Distribution.ipynb` compares random sampling strategies across all tested densities.

---

## 📈 Key Findings

- **Random subsampling** down to 11–12.5% (approx. 45–50 positions) preserved major spectral features in broader cracks (S1).
- Narrow crack regions (S2) required higher sampling densities (>45 points) to maintain acceptable SNR.
- **White-light** and **grid sampling** approaches showed variable robustness depending on feature scale.

> "Compressed sampling allows acquisition time reduction of up to 90% while retaining usable spectral information for broader features. Critical fine structures require denser sampling."

Full experimental results and interpretations are detailed in [`thesis/BSc_BV.pdf`](../thesis/BSc_BV.pdf).

---

## 🛠️ Technologies Used

- Python 3.x
- Jupyter Notebooks
- NumPy, SciPy, Matplotlib, Pandas
- Gwyddion (external data pre-processing)
- MATLAB (auxiliary data verification)

---

## 🧩 Example Usage

Clone this repository and open any notebook:

```bash
git clone https://github.com/yourusername/nanoFTIR_SiC_CompressedSampling.git
cd notebooks/
jupyter notebook Random-Subsampling_45.ipynb
```

---

## 📜 License

This project is distributed under the MIT License.

> Vinatzer, B. (2021). *Compressed Sensing in nano-FTIR Spectroscopy*. Bachelor's thesis, Humboldt-Universität zu Berlin / PTB Berlin.

---

## 🙋‍♀️ Author

**Barbara Vinatzer**  
Research Associate @ TU Dresden (SynoSys)  
[GitHub](https://github.com/Batuffola)

---
