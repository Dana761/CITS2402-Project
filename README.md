# Housing Security in Australia and New Zealand

**CITS2402 — Introduction to Data Science, University of Western Australia**

This project compares housing security using Australia's 2021 Census and New Zealand's 2023 Census. It explores how tenure, affordability, and housing adequacy vary across household compositions and dwelling types through data preparation, exploratory analysis, and visualisation in Python.

## Research questions

1. **Housing tenure:** How do ownership and rental arrangements differ between the two countries?
2. **Income and rent:** How do household income and rent distributions compare, and what do they suggest about affordability?
3. **Housing-cost pooling:** How do household composition and group-household sizes differ, and could these patterns reflect shared housing costs?
4. **Housing adequacy:** How does estimated bedroom availability compare with household size across different household types?

## Project files

- [Jupyter notebook](CITS2402-Project-25268295-25060589-25476895.ipynb) — analysis, code, charts, interpretation, and references.
- [PDF report](CITS2402-Project-25268295-25060589-25476895.pdf) — included report for reading without running Python.
- **13 CSV datasets** — the census extracts used by the notebook, stored alongside it.

| Analysis | Australian datasets | New Zealand datasets |
| --- | --- | --- |
| Housing tenure | `G37.csv` | `Q1 Data NZ Stats.csv` |
| Income and rent | `G33.csv`, `G40.csv` | `Total Household Income and Weekly Rent NZ.csv`, `Income Dist. NZ.csv`, `Rent Dist. NZ.csv` |
| Household composition | `G35.csv` | `Q3 Data NZ Stats.csv` |
| Housing adequacy | `G29.csv`, `G35.csv`, `G41.csv`, `G42.csv` | `Q4 Data NZ Stats.csv` |

The Australian extracts come from the **Australian Bureau of Statistics 2021 Census General Community Profile DataPacks**. The New Zealand extracts come from **Stats NZ's Aotearoa Data Explorer, using the 2023 Census**. The notebook documents the table selections, filters, preparation steps, and source references.

## Run the notebook

The notebook records a Python **3.13.3** environment and uses **pandas**, **Matplotlib**, and **seaborn**. JupyterLab provides an interface for running it.

1. Clone the repository and enter its directory:

   ```bash
   git clone https://github.com/Dana761/CITS2402-Project-25268295-25060589-25476895.git
   cd CITS2402-Project-25268295-25060589-25476895
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   ```

   macOS / Linux:

   ```bash
   source .venv/bin/activate
   ```

   Windows PowerShell:

   ```powershell
   .venv\Scripts\Activate.ps1
   ```

3. Install the dependencies and start JupyterLab:

   ```bash
   python -m pip install pandas matplotlib seaborn jupyterlab
   python -m jupyterlab
   ```

4. Open `CITS2402-Project-25268295-25060589-25476895.ipynb`, select the virtual environment's Python kernel, and run the cells from top to bottom.

Keep the CSV files in the same directory as the notebook: the analysis reads them using relative paths. Package versions are not pinned, so this setup does not recreate an exact original environment.

## Interpretation and limitations

The notebook's analysis suggests stronger outright ownership and lower estimated affordability pressure in Australia, while its bedroom-availability estimates identify couples with children as a group facing space pressure in both countries.

These comparisons require care: the censuses cover different years, some income comparisons use different household populations, and grouped data require assumptions about bracket values. Australia's bedroom estimates also combine separate tables, whereas New Zealand's use a joint table. Bedroom availability relative to household size is an exploratory proxy, not a formal overcrowding measure, and shared-household patterns alone do not establish financial necessity. The notebook discusses these assumptions and sensitivity checks in detail.

## Authors

| Author | Student ID |
| --- | --- |
| Ryan Widjaya | 25268295 |
| Muhammad Navy Akbar Perdana | 25060589 |
| Christopher Hui-Jie Law | 25476895 |
