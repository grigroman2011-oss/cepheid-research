# Period-Luminosity Relation of Classical Cepheids using Gaia DR3

An open-source data science project exploring the Period-Luminosity relation (Leavitt's Law) for Classical Cepheids using astrometric data from the ESA Gaia DR3 catalog.

## 📌 About the Project
This project retrieves physical parameters of Classical Cepheids (DCEP) from the **Gaia Data Release 3 (DR3)** archive via ADQL queries, filters the data by error margins and distances, computes absolute magnitudes ($M$), and visualizes the Period-Luminosity relation.

## 🚀 Features
* Automated ADQL querying of the Gaia archive using `astroquery`.
* Data cleaning and filtering based on parallax errors and physical distance constraints.
* Calculation of absolute magnitudes ($M$) via distance moduli.
* Scientific data visualization using `matplotlib` and `pandas`.

## ⚙️ Data Filtering & Processing
To clean up noise and account for observational errors, the following filters were applied to the dataset:
* **Parallax Accuracy:** $\frac{\varpi}{\sigma_\varpi} > 5$ (to ensure reliable distance measurements).
* **Distance Limit:** $d < 5000\text{ pc}$ (to minimize errors caused by large distances and interstellar extinction effects).
* **Absolute Magnitude Range:** $-10 \le M \le 10$ (to capture the main sequence of variability while excluding extreme outliers).

## 📈 Results & Trend Analysis
Distances are calculated as $d = \frac{1000}{\varpi}$, and absolute magnitudes $M$ are derived using Gaia's $G$-band photometry. 
The linear regression fit yields the following relation:
$$\text{Trend: } M = -2.23 \cdot \log P + 0.52$$
*Note: The Y-axis is inverted following standard astronomical conventions (brighter objects with more negative magnitudes are placed at the top).*

## 🛠️ Tech Stack
* **Python 3.x**
* **Astroquery** (for accessing ESA Gaia database)
* **Pandas & NumPy** (for data manipulation and calculations)
* **Matplotlib** (for scientific plotting)

## 📊 Usage
1. Open the Jupyter Notebook / Google Colab file provided in the repository.
2. Run the ADQL query block to fetch data from the Gaia archive.
3. Execute the processing and visualization blocks to generate the Period-Luminosity scatter plot.

## 📝 Conclusion
The derived Period–Luminosity relation for our sample of Galactic Cepheids is consistent with the classical Leavitt's Law, confirming its validity in the optical band. The slope of –2.23 aligns well with established calibrations, while the colour gradient reveals a distance distribution extending up to ~5 kpc. This work demonstrates that Gaia DR3 data, when properly filtered, can serve as a powerful tool for large-scale stellar variability studies.
Beyond confirming the well-known relation, this project was my first hands-on journey into the world of astronomical data — from writing ADQL queries to visualising real stars.

## 📚 References & Data Sources
* ESA Gaia Mission and Gaia DR3: [https://www.cosmos.esa.int/gaia](https://www.cosmos.esa.int/gaia)
* Leavitt, H. S. (1908). *1770 variables in the Magellanic Clouds*. Annals of Harvard College Observatory.

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
