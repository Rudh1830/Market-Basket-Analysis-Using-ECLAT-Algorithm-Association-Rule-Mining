# Market-Basket-Analysis-Using-ECLAT-Algorithm-Association-Rule-Mining

This project applies the ECLAT algorithm to a Market Basket Optimization dataset to discover frequently purchased item combinations.
ECLAT is an efficient association rule mining technique that uses a vertical data format (TID sets) to identify frequent itemsets.

The goal of this analysis is to help retailers understand customer purchase patterns, improve product placement, and design effective cross-selling strategies.

📂 Dataset

Market Basket Optimization dataset

Each row represents a transaction

Each column represents an item purchased in that transaction

⚙️ Algorithm Used

ECLAT (Equivalence Class Clustering and bottom-up Lattice Traversal)

Support-based frequent itemset mining

More memory-efficient than Apriori for large datasets

🧪 Methodology

Data preprocessing (transaction format)

Apply ECLAT with:

min_support = 0.03

min_combination = 1

max_combination = 3

Extract frequent itemsets

Analyze high-support item combinations

Interpret business insights

📊 Results

Identified most frequent single, pair, and triple item combinations

Revealed strong associations between commonly co-purchased products

Useful for:

Bundle offers

Store layout optimization

Recommendation systems

🛠️ Technologies Used

Python

Pandas

NumPy

ECLAT (pyECLAT)

Jupyter Notebook / Kaggle Notebook

🚀 How to Run
from pyECLAT import ECLAT

eclat_instance = ECLAT(data=df, verbose=True)
itemsets, supports = eclat_instance.fit(
    min_support=0.03,
    min_combination=1,
    max_combination=3,
    separator='&',
    verbose=True
)

📈 Future Improvements

Generate association rules with confidence & lift

Compare ECLAT vs Apriori vs FP-Growth

Build a recommendation engine

Visualize item relationships using network graphs

⭐ Why ECLAT?

Unlike Apriori, ECLAT uses TID intersections, making it faster for dense datasets and suitable for real-world retail analysis.
