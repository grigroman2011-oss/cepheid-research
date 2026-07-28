# Period-Luminosity Relation of Classical Cepheids using Gaia DR3

An open-source data science project exploring the Period-Luminosity relation (Leavitt's Law) for Classical Cepheids using astrometric data from the ESA Gaia DR3 catalog.

## 📌 About the Project
This project retrieves physical parameters of Classical Cepheids (DCEP) from the **Gaia Data Release 3 (DR3)** archive via ADQL queries, filters the data by error margins and distances, computes absolute magnitudes ($M$), and visualizes the Period-Luminosity relation.

## 🚀 Features
* Automated ADQL querying of the Gaia archive using `astroquery`.
* Data cleaning and filtering based on parallax errors and physical distance constraints.
* Calculation of absolute magnitudes ($M$) via distance moduli.
* Scientific data visualization using `matplotlib` and `pandas`.

## 🛠️ Tech Stack
* **Python 3.x**
* **Astroquery** (for accessing ESA Gaia database)
* **Pandas & NumPy** (for data manipulation and calculations)
* **Matplotlib** (for scientific plotting)

## 📊 Usage
1. Open the Jupyter Notebook / Google Colab file provided in the repository.
2. Run the ADQL query block to fetch data from the Gaia archive.
3. Execute the processing and visualization blocks to generate the Period-Luminosity scatter plot.

## 📚 References & Data Sources
* ESA Gaia Mission and Gaia DR3: [https://www.cosmos.esa.int/gaia](https://www.cosmos.esa.int/gaia)
* Leavitt, H. S. (1908). *1770 variables in the Magellanic Clouds*. Annals of Harvard College Observatory.

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
