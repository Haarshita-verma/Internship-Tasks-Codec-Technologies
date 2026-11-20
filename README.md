# Market Basket Analysis

Data Analytics Internship · Project 06

## Run locally

From this folder, create a Python 3 environment and run:

```bash
python -m pip install -r requirements.txt
jupyter lab Market_Basket_Analysis.ipynb
```

The notebook includes executed cells and charts. Use **Run All Cells** to reproduce the analysis.

## Data

Chen, D. (2015). [Online Retail](https://doi.org/10.24432/C5BW33). UCI Machine Learning Repository. [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

The bundled `data/uk_retail.csv.gz` was adapted from the original workbook by keeping only United Kingdom rows and the InvoiceNo, StockCode, Description, Quantity and UnitPrice fields. The notebook filters cancelled invoices and administrative lines, then counts each product once per eligible invoice.

## Results

- 17,901 eligible invoices yielded 1,041 frequent pairs at a minimum support of 1%.
- 838 directional rules met the 30% confidence and lift above 1 thresholds.
- The most frequent pair was **Jumbo Bag Pink Polkadot + Jumbo Bag Red Retrospot**, appearing in 785 baskets (4.39%). Test joint placement to see if it increases add-on purchases.
- **Herb Marker Parsley → Herb Marker Chives** appeared in 187 baskets, with 82.0% historical confidence and 72.32 lift. Test the targeted recommendation on new orders. High lift can reflect a low overall purchase rate for the suggested product.

The results describe historical purchases at one retailer. Use a controlled test to estimate the effect of an offer on sales or margin.
