# Code and data supporting "Linear response in generalized Lotka–Volterra systems with a finite number of species"

This repository holds the Google Colab notebooks and the exact input datasets used in our numerical experiments and EcoBase ecosystem analysis.

## Contents

- `Numerical_calculation_gLV.ipynb`: non-normal transient dynamics, numerical-range plot and random-matrix experiments. No external input data.
- `EcoBase.ipynb`: EcoBase analyses, bounds/RMT comparisons, histograms, geographic maps and network visualizations. Requires `data/df.csv` and `data/Ecopath_list.pkl`.
- `data/`: input datasets from the study.
- `requirements.txt`: dependencies.

## Run in Google Colab

1. Open either `.ipynb` notebook in Google Colab from the GitHub repository (File -> Open notebook -> GitHub), or use the badge/link on GitHub.
2. In a *new first code cell*, run the following commands, replacing placeholders with the real repository owner and name:

   ```python
   !git clone https://github.com/USER/REPOSITORY.git /content/paper-repro
   %cd /content/paper-repro
   %pip install -r requirements.txt
   ```

   If using the published version, clone its tag instead:

   ```python
   !git clone --branch v1.0.0 --depth 1 https://github.com/USER/REPOSITORY.git /content/paper-repro
   %cd /content/paper-repro
   %pip install -r requirements.txt
   ```

3. Execute the remaining cells in order, in a clean Colab runtime. Some figures may take time to generate.
4. SVG figures are written to the current working directory.

**Note:** Opening a notebook via GitHub in Colab does not automatically copy the repository's data files into the Colab runtime; hence the clone step is necessary.

## Reproducibility

- `Numerical_calculation_gLV.ipynb` sets `np.random.seed(0)` before its random-matrix sampling.
- The EcoBase notebooks expect the exact same data snapshot and row order in `df.csv` and `Ecopath_list.pkl`.
- The geographic map cell also loads a Natural Earth ZIP from `https://naciscdn.org/naturalearth/110m/cultural/ne_110m_admin_0_countries.zip`, so this part currently needs internet access.

## Citation and license

