# Data Science 500: Web Scraping, EDA, and Predictive Modeling Pipeline

An end-to-end data science project demonstrating web scraping, data cleaning, exploratory data analysis (EDA), and machine learning using Python. This repository contains the source code, dataset, and documentation for analyzing book details harvested from the **Books to Scrape** sandbox platform.

---

##  Project Overview

The main objective of this project is to automate the acquisition of unstructured e-commerce data, transform it into a structured tabular dataset, perform exploratory statistical visual analysis, and evaluate a predictive model to assess whether product attributes can forecast retail prices.

### Key Objectives:
1. **Web Scraping:** Extract book titles, prices, star ratings, and stock availability across multiple pages using `BeautifulSoup` and `requests`.
2. **Data Cleaning:** Clean currency symbols, convert textual ratings into numerical values, handle missing entries, and export a structured CSV dataset.
3. **Exploratory Data Analysis (EDA):** Visualize price distributions and category spreads using `Matplotlib` and `Seaborn`.
4. **Predictive Analytics:** Build and evaluate a `LinearRegression` model using `Scikit-Learn` to analyze feature relationships with pricing.

---

## 🛠️ Repository Structure

```text
.
├── README.md                     # Project documentation and setup guide
├── books_to_scrape_clean.csv     # Final cleaned tabular dataset (200 records)
└── notebook.ipynb                # End-to-end Jupyter Notebook (Scraping, EDA, Modeling)
```

---

## Dataset Summary (`books_to_scrape_clean.csv`)

The final dataset comprises **200 individual product records** collected across 10 catalog pages.

| Field Name | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `Title` | String | Full title of the book | *"A Light in the Attic"* |
| `Price_GBP` | Float | Book price in British Pounds (£) | `51.77` |
| `Star_Rating` | Integer | Customer rating encoded from 1 to 5 | `3` |
| `Stock_Availability` | String | Operational availability status | *"In stock"* |

---

##  Key Findings & Insights

1. **Price Distribution:** Book prices on the target site exhibit a right-skewed distribution, with the majority concentrated in lower-to-mid price tiers.
2. **Rating Dynamics:** Star ratings are distributed relatively evenly across catalog offerings; median prices do not vary significantly across star rating tiers.
3. **Predictive Modeling:** 
   * **Model Used:** Linear Regression (`sklearn.linear_model.LinearRegression`)
   * **Train/Test Split:** 80% / 20%
   * **Performance:** $R^2 \approx -0.0085$
   * **Conclusion:** Star ratings and stock availability alone do not hold a linear relationship with retail prices on this platform. Pricing is likely governed by uncaptured features such as book genre or page count.

---

##  Getting Started & Installation

### Prerequisites
Make sure you have **Python 3.8+** installed along with `pip`.

### 1. Clone or Download the Repository
```bash
git clone https://github.com/your-username/data-science-500-assignment.git
cd data-science-500-assignment
```

### 2. Install Required Dependencies
Install the required standard data science packages:
```bash
pip install requests beautifulsoup4 pandas matplotlib seaborn scikit-learn jupyter
```

### 3. Run the Jupyter Notebook
Start Jupyter Notebook to execute the end-to-end data pipeline:
```bash
jupyter notebook notebook.ipynb
```

---

##  Tools & Technologies Used

* **Python 3** - Programming language
* **BeautifulSoup4 & Requests** - Web scraping & HTML parsing
* **Pandas** - Data manipulation, cleaning, and CSV export
* **Matplotlib & Seaborn** - Data visualization
* **Scikit-Learn** - Machine learning pipeline and regression modeling

---

##  Author & Acknowledgments

* **Module:** Data Science 500
* **Data Source:** [Books to Scrape](http://books.toscrape.com/)

## My project repocsitory

* **url: https://github.com/jujuman28/data-science-500-books-to-scrape/upload/main