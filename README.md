# Amazon Delivery: From Probability Distributions to Machine Learning

## Purpose

This project uses a real-world Amazon delivery dataset to make probability mass functions (PMF), probability density functions (PDF), and cumulative distribution functions (CDF) practical and intuitive - and then shows how those same ideas connect naturally to conditional probability and machine learning.

The guiding question: **can probability help us understand and predict delivery times?**

## Learning objectives

By working through this notebook, you should come away able to:

- Understand and compute a PMF from empirical, discrete data
- Understand what a PDF represents (density, not probability) and how probability corresponds to area under the curve
- Understand and compute an empirical CDF, and use it to answer concrete questions about a dataset
- Compare conditional distributions and explain why conditioning on another variable can reveal relationships a single overall distribution hides
- See how a simple ML model (logistic regression) estimates a conditional probability, connecting directly back to the distributions explored earlier

## Dataset

This project uses the [Amazon Delivery Dataset](https://www.kaggle.com/datasets/sujalsuthar/amazon-delivery-dataset) from Kaggle. 

## Project structure

```bash
amazon-delivery-pmf-pdf-cdf/
├── README.md                 # Project documentation
├── amazon-delivery.ipynb     # Main notebook — the full walkthrough
├── data/
│ └── amazon_delivery.csv     # Dataset (see Kaggle link above)
├── requirements.txt          # Python dependencies
└── .gitignore
```


## Setup

```bash
# Clone the repository
git clone <repo-url>
cd amazon-delivery-pmf-pdf-cdf

# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

## Running the project

Open `amazon-delivery.ipynb` in Jupyter and run the cells from top to bottom. The notebook is written to be read as a guided story - each section builds on the previous one, with markdown explaining the reasoning before and after each piece of code.

## Concepts covered

- **PMF** - probability mass function, for discrete variables like `Weather` and `Traffic`
- **PDF** - probability density function, for the continuous `Delivery_Time` variable
- **CDF** - cumulative distribution function, answering "what proportion of deliveries finish within x minutes?"
- **Conditional distributions** - how the distribution of `Delivery_Time` changes when we condition on `Traffic`
- **Probabilistic machine learning** - logistic regression estimating P(Late | features) directly as a probability

## Key takeaway

Probability concepts are tools for describing uncertainty and distributions in data - and that same foundation is what machine learning models are built on. A model that predicts P(Late | features) is doing the same kind of thing we did by hand with PMFs, PDFs, and CDFs, just learned from data across multiple features at once.