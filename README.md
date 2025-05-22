# Market Basket Analysis with Apriori Algorithm

This project applies **Association Rule Mining** using the **Apriori algorithm** to uncover hidden patterns in retail transaction data. By analyzing a dataset of customer transactions, the goal is to identify frequent itemsets and generate association rules that reveal which products are often purchased together.

## Dataset

- **Source**: `marketbasket.csv`
- **Description**: A structured CSV file containing transactional data with fields:
  - `transaction_ID`
  - `Date`
  - `Time`
  - `item_0` to `item_40`: items purchased in a transaction

## Tools & Libraries

- Python
- pandas
- numpy
- matplotlib
- apyori

## Methodology

1. **Data Preprocessing**
   - Cleaned the dataset and removed unnecessary columns.
   - Converted transactional records into a format suitable for the Apriori algorithm.

2. **Frequent Itemset Mining**
   - Applied Apriori with various parameter settings for:
     - Minimum Support
     - Minimum Confidence
     - Minimum Lift
     - Minimum Rule Length

3. **Association Rule Generation**
   - Compared rules across different settings to assess quality and significance.
   - Analyzed the presence (or absence) of top-selling items in generated rules.

## Parameter Settings & Results

Three configurations were tested:

| Setting | Min Support | Min Confidence | Min Lift | Rules Generated |
|--------|-------------|----------------|----------|-----------------|
| 1      | 0.015       | 0.7            | 3        | 3               |
| 2      | 0.009       | 0.5            | 3        | 48              |
| 3      | 0.015       | 0.5            | 9        | 10              |

### Observations:
- Some frequently bought items did not appear in rules due to low co-occurrence with other products.
- Rules in Setting 3 revealed higher-lift associations involving popular products like JUMBO BAG RED RETROSPOT.

## Key Insight

> High-frequency items are not always strongly associated with other items. Association mining reveals deeper co-purchase behavior beyond surface-level frequency counts.

## References
- [Apriori: Association Rule Mining — Explanation and Python Implementation](https://towardsdatascience.com/apriori-association-rule-mining-explanation-and-python-implementation-290b42afdfc6) by Chonyy

## Getting Started

To run the notebook:

```bash
pip install pandas numpy matplotlib apyori
