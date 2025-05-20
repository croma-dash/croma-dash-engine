# Croma Dash Engine

*Croma Dash* (INPI BR512022000420-8) is a computational decision-support tool for the *development of chromatographic methods. Developed in Python, it enables the estimation of physicochemical parameters and the simulation of chromatographic columns under **gradient elution*, with a focus on preparative chromatography.

## 🔧 Software Modules

Croma Dash is structured into four main modules:

---

### 🧪 CromaD_BEP – Batch Equilibrium Parameters

- Estimates adsorption isotherm parameters (Langmuir and linear models with phase modifier effects) using *microplate data* (8x12 layout).
- Features:
  - Outlier detection (Z-test)
  - Parameter estimation: \( q_S \), \( b_0 \), \( S \)
  - Correlation and covariance matrix calculation
- Input: .xlsx files formatted to reflect microplate organization.

---

### 📈 CromaD_CEP – Column Experimental Processing

- Processes raw chromatographic data files (e.g., .xml from Biotage Selekt systems).
- Applies corrections (e.g., dead volume) and extracts:
  - Retention volume
  - Theoretical plate height
  - Apparent dispersion
- Outputs results as .csv or .xlsx files.

---

### 🔬 CromaD_S – Chromatographic Column Simulator

- Simulates chromatographic elution using phenomenological models:
  - EDM (Equilibrium Dispersive Model)
  - LKM (Lumped Kinetic Model)
- Supports multiple interaction models:
  - LSS (Linear Solvent Strength)
  - MPM (Modifier Phase Model)
  - SMA (Steric Mass Action)
- Allows customization of finite volume grids, numerical schemes (e.g., Koren, Superbee), and stability analysis.

---

### 📊 CromaD_E – Column Parameter Estimation

- Performs experimental data fitting using:
  - Classical Least Squares (CLS)
  - Weighted Least Squares (WLS)
- Supports joint parameter estimation by combining *batch and column data*:
  - Uses covariance matrices from CromaD_BEP
  - Reduces uncertainty and improves statistical confidence

---

## 🎯 Purpose

Croma Dash is designed to *accelerate method development, **minimize material consumption, and **increase confidence in mechanistic modeling. It enables **integration of heterogeneous experimental data* (batch and column) into a unified modeling and optimization workflow.

---

## 📄 License

This project is released under the GNU AFFERO GENERAL PUBLIC License. See the LICENSE file for details.
