# Genome Scale Metabolic Models (GSMM) 
## Construction and Analysis

A collection of Jupyter notebooks for building and analysing simplified genome-scale metabolic models (GSMMs) using Python and COBRApy.

---

## Repository Structure

```
gsmm/   
├── GSMM_Building.ipynb      # Notebook for constructing a custom GSMM
├── GSMM_Analysis.ipynb      # Notebook for analysing and simulating the GSMM
├── environment.yml          # Conda environment file (optional)
├── requirements.txt         # Python dependencies
└── README.md                # Project overview and instructions
```

## Prerequisites

* Python 3.8 or higher
* [Conda](https://docs.conda.io/) (recommended) or virtualenv

## Installation

### Using Conda (recommended)

```bash
# Create the environment from environment.yml if provided
conda env create -f environment.yml
# Otherwise, create a new environment and install requirements
conda create -n gsmm python=3.8
conda activate gsmm
pip install -r requirements.txt
```

### Using pip

```bash
python3 -m venv venv
source venv/bin/activate    # macOS/Linux
venv\Scripts\activate     # Windows
pip install -r requirements.txt
```

## Dependencies

The `requirements.txt` file should include at least:

```
cobrapy>=0.25.0
pandas
numpy
matplotlib
jupyter
```

## Usage

1. **Clone the repository**

   ```bash
   git clone https://github.com/<your-username>/gsmm.git
   cd gsmm
   ```

2. **Activate your environment**

   ```bash
   conda activate gsmm   # or source venv/bin/activate
   ```

3. **Launch Jupyter Notebook**

   ```bash
   jupyter notebook
   ```

4. **Run the notebooks**

   * **GSMM\_Building.ipynb**: Step-by-step construction of a simplified GSMM. You will:

     * Load and preprocess metabolic network data
     * Define metabolites, reactions, and stoichiometry
     * Build and export a COBRApy model object

   * **GSMM\_Analysis.ipynb**: Perform flux balance analysis and simulations to:

     * Compute growth rates under different conditions
     * Identify essential reactions and genes
     * Visualise flux distributions

## File Descriptions

* **GSMM\_Building.ipynb**:

  * Imports foundational libraries (COBRApy, pandas, numpy)
  * Demonstrates how to assemble the stoichiometric matrix
  * Defines exchange and biomass reactions
  * Saves the model in SBML and JSON formats

* **GSMM\_Analysis.ipynb**:

  * Loads the built model
  * Runs optimisation (FBA) to predict fluxes
  * Explores gene knockout simulations
  * Generates plots of flux distributions

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature`
3. Commit your changes: \`git commit -m "Add new feature"
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
