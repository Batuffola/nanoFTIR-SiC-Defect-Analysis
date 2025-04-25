# Compressed Sensing in nano-FTIR Spectroscopy of SiC Microchips (Defect Analysis)

This repository documents a Bachelor’s thesis project on the application of compressed sensing and optimized sampling techniques in nano-FTIR spectroscopy of SiC microchip structures, conducted at the Physikalisch-Technische Bundesanstalt (PTB), Berlin.

## 🔬 Project Overview

Using synchrotron IR radiation (BESSY II), hyperspectral interferograms of microstructured SiC samples were acquired. The project investigates how various compressed sampling strategies (random, grid, equidistant, white-light) affect:

- Reconstruction accuracy
- Signal-to-noise ratio (SNR)
- Measurement time

## 📂 Contents

- `notebooks/` – All main analysis Jupyter notebooks
  - `Random-Subsampling_X.ipynb`: Subsampling + Fourier reconstruction
  - `SNR-Verteilungen.ipynb`: Comparison of SNR distributions
- `data/` – Reduced datasets and computed SNR values (NumPy arrays)
- `sampling_results/` – Foldered results by sampling strategy and parameters
- `thesis/` – Optional PDF version of the BSc thesis (if license/consent allows)

## 📈 Techniques Used

- Python (NumPy, SciPy, Matplotlib, Seaborn)
- Fourier Transform & interferogram reconstruction
- Custom SNR metrics
- Compression ratio testing and error visualization
- Radiation-safe lab measurements using s-SNOM and BESSY II beamline

## 🧠 Key Findings

- Random subsampling down to 20–30% retained spectral peak integrity for key resonance bands
- SNR begins to drop nonlinearly below ~25% sampling rate
- Compressed sensing strategies can reduce acquisition time up to 90% with acceptable reconstruction quality

## 📘 Citation

If using this work in a publication or reference, please cite:
> Vinatzer, B. (2021). *Compressed Sensing in nano-FTIR Spectroscopy*. Bachelor’s thesis, Humboldt-Universität zu Berlin / PTB Berlin.

## ⚠️ Disclaimer

This repository includes sample data only. Full experimental datasets can be shared upon request (subject to approval). Thesis document available in `/thesis/` for academic purposes.

## 📜 License

MIT License or academic use only — depending on your preference.

